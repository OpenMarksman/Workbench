# Agent instructions

This repository holds the project baseline of Workbench (license, CI, release and settings); the code follows. Read `README.md` and `CONTRIBUTING.md` first.

## Commands

- Node 26 (`.nvmrc`) and npm. `npm ci` installs.
- `npm run check` runs Biome (`lint`), knip and jscpd (`dup`), the same as CI. Run it before every push.
- jscpd fails on new clones against `.jscpd-baseline.json`. Remove the clone; do not regenerate the baseline to make the check pass.

## Changes

- Branch from `main` and open one pull request per change into `main`. Pull requests are squash-merged through the merge queue, so the title becomes the commit message.
- The title follows Conventional Commits, checked by `conventional`. `feat`, `fix` and `perf` cause a release; use `ci`, `docs`, `chore`, `test` or `refactor` for the rest.
- Merge only when every required check is green and every review thread is resolved. When a check fails, fix the cause; never skip it (`--no-verify`, an admin merge) or loosen it.
- Workflows: pin each action to a full commit SHA with its version as a comment, and give each job only the `permissions` it needs; actionlint and zizmor check every workflow. A required check also runs on `merge_group`, or the queue waits for it.
- release-please owns the version and the changelog: do not edit `.release-please-manifest.json` or the version in `package.json` by hand.

## Agent skills

### Issue tracker

GitHub Issues, used through `gh`. See `docs/agents/issue-tracker.md`.

### Triage labels

The five default roles, label names equal to the role (`needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`). See `docs/agents/triage-labels.md`.

### Domain docs

Single-context: `GLOSSARY.md` and `docs/adr/` at the repository root. See `docs/agents/domain.md`.
