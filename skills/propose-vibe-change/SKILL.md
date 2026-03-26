---
name: propose-vibe-change
description: Use when the user disagrees with an emoji's meaning, suggests a different vibe for an emoji, wants to add a new emoji to the set, or wants to remove one
---

# Propose Vibe Change

When a user wants to add, change, or remove an emoji vibe, help them open a proposal.

## Steps

1. **Identify the change type:** Is this an add, change, or remove?
2. **Show current state:** Read @../../vibes.json and show the user the current meaning for the emoji (if it exists).
3. **Clarify the proposal:** Ask what they think the vibe should be (for adds/changes) or confirm they want it removed.
4. **Suggest tags:** Propose 3-5 short tags for the emoji (for adds/changes). Let the user adjust.
5. **Open the issue:** Run the `gh` command below with the details filled in.
6. **Tell the user** the issue is open and they can share the link to get votes. Explain: 70% approval within a week (minimum 3 votes) auto-merges the change.

## Issue Creation

Title format: `[add|change|remove] <emoji> — <short description>`

```bash
gh issue create \
  --repo rymarren/emoji-vibes \
  --label "vote-open" \
  --title "[ACTION] EMOJI — SHORT_DESCRIPTION" \
  --body "**Action:** ACTION
**Emoji:** EMOJI
**Current meaning:** CURRENT_OR_NA
**Proposed meaning:** PROPOSED_OR_NA
**Tags:** comma, separated, tags
**Rationale:** USER_REASONING

---
👍 this issue to approve, 👎 to reject. Voting closes 7 days after issue creation. Needs 70% approval with at least 3 votes."
```

Replace the ALL_CAPS placeholders with the actual values from the conversation.
