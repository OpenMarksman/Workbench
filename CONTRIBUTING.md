# Contributing

Questions and ideas go to [issues](https://github.com/OpenMarksman/Workbench/issues); security reports go to [SECURITY.md](SECURITY.md).

## Setup

- Node 26 (`.nvmrc`) and npm.
- `npm ci`, then `npm run check` (Biome, knip and jscpd; CI runs the same).

## Pull requests

- Branch from `main` and open a pull request into `main`. Pull requests are squash-merged, so the title becomes the commit message.
- The title follows [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) (`feat: ...`, `fix: ...`); the check `conventional` enforces it. `feat`, `fix` and `perf` cause a release; release-please writes the changelog from the titles.
- Every required check is green and every review thread is resolved before the merge.
