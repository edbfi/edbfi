# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

This is the `edbfi/edbfi` GitHub profile repo: `README.md` renders publicly on github.com/edbfi the moment it lands on `main`. There is no build, runtime, or test suite; the only checks are the prek content hooks in `prek.toml`.

## Commands

- Full local check (same as CI, which also runs `git diff --exit-code HEAD` after it): `SKIP=no-commit-to-branch prek run --all-files`
- Without `SKIP`, the `no-commit-to-branch` hook fails on `main`. Once hooks are installed (`prek install`), it also blocks commits to `main`; do the work on a branch and open a PR instead.

## Gotchas

- The stats SVGs come from `raw.githubusercontent.com/edbfi/github-stats/generated/...`. This repo can't change what they show; only the embedding markup lives here. To change the stats themselves, work in `edbfi/github-stats`.
- To add an image, copy an existing `<picture>` block from `README.md`. It needs both the `media="(prefers-color-scheme: ...)"` attribute and the `#gh-dark-mode-only` / `#gh-light-mode-only` fragment, and the `<img>` fallback uses the light fragment. Use `raw.githubusercontent.com` URLs, not `github.com/.../blob/...`, which return an HTML page instead of the image.
- Keep the stats images bare, with no wrapping `<a>` and no attribution text under them. Both were removed on purpose (`5a029ba`, `6300e83`).
- Update the `<sub>Last edited: YYYY-MM-DD</sub>` footer in `README.md` by hand, in the same commit as any README content change. Nothing enforces this.
- `edbfi/automation` is pinned at one version in four places: `renovate.json` (the `default.json` and `automerge.json` presets, `#v4.0.0`), `.github/workflows/ci.yml` (the gate `uses:`), and `.github/workflows/pr-policy.yml`. `CI.md` also names it. Leave the bumps to Renovate. For a manual bump, change all of them together.
- Shared Renovate policy lives in the `edbfi/automation` presets that `renovate.json` extends. Make fleet-wide changes there. The shared `automerge.json` preset sets how this repo merges.
- PR policy (`.github/workflows/pr-policy.yml`) requires a Conventional Commit PR title and a matching author sign-off, so commit with `git commit -s`.

## Reference

- `CI.md` explains the CI gate, PR policy, and Renovate merge ownership. Read it before editing workflows, `prek.toml`, or `renovate.json`, or when a required check or merge is blocked.
