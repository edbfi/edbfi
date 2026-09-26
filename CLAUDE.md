# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

This is the `edbfi/edbfi` GitHub profile repo: `README.md` renders publicly on github.com/edbfi the moment it lands on `main`. There is no build, runtime, or test suite; the only checks are the prek content hooks in `prek.toml`.

## Commands

- Full local check: `SKIP=no-commit-to-branch prek run --all-files`
- Without `SKIP`, the `no-commit-to-branch` hook fails on `main`. Once hooks are installed (`prek install`), it also blocks commits to `main`; do the work on a branch and open a PR instead.

## Gotchas

- The stats SVGs come from `raw.githubusercontent.com/edbfi/github-stats/generated/...`. This repo can't change what they show; only the embedding markup lives here. To change the stats themselves, work in `edbfi/github-stats`.
- To add an image, copy an existing `<picture>` block from `README.md`. It needs both the `media="(prefers-color-scheme: ...)"` attribute and the `#gh-dark-mode-only` / `#gh-light-mode-only` fragment, and the `<img>` fallback uses the light fragment. Use `raw.githubusercontent.com` URLs, not `github.com/.../blob/...`, which return an HTML page instead of the image.
- Keep the stats images bare, with no wrapping `<a>` and no attribution text under them. Both were removed on purpose (`5a029ba`, `6300e83`).
- Update the `<sub>Last edited: YYYY-MM-DD</sub>` footer in `README.md` by hand, in the same commit as any README content change. Nothing enforces this.
- Project conventions require a Conventional Commit PR title and a matching author sign-off, so commit with `git commit -s`.

## Reference
