# web-design

**Web interfaces that don't look like every other AI-built page.**

You know the one before it finishes loading: Inter, an indigo-to-violet gradient, a centered headline above three equal cards, a fade-up on every section. None of it is a mistake — it's the *most likely* answer, which is why it all arrives together and why people clock it on sight.

This skill gets you off that default and onto something the page can justify. It also ships the parts that usually go missing: keyboard access, focus states, real error messages, a form that doesn't wipe what you typed.

## How it gets there

**It derives a direction instead of picking one.** Rather than reaching for an aesthetic, it works forward from what the thing actually is — the documents the trade already uses, what the product does, the state the user is in when they arrive. Freight invoicing software derives from the paper bill of lading: carbon-copy pink, dense ruled tables, tabular figures. The test everything gets held to is whether a choice traces back to something specific about your project. If it can't be justified, it's a default, whatever it looks like.

**It knows what the defaults look like.** A catalog of the tells across color, type, layout, spacing, components, effects, imagery, motion, and copy — ranked by how loudly each actually registers, so effort goes where it's noticed. Bento grids and glassmorphism get explicitly demoted; the online version of this list overstates them.

**It checks its own work, twice.** An anti-default audit for taste, where each hit is a question rather than a failure. Then verification for correctness, kept separate and pass/fail: keyboard access, visible focus, contrast, forms that preserve input, nothing fabricated. Your brief overrides every aesthetic rule in the skill, including the ones written as "never". It doesn't override those gates.

**It won't sell you the fashionable escape either.** Cream, serif, and sage is the well-known correction to purple polish, which is exactly what makes it the next template. There's no safe aesthetic — the problem was never purple, it was choosing without a reason.

## Using it

Fires on its own for a landing page, dashboard, form, app screen, or a request to polish existing UI. Or call it:

```
/web-design a landing page for a freight invoicing tool
```

Skip it for a single component inside an existing design system — that inherits its type, palette, and spacing, and needs none of the page-level guidance.

## Installing

```bash
cp -r web-design ~/.claude/skills/
```

Only `SKILL.md` is read by Claude Code; this README rides along and is ignored.
