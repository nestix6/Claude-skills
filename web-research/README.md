# web-research

**Research you can check.**

Ask for research and you usually get back a confident summary with no way to tell which parts are true — claims with no link behind them, a source list bolted on at the end that doesn't match the text, and nothing at all about what the search failed to turn up.

This skill searches, weighs what it finds, and hands it back with every claim linked where it's made, disagreements left visible, and the thin spots labeled as thin. What the research then feeds into is yours to decide.

## What it changes

**It asks once, or not at all.** Purpose and depth are usually inferable — "research X for a blog post" tells you both — so it doesn't spend a turn confirming what you just said. What it does ask for is the thing it genuinely cannot guess: references you already have. Any remaining questions arrive in one message rather than one at a time.

**It reads sources for what would make them wrong.** Can it reach the original study or filing rather than an article describing it — coverage drops caveats and rounds findings up. When was it published, and how fast does this topic move. Who benefits from the claim. Does it link its evidence, or just assert with confident formatting.

**It knows when to stop.** Searching ends when new searches stop changing the report — when the results are pages already read and claims already recorded. Before it stops, load-bearing claims need more than one independent source, and two outlets running the same wire story count as one.

**It tells you what it couldn't find.** Gaps go in the place the claim would have gone: nothing credible on this, sources disagree and here's who holds which position, the best source is paywalled or three years old. If the topic isn't covered at all, it says so and stops rather than padding the report out with content farms.

## Using it

Ask for research on a topic and it applies itself. Or call it:

```
/web-research the current state of EU battery passport regulation
```

Give it any links, PDFs, or prior notes you already have — those anchor the research more than any search will.

Output is a markdown file unless you want something else. Say so up front — a one-pager, a client email, notes for a slide — and it writes to that instead.

## Installing

```bash
cp -r web-research ~/.claude/skills/
```

Only `SKILL.md` is read by Claude Code; this README rides along and is ignored.
