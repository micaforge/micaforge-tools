# Linus Review: micaforge-github + mica-flow

Date: 2026-10-16. Read-only review. I didn't touch anything.

---

## micaforge-github — SHIP

**Does the README describe what the repo actually does?** Yes. "Mica's GitHub identity, org ops, and publishing workflow." That's what it is. The scripts table lists exactly one script (`bin/gh-avatar-prep`), and that script exists. The structure diagram matches the actual tree. No lies.

**Are documented commands real?** Spot-checked `bin/gh-avatar-prep --help` — works. Ran it against a test image — produced a valid 460px PNG. Does what it says.

**Anything embarrassing?** One nit: `SKILL.md:68` references `~/workspace/bin/mica-scaffold`. That's the author's local path, not the repo's. A stranger cloning this has no `~/workspace/bin/`. It's a one-line fix (point at micaforge-tools or use a relative path), not a ship-blocker, but it's the exact kind of thing that makes you look sloppy.

The "GET 1 BILLION TOKENS" referral badge in the footer is marketing fluff, but it's honest about what it is. I've seen worse. It doesn't pretend to be a feature.

**Verdict: SHIP.** Fix the local path when convenient.

---

## mica-flow — SHIP

**Does the README describe what the repo actually does?** Yes. "Multi-cycle flow orchestration for AI agents — briefs, gates, run records." The quick start is real: clone, symlink, scaffold. The usage section describes the actual cycle loop. The scripts table lists all four `bin/` scripts, and all four exist. The structure diagram matches.

**Are documented commands real?** Spot-checked `bin/mica-flow-status --help` — works, prints real usage. Read the first 20 lines of `bin/mica-flow` — it's real Python that scaffolds the described directory structure. The templates (`AGENT.md`, `RUNBOOK.md`, `TODO.md`, `a00-scaffold/` with `cycle.md` + `BRIEF.md`) all have substantive content, not placeholders.

**Anything embarrassing?** No. I checked for the TODOs a previous audit flagged — they're gone. Someone did the work. The `hooks/pre-push` is a real secrets-audit hook, not a stub.

One observation: the SKILL.md entry points table documents `mica flow run` / `status` / `complete` / `close` (the cap interface), while `bin/` contains the legacy shims. The SKILL.md does note "`mica-flow` | legacy shim for the above," so it's not lying — but a new user might wonder which interface is canonical. Worth one clarifying sentence. Not a blocker.

**Verdict: SHIP.**

---

## Summary

| Repo | Verdict | Blocker |
|------|---------|---------|
| micaforge-github | SHIP | None (one local-path nit in SKILL.md:68) |
| mica-flow | SHIP | None |

Both repos are honest about what they do. The docs match the code. Nothing here would embarrass the author. Ship them.
