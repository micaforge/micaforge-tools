# micaforge-tools

Shared tooling for the micaforge org — scaffolding, media, and repo ops.

## Use when

- Starting a new repo (scaffold it instead of building from scratch)
- Generating and placing repo media (icons, banners)
- You need the org's shared scripts

## Quick start

```bash
mica-scaffold <slug> --type project|agent --title "Name" --tagline "..."
mica-media-place <slug> <image> <name> --readme
```

## Scripts (bin/)

| Script | When to use |
|--------|-------------|
| `mica-scaffold` | New repo. Fills the template README, adds MIT license, creates private GitHub repo, pushes. Use `--type agent` for skill packages (adds SKILL.md, workflows/, tools/). |
| `mica-media-place` | Generated an icon/banner. Converts to PNG, places in `assets/`, optionally rewires README img tag, commits. |
| `mica-sync` | Package changed locally (or in repo). Syncs SKILL.md, bin/, workflows/, tools/, references/ between `~/workspace/custom-skills/<pkg>/` and the repo. `--push` to commit+push. |

## Workflows

- Scaffold → customize README → generate icon → `mica-media-place` → push → flip public when ready.

## References

- Template: `micaforge/micaforge-template` (README.template.md, PACKAGE.md)
- Media workflows: `~/workspace/micaforge/content/media-workflows.md`
