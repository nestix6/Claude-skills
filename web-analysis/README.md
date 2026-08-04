# web-analysis

**Paste a link. Get the whole site in one summary.**

What it's for, what it does, how it's designed, and the details you'd otherwise click through four pages to find — condensed into something short enough to actually read.

Useful when you're pitching a client and want their current site read back to you before the call, sizing up a competitor, or picking apart a design you like to work out what's holding it together.

## Two passes, one summary

The **design** pass reads the visual system: layout and grids, navigation, buttons and forms, typography, color palette, and the patterns that recur across the page.

The **information** pass reads the site as a business: purpose, key features, locations, contact details, opening hours.

They stay separate because "what does this look like" and "what does this actually do" have different answers, and running them together produces a vague impression of both.

## Feed it into a redesign

The design half of the output is close to what [web-design](../web-design/) wants as input — an existing visual system to work within, or a reference to derive from. Analyze the current site, hand the result over, redesign against it.

## Using it

Paste a link and ask for an analysis. Or call it:

```
/web-analysis https://example.com
```

It reads the page with a browser automation tool where one is available (Chrome DevTools MCP, Playwright, Puppeteer), since that runs the site's JavaScript and exposes computed styles. Plain fetch is the fallback, and on a client-rendered site it returns an empty shell — in which case the skill says so and stops rather than describing a page it never saw. Every summary states which method was used and what it left unseen.

## Installing

```bash
cp -r web-analysis ~/.claude/skills/
```

Only `SKILL.md` is read by Claude Code; this README rides along and is ignored.
