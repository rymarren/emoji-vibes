# emoji-vibes

Emoji vibes for Claude Code. Teaches Claude which emojis to use and when.

## Install

From the marketplace:

```
claude marketplace add emoji-vibes
```

Or directly from GitHub:

```
claude install-plugin rymarren/emoji-vibes
```

### Staying up to date

After installing, enable auto-update for the marketplace so you get new vibes automatically:

1. Open `/plugin` in Claude Code
2. Go to the **Marketplaces** tab
3. Enable **auto-update** for emoji-vibes

If auto-update isn't picking up changes, you can manually refresh:

```
/plugin marketplace update emoji-vibes
/reload-plugins
```

## Vibes

| Emoji | Vibe |
|-------|------|
| 🫡 | Acknowledging instructions, confirming understanding, got it |
| 🚢 | Shipping code, pushing PRs, merging, wrapping up work |
| 🚀 | Launching something new, excitement, big moves |
| ✨ | General good vibes, something came together nicely, chef's kiss moments |
| 😩 | When stuff just isn't going right, frustrating failures, things fighting back |
| 🧐 | Digging into something, investigating, really scrutinizing |
| 🤠 | Wilding, yoloing, running commands on prod, living dangerously |
| 🧹 | Sweeping away dead code, removing cruft, cleaning up leftovers |
| 🧼 | Something is clean, tidy, well-organized |
| 🤌 | Chef's kiss, something is perfect |
| 🔥 | Hype, locked in, let's fucking go, pure momentum energy |
| 🧠 | Big brain mode, deep focus, in the zone, flow state |
| 👀 | Side eye, judging your choices, you sure about that? |
| 🤯 | Mind blown, something truly insane just happened, can't believe that worked |
| 💎 | Found something valuable, key insight, this is the important bit |
| ⛏️ | Struck gold, hit the jackpot on a search, dug up exactly what we needed |
| 🏎️ | Blazing fast, optimized the hell out of something, speed demon energy |
| 🧘 | Letting it be, accepting complexity, releasing what you can't control, not every problem needs solving |

## Propose a Change

Think a vibe is wrong, missing, or needs to go? Just tell Claude — say something like "I think 🤠 should mean something different" or "add a skull emoji" and it'll open an issue on this repo with your proposal.

## Versioning

Plugin updates are delivered through `plugin.json` — bumping its version triggers updates for installed users without needing to update the marketplace listing. The marketplace is just for discovery.
