# Propose Vibe Change — Redesign

## Summary

Rewrite the `propose-vibe-change` skill so that anyone with the plugin installed can propose emoji vibe changes by opening a structured GitHub issue on `rymarren/emoji-vibes`. Tries `gh` first, falls back to `curl` with `GITHUB_TOKEN` if `gh` isn't installed.

## How It Works

When a user says something like "I think 🤠 should mean something different" or "add a skull emoji":

1. **Identify change type** — add, change, or remove
2. **Check current state** — read `skills/apply-vibes/SKILL.md` to see if the emoji exists and what it currently means
3. **Clarify with user** — confirm the proposed meaning (for add/change) or confirm removal
4. **Open issue** — try `gh issue create` first. If `gh` is not installed, fall back to `curl` with `GITHUB_TOKEN` to `POST /repos/rymarren/emoji-vibes/issues`.

## Issue Format

**Title:** `[add|change|remove] <emoji> — <short description>`

**Body:**
```
**Action:** add|change|remove
**Emoji:** <emoji>
**Current meaning:** <current meaning or N/A>
**Proposed meaning:** <proposed meaning or N/A>
**Rationale:** <user's reasoning>
```

## What Changes

- `skills/propose-vibe-change/SKILL.md` — rewritten to the new flow
- No other files change

## What Doesn't Change

- `skills/apply-vibes/SKILL.md` — untouched, remains the source of truth for vibes
- `README.md` — untouched
- No new files, no new dependencies

## Maintainer Side

Ryan reviews incoming issues and makes the change directly (or has Claude do it). No automation needed — just review and act.
