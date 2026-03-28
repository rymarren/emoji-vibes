---
name: propose-vibe-change
description: Use when the user disagrees with an emoji's meaning, suggests a different vibe for an emoji, wants to add a new emoji to the set, or wants to remove one
---

# Propose Vibe Change

When a user wants to add, change, or remove an emoji vibe, help them open a proposal as a GitHub issue.

## Steps

1. **Identify the change type:** Is this an add, change, or remove?
2. **Show current state:** Read `skills/apply-vibes/SKILL.md` to check the current meaning for the emoji (if it exists).
3. **Clarify the proposal:** Ask what the vibe should be (for adds/changes) or confirm removal.
4. **Open the issue:** Use `gh` if available, otherwise fall back to `curl`. See below.
5. **Tell the user:** Share the issue link so they can track it.

## Opening the Issue

**Title format:** `[add|change|remove] <emoji> — <short description>`

### Try gh first

```bash
gh issue create \
  --repo rymarren/emoji-vibes \
  --title "[ACTION] EMOJI — SHORT_DESCRIPTION" \
  --body "**Action:** ACTION
**Emoji:** EMOJI
**Current meaning:** CURRENT_OR_NA
**Proposed meaning:** PROPOSED_OR_NA
**Rationale:** USER_REASONING"
```

### If gh is not installed, fall back to curl

```bash
curl -s -X POST \
  -H "Authorization: token $GITHUB_TOKEN" \
  -H "Accept: application/vnd.github+json" \
  https://api.github.com/repos/rymarren/emoji-vibes/issues \
  -d '{
    "title": "[ACTION] EMOJI — SHORT_DESCRIPTION",
    "body": "**Action:** ACTION\n**Emoji:** EMOJI\n**Current meaning:** CURRENT_OR_NA\n**Proposed meaning:** PROPOSED_OR_NA\n**Rationale:** USER_REASONING"
  }'
```

Replace ALL_CAPS placeholders with actual values from the conversation.

## Current Vibes

- 🫡 — Acknowledging instructions, confirming understanding, got it
- 🚢 — Shipping code, pushing PRs, merging, wrapping up work
- 🚀 — Launching something new, excitement, big moves
- ✨ — General good vibes, something came together nicely, chef's kiss moments
- 😩 — When stuff just isn't going right, frustrating failures, things fighting back
- 🧐 — Digging into something, investigating, really scrutinizing
- 🤠 — Wilding, yoloing, running commands on prod, living dangerously
- 🧹 — Sweeping away dead code, removing cruft, cleaning up leftovers
- 🧼 — Something is clean, tidy, well-organized
- 🤌 — Chef's kiss, something is perfect
- 🔥 — Hype, locked in, let's fucking go, pure momentum energy
- 🧠 — Big brain mode, deep focus, in the zone, flow state
- 👀 — Side eye, judging your choices, you sure about that?
- 🤯 — Mind blown, something truly insane just happened, can't believe that worked
- 💎 — Found something valuable, key insight, this is the important bit
- ⛏️ — Struck gold, hit the jackpot on a search, dug up exactly what we needed
- 🏎️ — Blazing fast, optimized the hell out of something, speed demon energy
- 🧘 — Letting it be, accepting complexity, releasing what you can't control, not every problem needs solving
- 💀 — So bad it's funny, I'm fucking dead, can't even, comedic disaster
