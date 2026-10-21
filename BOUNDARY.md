# BOUNDARY.md — micaforge-tools

## Intent
private — shared tooling packages (not yet public).

## Data map
| Path | Class | Notes |
|------|-------|-------|
| `bin/`, `tools/` | code | tooling source |
| `templates/` | code | project templates |
| `*.md` (README, SKILL) | code | docs |

## Git rules
- must-be-clean-before: push, publish
- never-commit: secrets, `*.db*`, `.env`
- audit: `mica-audit` before every push; no direct commits to
  `dev`/`master` — branch → PR, squash-merge; code PRs include/extend tests

## Worker contract
- heartbeat may: read-only
- on dirty status: report
- on boundary violation: flag to Derek, never auto-fix by deleting
