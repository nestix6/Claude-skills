---
name: web-design
description: Design and build websites and web interfaces with a deliberate visual point of view. Use when creating or redesigning a landing page, dashboard, form, web app screen, component, or artifact, or when asked to style, polish, or improve existing web UI. Produces working code whose design choices trace to the project rather than to generic AI defaults, then verifies breakpoints, interaction states, and accessibility before handing off.
---

This skill guides the creation of distinctive frontend interfaces. Implement real working code with exceptional attention to aesthetic details.

The user provides design requirements: a component, page, application, or interface to build. They may include context about the purpose, audience, or technical constraints.

**Scope this to the ask.** What follows assumes an interface designed from scratch. Trim it to the actual request — a single component inside an existing system inherits that system's type, palette, and spacing, and needs none of the page-level structure guidance. Sections that are narrower say so.

**The user's request outranks the taste rules here.** An explicit instruction, an existing brand, or an established design system overrides every aesthetic prohibition in this file, including the ones written as "never" — the purple gradient, pure `#000`, emoji icons, a centered hero above three cards, Inter. Comply, then name the tension once in the handoff. Arguing with the brief, or quietly delivering something other than what was asked for, is the worse failure.

**It does not override the pass/fail gates in Verification** — keyboard access, visible focus, contrast, a form that doesn't destroy what was typed, content that isn't fabricated. Those are correctness, not preference, and "make it cleaner" is not a request to remove them. Where an instruction genuinely can't be met without breaking one, say which one and offer the nearest version that holds.

**Verification scales with the change, but never to zero.** Every handoff runs the core checks in Verification; anything page-sized runs all of them. State plainly what you could not check.

## Design Thinking

Before coding, understand the direction the user wants to take with the design and commit to it:

- **Purpose**: Who uses this interface and what problem does it solve? What is the context of the design?
- **Kind**: Does this page _argue_ (marketing, editorial, campaign), _transact_ (checkout, signup, booking), or _operate_ (dashboard, admin, settings, internal tool)? The kind sets how much novelty is appropriate before anything else does. A page that argues has to be memorable or it has failed. A page that operates mostly has to disappear into the task, and "boring, correct, fast" is a legitimate and often superior answer there — most of the page-level structure guidance below is written for the first kind.
- **Tone**: Pick a style: minimalist, maximalist chaos, retro-futuristic, organic/natural, luxury/refined, playful/toy-like, editorial/magazine, etc. Use these for inspiration but design one that is true to the user's direction. **Tone covers the writing as much as the visuals** — decide how the page is written in the same breath as how it looks: terse or expansive, plain or ornate, dry or warm, formal or direct. A page whose type is severe and whose copy is chatty has two directions and reads as neither.
- **Constraints**: Technical requirements (framework, performance, accessibility).
- **Differentiation**: What is the one thing someone will remember after leaving the page? Name it before you build, then give it disproportionate weight — the first screen, the largest type, the only place motion does real work, whatever it takes to make it the thing the page is _about_. A page where every section got equal effort has no answer to this question. On an argue-kind page, being correct but unmemorable is a failure, not a safe result.

- **CRITICAL**: Choose a clear conceptual direction that aligns with the user's vision and execute it with precision. Bold maximalism and refined minimalism both work - the key is intentionality, not intensity. Elegance comes from executing the direction well rather than from adding more, so match implementation complexity to what the interface actually requires, not to how elaborate the aesthetic sounds. When the direction calls for density, keep it organized chaos — visually busy but clearly structured. When it calls for restraint, restraint _is_ the bold choice.

**Familiar is not the same as generic.** Generic means _unchosen_, not _common_. A convention is a usability asset — a checkout that behaves like a checkout, a table that sorts the way tables sort, navigation where the eye already expects it — and breaking one costs the user real effort, which the design has to be worth. So set a novelty budget: decide where this interface is unusual and where it stays ordinary, and spend the budget on the few places that carry the direction — the type, the composition, the way the core content is displayed, the voice. Deciding which parts are conventional is part of the design, not a failure to design them.

If the brief is thin, do not stall on questions. Pick a direction, state it in one line, and build. Ask the user to clarify — ideally with examples of what they like and dislike — only when two readings of the brief would produce materially different work.

**Deriving the direction.** Every notable choice should trace back to something specific about this project rather than to taste in general — but that test is easy to apply after the fact and useless for generating anything. Work forward from the subject instead, in one pass, and write the chain down so the handoff can state it:

1. **Name the subject concretely.** Not "a fintech site" but "software that reconciles freight invoices, used by brokers for eight hours a day."
2. **Find what it derives from.** Look first for a **physical or documentary reference**: what does this thing already look like in the world? A material, a document, a machine, an environment, an artifact of the trade. Freight brokerage has an obvious one, the paper bill of lading, with its carbon-copy pink and yellow, dot-matrix figures and dense ruled tables. Plenty of subjects have none, and forcing one is where this procedure fails — a reference that doesn't fit produces decoration with a backstory. So work down instead:
   - **The verb.** What the product _does_ usually has a physical analogue even when the product doesn't. Rate limiting is a valve. Reconciliation is matching two columns. Scheduling across time zones is a timetable. Deleting an account is a lever with a guard over it.
   - **The condition the user is in** when they arrive. Every product has one, so this never comes back empty, and it drives density, contrast, motion tolerance and tone more directly than any visual reference does. Mid-incident at 2am. Eight hours a day, five days a week. Deciding whether to spend £14,000. Waiting, bored, on a phone.
   - **The constraint that actually shapes the thing** — latency, regulation, trust, scale, or the plain fact that nobody wants to be here. A tax product's real constraint is dread, and that is a design brief.
   - **Any existing brand asset**, which outranks everything above it whenever one exists.
3. **Read the specifics off the reference — the writing as well as the look.** The carbons give the neutrals: a yellowed paper white, a carbon-smudge near-black. The pink copy gives an accent that is already the trade's own signal color. The ruled tables say hairline rules, not cards. The dot-matrix figures say tabular numerals and a mono reserved for quantities rather than used as decoration. The reference also sets how the page is written: a bill of lading is terse, declarative and numeric — it states quantities and consignees and never sells — so a page derived from one uses short factual sentences and no brochure language. Both come off the reference in the same pass.
4. **Edit it against the job.** Eight hours a day means desaturating that paper white further and spending the pink only on exceptions instead of on furniture. The reference proposes; the use case decides.

**The brand name is not a subject.** Deriving from the word is the weakest move on that list and normally produces a pun: it works only when the name happens to describe something the product genuinely does. A web studio called Click can derive from the mechanical click, because engaging and committing is what the work actually is; the same studio called Meridian would get navigational-instrument decoration bearing no relationship to building websites. If the name is all you have, you are missing step 1, not finishing step 2 — go back and describe the subject.

The result of step 4 is the direction, and every choice in it answers "why this?" with something other than "it looked good." Where the reference is silent — motion, density, radius — ask what the subject would do rather than what looks nice.

**The literals in this file are shapes, not values.** Every hex, ratio, grid declaration, and class string below illustrates the _kind_ of decision being described. Reused verbatim across projects they produce a new house style — this file's — which fails the test above exactly as squarely as the defaults it replaces.

Then implement working code (HTML/CSS/JS, React, Vue, etc.) that is **both** of the following. Neither one buys you the other, and neither is the safe answer when the work gets hard:

- **Production-grade and functional.** It works, in every state, for everyone, on every width. A beautiful page whose form eats your input is a broken page.
- **Visually striking and memorable, with a clear aesthetic point-of-view.** It is worth looking at and hard to forget. A page that is merely correct has failed at the half of the job people actually see — "at least it's accessible" is not a design.
- **Written, not filled in.** A site expresses as much through its words as through its design, and the copy is the only part that can make a specific claim. Placeholder prose under a considered layout is a half-finished page, not a finished one awaiting content.

Refined in every detail, which is where the two meet: the same care that catches a missing focus ring catches a headline set two points too small.

**Output format**: Match the project's existing stack — framework, styling approach, file layout. For standalone work with no existing project, prefer a single self-contained file. Confirm before introducing a new dependency the project doesn't already have.

**Which libraries to reach for: take capability and correctness, never appearance.** A library that supplies a _capability_ you would otherwise have to build — timeline orchestration, SVG morphing, virtualised lists — leaves every design decision yours; nobody can tell which animation engine a page used. A library that supplies _correctness_ — focus management, ARIA wiring, keyboard behaviour — is better than what you would hand-roll, and this file's accessibility gates are hard to pass without one. Both are named where they come up below. A library that supplies _appearance_ is the default cascade with a package name: component galleries indexed by effect rather than by function, where the pieces are called things like glass-card, beams-background, or gradient-button. Reading one to see how an effect is built is a good use of an afternoon. Installing one puts a look on the page that has no reason behind it, which is the thing this file exists to prevent.

If you are working on a page that already has an established design, consistency wins by default: reuse its type scale, palette, spacing rhythm, and component vocabulary. Be bold _within_ that vocabulary — through composition, hierarchy, and motion — rather than against it. Introduce a new primitive only when the existing system genuinely cannot express the idea, and say so explicitly when you hand off.

---

## Why interfaces read as AI-generated

Interfaces read as AI-generated because they are **generic**, not because they are ugly. Inter is a good typeface. `rounded-2xl` is a reasonable radius. Three feature cards is a functional layout. Nothing below is a _mistake_ — each is the _median_ choice, and the median is invisible. Generic is worse than ugly, because ugly is at least memorable.

What viewers actually register is sameness — "they all look the same" — and only then do they go looking for a reason. They rarely name the purple gradient consciously. **This means fixing tells one at a time does not work.** Every tell catalogued in this file can be removed and the result can still read as AI, because the underlying problem is the absence of a decision, not the presence of a specific color.

Four mechanisms produce every version of this, including versions not yet catalogued. Counter them at the source:

1. **Distributional convergence.** The model emits the median of its training data, and the median is by definition unmemorable. _Counter: anchor every choice to something specific about this project, so the median is out of reach._
2. **The default cascade.** Framework defaults — Tailwind's indigo, shadcn's Inter and Lucide, the tutorial card — were over-represented in tutorials and became the baseline. _Counter: replace defaults at the config level rather than overriding them per component, so the defaults are already yours._
3. **Screenshot bias.** Training data shows resting states; everything a user has to trigger is nearly invisible in it. _Counter: interaction states and accessibility are part of the deliverable, not a polish pass._
4. **The feedback loop.** AI output is now training data, so each generation converges harder. The tells get _stronger_ over time, and today's escape hatch becomes tomorrow's tell. _Counter: none at the source — unlike the first three, this one cannot be escaped by finding a better answer, because any answer good enough to spread becomes the next median. It can only be survived by deriving again each time. This is why the catalogue below has a shelf life and the second-order trap near the end is a permanent condition rather than a list of currently-tired styles._

**The derivability test — the one that generalizes:** every notable choice — typeface, palette, radius, layout, motion, section order — should trace back to a reason specific to this project: the subject matter, the audience, the actual content, an existing brand, a physical material, a real constraint. A choice that can't be justified is a default, whatever it looks like. If you can't explain why this typeface and not another one, you defaulted. (Deriving the direction, above, is the procedure that produces choices which pass it; everything below only detects choices that don't.)

### Where to spend effort first

The strongest tells are all _defaults_: the color that wasn't picked, the component that wasn't restyled, the layout that wasn't questioned. In rough order of how loudly they register:

1. Framework/component defaults left untouched
2. "AI purple" — the indigo/violet-to-blue gradient
3. Centered hero + three-card row
4. Gradient text on the headline
5. Unprompted neon glow
6. Emoji used as icons

Two corrections to the popular version of this list. **Bento grids, glassmorphism, and aurora/mesh backgrounds are weak signals, not fingerprints** — they are legitimate techniques and rank far lower in practice than online discourse claims; don't avoid them reflexively. And **loud, nameable tells are over-represented** because they are easy to articulate. "The spacing is uniform so nothing has hierarchy" has no snappy name but matters more than most of the list. Spacing, hierarchy, and interaction states deserve more attention than their fame suggests.

## Color

**Never the indigo→violet→blue gradient** — `#6366F1 → #8B5CF6 → #3B82F6`, Tailwind's `indigo-500`/`violet-500`/`blue-500` — behind hero headlines, on primary CTAs, in background orbs, or on section accents. It is the loudest single tell. Purple there carries no semantic load: it isn't the brand color, it doesn't encode state, it doesn't relate to the product. It is decoration standing where a decision should be. It arrives because Tailwind uses indigo as the accent throughout its own docs, thousands of tutorials copied that verbatim, and models trained on the result predict the most likely token after `bg-`.

- **Replace framework palettes, don't extend them.** In a Tailwind project, clear the default color scale and define your own rather than adding alongside it, so `indigo-600` is not reachable as a fallback. Express the result as CSS custom properties, so the palette stays one decision instead of fifty scattered literals.
- **Never pure `#FFFFFF` or `#000000`**, and no literal gray borders. Real design systems almost never use pure values — physical white is warm or cool, physical black is brown-black or blue-black. Pure values look like an unconfigured default because that is exactly what they are. Tint neutrals toward the accent hue or a deliberate temperature: `#f6f5f1` warm off-white, `#1a1814` warm near-black. **This single change does more work than almost anything else here.** Tint toward _this_ project's reason, though, not toward those two values — warm off-white plus a serif display face plus generous whitespace is itself a house style, and a recognizable one; see the second-order trap below.
- **Three hues carry the design; anything past that has to be doing a job.** One dominant (~60%), one neutral (~30%), one sharp accent (~10%), with everything else a tint or shade of those three. The percentages are a rough target rather than something to measure: what matters is that one surface dominates and the accent goes to the single most important action on the page instead of being sprinkled. Color doing semantic or functional work sits outside that budget entirely — chart series, status and severity systems, category coding, wayfinding in a large product, and directions that are deliberately polychrome (maximalist, editorial, children's, games). What the cap prevents is decorative hue accumulation, not color.
- **Color in small equal doses everywhere is the failure mode** — a colored icon here, a colored badge there, a colored border strip, so nothing dominates. That's risk-averse averaging: no hierarchy, no attention direction. Real design commits.
- **Derive the accent from something real**: the product's domain, an existing logo, a physical material, a photograph.
- **Color is never the only thing encoding a value.** Not for chart series, not for status and severity, not for a field that failed validation, not for which item is selected. Roughly one man in twelve cannot separate the two hues you picked, and nobody at all can hear them. Pair every color signal with a second channel — a label, a shape, a position, an icon, a word. This applies wherever data is drawn, not only on dashboards.
- If a flat color "looks plain" and the instinct is to reach for a gradient, the flatness isn't the problem — the color choice is.

## Typography

**Avoid the default set**: Inter, Roboto, Poppins, Space Grotesk, Geist, Arial, system-ui — especially at default line-height and default letter-spacing with `font-bold` on headings as the only hierarchy device. Inter in particular is shadcn/ui's default, so every project scaffolded from it starts there unless someone intervenes, and _unchosen_ Inter signals that no typography decision was made at all.

- **The count isn't the decision; choosing is.** Two typefaces chosen for tone is the common answer — a display face with character for headings, a workhorse for body — and one face deployed deliberately across a full range of weight, size, and tracking is equally a decision, frequently the better one for applications, dashboards, technical products, and anything multilingual, where glyph coverage and legibility at 13px outrank personality. Inter, Roboto, and `system-ui` are widely used partly because they are genuinely excellent at UI sizes. What reads as absent is an _unconsidered_ face, not a single one.
- **Build hierarchy from a scale**, not from bold alone. Pick one mathematical ratio (×1.25 or ×1.333), derive sizes from it, and use weight and spacing as the other two levers.
- **Body text ≥16px**, measure capped around 60–75 characters.
- **Touch the details defaults never touch**: negative tracking on large display text, tightened leading on headings, deliberate optical alignment.
- If a project has real reason to use one of the default faces, _earn_ it: an unusual weight, tightened tracking, a distinctive scale.
- **Where the project can load a font, choose a real one — a local stack is the fallback, not the default.** Typeface does more for a page's character than any other single decision, and when the build can fetch a file the entire catalogue is available; assembling a stack out of whatever happens to be installed is a constraint being obeyed, and obeying it when it doesn't apply leaves most of the available character on the table. Decide how it arrives before committing to it, because a webfont that fails to load falls back to a system face — exactly the generic look this file exists to avoid — and it fails silently. Self-host or use a font CDN, always with `font-display: swap` and a real fallback stack behind it rather than a bare `sans-serif`, and subset it so the payload is tens of KB rather than hundreds.
- **Only where external requests are actually blocked** — Claude artifacts, most embedded previews, strict CSP — does that stop working, and there a Google Fonts `<link>` does nothing at all rather than failing loudly. Either embed a subsetted face as a base64 `data:` URI, or build the type system from locally available faces and take distinctiveness from scale, weight, tracking, and case instead. Characterful local stacks beat Inter — `"Iowan Old Style", "Palatino Linotype", Palatino, Georgia, serif` or `Futura, "Trebuchet MS", Optima, sans-serif` — and always chain to a generic family, since the first choice is platform-dependent.

**Skip the decorative tics.** A cluster of small moves that were fresh once and are now reflexes:

- One serif-italic word dropped into an otherwise sans headline ("Build _beautiful_ things") — the most reliable of the three
- All-caps letterspaced section labels above every heading. **Count this one rather than judging it** — each label is defensible alone and the tell exists only in aggregate, which is why it survives every taste review. Roughly one per three sections is the ceiling, with any hero label counting as the first. Over budget, delete the label instead of rewording it: a section's position on the page already says what it is
- Monospace used decoratively for eyebrow text and badges

Each is a recognizable "add sophistication" gesture with no relationship to the content. Use them only when the meaning justifies the emphasis. Test: if the italic word could be swapped for any other word in the sentence without loss, delete the italic.

## Layout & page structure

**Avoid the centered hero + three cards** — the single most stereotyped structure on the web:

```
        [ small pill badge with sparkle/emoji ]
             Big Centered Headline Here
      One supporting sentence, also centered.
        [ Primary CTA ]  [ Secondary CTA ]
    - - - - - - - - - - - - - - - - - - - - -
   ┌─────────┐   ┌─────────┐   ┌─────────┐
   │  icon   │   │  icon   │   │  icon   │
   │  Title  │   │  Title  │   │  Title  │
   │  desc   │   │  desc   │   │  desc   │
   └─────────┘   └─────────┘   └─────────┘
```

This is the layout Tailwind tutorials used to _demonstrate a grid_ — pedagogical scaffolding absorbed as a design pattern. The pill badge above the H1 is its most recent addition and now travels with it almost universally. Perfect symmetry is the absence of editorial judgment: real layouts have a dominant element and subordinate ones, not three equal ones. Three is suspicious in itself, since real products rarely have exactly three equally important features — three usually means the grid chose the count, not the content.

- **Decide the viewing order first** — what the viewer sees first, second, and third — then build the hierarchy to enforce it. Asymmetry, overlap, diagonal flow, grid-breaking elements, generous negative space, and controlled density are the means to that end; deployed without an order to express, they are decoration with extra steps.
- **Break symmetry structurally**, e.g. `grid-template-columns: minmax(2rem, 1fr) minmax(0, 38rem) minmax(0, 1fr);` with content in column 2 and art bleeding off the right edge via `grid-column: 2 / -1`.
- **Let counts follow content** — 2, 4, 5, or one hero feature plus three minor ones. Vary card weight so one is visually dominant. This governs every repeating set on the page, not only cards: numbered steps, pricing tiers, nav items, benefit bullets, footer columns. Three is the count that arrives by rhythm rather than by content, and a three-step "how it works" is the same failure as three feature cards wearing a list.
- **Left-align long-form text.** Centered text is for short statements only.

**Don't ship the stock skeleton in stock order:**

`Hero → feature cards → logo cloud ("Trusted by") → how-it-works (numbered 1·2·3) → stats banner → testimonials → pricing tiers (3, middle one highlighted "Most Popular") → FAQ accordion → CTA band → footer`

The sections aren't wrong — most are legitimate. Arriving in the same order with the same weight every time is. That's a template being filled, not an argument being made. Decide what this specific page must prove and order sections by that argument, cut anything that can't be filled with real content, and vary treatment down the page — alternate density, background, alignment, rhythm — so the page has a shape rather than a stack.

### Dashboards and data-dense UI

Everything above assumes a page that argues. A dashboard reports, and some of it inverts — density is the goal rather than a compromise, and the whitespace that gives a landing page room makes an admin tool feel empty and slow to scan. Hierarchy still comes from spacing, just at a smaller amplitude. The stock skeleton has its own recognizable form:

`left sidebar → top bar with search and avatar → row of four KPI stat cards → one wide line chart → one table`

- **Not every number needs a card.** Four bordered, shadowed stat tiles in a row is the dashboard's version of three feature cards. Metrics that are read together belong on one surface, divided by rule lines or spacing — promote the one or two numbers the user opened the page for, and let the rest be a compact list.
- **A number without a comparison is decoration.** "1,247" tells nobody anything on its own — against what? Give every headline metric a baseline: the previous period, a target, or the same metric elsewhere. A `+12%` delta with no period attached is furniture in the same sense the floating social-proof badge is, and where _down_ is the good direction, say so rather than leaving it to the arrow.
- **The table is the product, not a component sitting beneath it.** Right-align numerals in tabular figures so digits stack, left-align text, and give the identifying column more weight than the rest. Sorting, filtering, and pagination are functionality to build, not chrome to draw. Skip zebra striping by default — it treats a row-tracking problem that adequate row height and a row hover state solve better.
- **Design against realistic data, not tidy data.** Invented rows come out conveniently uniform — eight of them, names that fit their column, no nulls, every number the same digit count — and a layout that has only ever met tidy data breaks on contact with real data. Real data has a 60-character company name, a null in the middle column, one row reading `1` and the next `4,182,993`, and forty thousand rows behind the first page. Populate with the longest, emptiest, and largest values the schema permits, and decide what truncation does — ellipsis, wrap, or tooltip — rather than discovering it later.
- **Charts get the same palette discipline as everything else.** Eight bright categorical hues is the charting-library default and looks like it. Use one accent with tints for series in the same family, and reserve a second hue for genuine contrast.
- **A real zero and a broken pipeline look the same.** The empty-state rules under Behavior & interaction apply here with the stakes raised: nobody merely reads a dashboard, they make a call on it, so an unlabelled empty chart is a decision taken on data that may not exist. Distinguish the two every time.

## Spacing

**Uniform spacing is a hierarchy failure that hides in plain sight.** Identical padding on every element (24px is the common value), identical gaps between every section, no density variation. Whitespace is a hierarchy tool; uniform whitespace means hierarchy was never expressed, and the page reads flat even when every individual element is fine.

Use an 8pt grid (4 as a half-step) but **vary within it**: tight grouping for related items, generous separation between sections.

**The squint test:** shrink the page to a thumbnail. Structure should still be visible. If it's an even gray field, the spacing is doing no work.

## Components & surfaces

**Restyle the primitives before building anything.** Change the radius scale, the shadow definition, and the padding baseline in the config itself. Overriding at the component level leaves stock values reachable, and they resurface.

**Restyle the appearance; do not hand-roll the behaviour.** A combobox, a menu, a tab set, a date picker and a dialog are each a week of edge cases wearing a simple shape: type-ahead, roving focus, `aria-activedescendant`, the arrow keys, the escape hatch, what happens on mobile. Hand-written versions of them are where the keyboard rules in Verification actually break, and they break invisibly, because everything looks right. **Headless libraries solve exactly this and impose no appearance** — `<dialog>` for the case it covers, then Radix Primitives in React, Ark UI where the project isn't React, or React Aria when the accessibility bar is the point and you want hooks-level control. They ship behaviour with no styles at all, so the entire visual argument stays yours and you are only spared the part that was never a design decision.

- **Avoid stock card values** — `rounded-2xl shadow-lg p-6` untouched is the most-cited tell of all. (Worth getting right: that exact trio is the Tailwind _tutorial and marketing-page_ idiom rather than shadcn's actual Card, which uses a tighter radius and a hairline ring in place of the shadow. Two separate default sources feed the same tell and models emit both. Either way they are stock values, trivially recognizable to anyone who has read the docs.)
- **Radius is a scale, not a setting.** `rounded-2xl`/`rounded-3xl` on cards, buttons, inputs, images, badges, and avatars at one uniform value (commonly 16px) flattens hierarchy — a radius that says "soft, friendly" on a card says nothing when it's also on the input, the image, and the tooltip. Build steps tied to meaning (e.g. 2px inputs / 6px cards / 999px pills), or try removing radius entirely: sharp corners are an instant differentiator precisely because soft is the default. Match the temperament — brutalist and editorial want sharp, consumer and playful want soft.
- **Escalate separation, stop at the first step that works** — starting with whether the thing needs a container at all. Boxing is the reflex default: content gets wrapped because a wrapper was available, not because anything needed dividing, and a page of nested panels reads as assembled rather than composed. Then: (1) whitespace — usually sufficient; (2) a background shift of 3–5% against the page; (3) soft elevation; (4) a border. Most surfaces need step 1 or 2. Every card getting a 1px gray border _and_ a soft shadow is separation solved with the most literal tool available; it produces visual noise and a "dashboard component gallery" feel. Same for the colored 3–4px left-border strip and cards nested inside cards.
- **No floating social-proof badges** — small blurred, glowing pills near the hero at jaunty angles with a drop shadow ("★★★★★ 4.9 from 2,000+ teams", "Backed by…", "#1 Product of the Day"). They are decorative furniture that appears whether or not the proof exists, arranged ornamentally rather than informationally. Include social proof only when it's real, and present it as information.

## Effects

- **No gradient text on headlines.** `background-clip: text` with a purple/blue gradient across the H1, sometimes with an added blur glow behind it. It appears unprompted, on every project, regardless of brand, and it usually hurts legibility and contrast. Solid color at the right weight and size is stronger. Use it only when specifically requested or genuinely part of an established brand system.
- **No unprompted neon glow** — outer glows on buttons, glowing card borders, cyan/violet neon on dark backgrounds, radial glow blooms behind hero content. Nobody asked for it; it's generic "make it look premium/futuristic" seasoning with no relationship to the subject matter. Start from zero glow and add back only what serves a purpose, such as a focus state or one genuine emphasis.
- **Glassmorphism and bento grids are fine when deliberate.** They read as AI only when applied uniformly and without cause — frosted glass on everything including elements with nothing behind them to blur, or a bento grid whose cell sizes don't correspond to content importance. For a bento grid specifically, cell size must encode importance; if the sizes are arbitrary it's just a grid with extra steps.
- **Texture is a decision like every other one here.** Geometric patterns, layered transparency, decorative rules and borders, treated photography, and shadow used as a deliberate device rather than as default elevation all build atmosphere where the direction calls for it — and a flat surface is a perfectly good answer where it doesn't. Grain, noise, and gradient mesh belong on that list too, but they are also the second-order defaults described below, so reach for them because this particular design calls for them and not to add texture in general.
- **Dark mode is a decision, not a reflex.** Dark-by-default with no light mode, chosen without being asked, is the corpus's "sophisticated" default — and it frequently ships broken, with thin text failing contrast and colors picked for light backgrounds simply inverted. Ship dark when the context earns it (developer tools, media, night use), design it as its own system, and check contrast against the values you actually chose — the WCAG 2 ratio formula under-reports on dark backgrounds, so text that passes comfortably can still read as thin and glaring, and weight it up rather than down. A design that must render in a viewer-controlled theme, such as an artifact, is not a choice between the two at all — style it for **both**.

## Icons & imagery

- **Never emoji as icons.** 🚀 ⚡ 🎯 ✨ 🔒 as feature-card icons, section markers, or bullet points. They're text tokens — free for a model to emit, no asset pipeline, no import — which is exactly why they show up. They render differently per platform, don't inherit brand color, can't be sized precisely, and read as informal in contexts that aren't. A rocket next to "Fast deployment" is the visual equivalent of a filler word. Use a real icon set styled to the system's stroke weight and color, or no icons at all — a well-set feature list often doesn't need them.
- **Apply the swap test to every icon.** If it could be exchanged for another without changing the meaning — a shield, a zap, and a gear that are interchangeable between features — it is decoration, not information. Cut it.
- **Don't ship a default icon set at default settings.** Lucide at default stroke and size, oversized and centered above card text, arrives with the shadcn scaffold rather than being chosen. Adjust stroke weight and size to fit the type it sits beside — an icon whose stroke is heavier than the text next to it reads as a sticker.
- **Pick the set for a property, not for having heard of it.** Sets differ in ways that matter once you look: **Phosphor** carries six weights from thin to filled, so icon weight can be matched to type weight rather than accepted; **Material Symbols** exposes weight, fill, grade and optical size as variable axes, making it the most tunable if its geometry suits the work; **Radix Icons** are drawn on a 15px grid for dense interfaces, where 24px sets look clumsy; **Tabler** and **Iconoir** cover breadth and a more distinctive line respectively. Any of them beats the scaffold default, because any of them was chosen. **Drawing your own is a bigger job than it looks** — consistent optical weight, alignment, and corner treatment across a set is most of what an icon designer does — so hand-draw only the one or two marks that are genuinely specific to this product, and take the rest from a set.
- **Avoid the two default hero images**: (a) diverse groups of people looking at laptops in impossibly well-lit offices, and (b) abstract 3D blobs, gradient orbs, and floating glass shapes in space. Both are content-free and occupy the position where a product screenshot, a diagram, or a real photograph belongs. **Prefer evidence over filler**: a screenshot of the real interface, a diagram of how the thing works, a photograph of the actual object. Where the product doesn't exist yet, isn't visual, or is genuinely an idea rather than a screen, a deliberately conceptual image is evidence of the idea and the abstract render is still filler — the distinction is whether it carries information about this specific thing. If there's nothing to show, show nothing; a strong typographic hero beats filler.
- **Process any generated imagery.** The crude giveaways (malformed hands, garbled background text) are largely fixed; the current tell is _tonal_ — uncanny smoothness, a plastic sheen, consistent lighting with no source, the absence of any imperfection. If using it, treat it as a deliberate style choice: add grain, crop unconventionally, push the color, break the symmetry. Untreated model output is the tell.

## Behavior & interaction

- **Motion comes in three registers. Name which one you're in before writing it.**
  - **Informational** — what changed, where it came from, what state something is in. A drawer sliding from the edge it belongs to, a row collapsing into the place it went, a value counting to its new number. Always earns its place; this is the register an operational interface should mostly stay in.
  - **Expressive** — the motion _is_ the experience: parallax depth, scroll-driven scenes, typography that assembles, hover choreography, a transition that makes two pages feel like one surface. It carries no information and it is not decoration either. It is legitimate whenever the direction is expressive, and on an argue-kind page it is frequently the thing people remember. It has to be _built_ rather than sprinkled — see below.
  - **Reflex** — the identical fade-up on every section, card, and heading at the same duration and easing, because sections are supposed to fade up. Carries nothing, delays content, and reads as a template.
- **The deletion test sorts them.** Take the animation out and look at what's left: informational motion leaves a gap in meaning, expressive motion leaves the page without the thing it was for, and reflex motion leaves no gap at all — so it stays deleted. **If you can't say which register something is in, it's reflex.**
- **Everything non-essential goes inside `@media (prefers-reduced-motion: reduce)`**, cut to a near-instant fade or nothing. The page has to be complete and fully usable with motion off — never gate content behind a scroll reveal, since a reader who has motion disabled, a crawler, and anyone who lands mid-page all need the text to be simply present.
- **Design every state a component actually has: rest, hover, focus, active, disabled, loading, empty, error.** Applies to anything interactive or stateful, which is the part that gets skipped — not to a static heading, a decorative image, or a paragraph, none of which have most of these and none of which should be given them. Go through the list per component and design the ones that exist. They are the least-represented things in training data, because tutorials and template screenshots show the resting state only. Their absence is the "polished but hollow" signature — the page looks finished in a screenshot and falls apart the moment it's touched. It's one of the most reliable tells precisely because it's the hardest to fake, and it's where the difference between generated and designed is most visible.
- **Loading is the state skipped most often and noticed fastest when missing.** Every async action needs a pending state on _the control that triggered it_ — a button that sits inert while a spinner appears somewhere else reads as broken, and the user clicks again. Concretely:
  - **Disable the trigger while in flight and change its label** ("Save" → "Saving…"), so the same action can't be fired twice.
  - **Match the indicator to what you know.** Skeletons for content whose shape is known in advance (lists, cards, text blocks); an inline spinner for short indeterminate actions; a real progress indicator only when progress is actually measurable. A skeleton must match the dimensions and rhythm of the content it stands in for — generic shimmering gray boxes are their own tell, a mismatched one just relocates the layout jump, and the shimmer itself is motion subject to the reduced-motion rule.
  - **Don't flash.** Delay showing a loader by roughly 200ms so fast responses never flicker one on and off, and once it's shown, hold it briefly instead of cutting it the instant data lands.
  - **Announce it.** Set `aria-busy` on the region being updated and route status changes through an `aria-live` region — a purely visual spinner tells a screen-reader user nothing.
- **Empty is the state most often written as a dead end.** "No projects yet" centred in gray reports a fact and leaves the user to work out the move — and indecision at that moment is where people leave. The same blank screen has four unrelated causes, and they need different screens:
  - **Never had data** — onboarding in disguise. Say what would be here, and give the one action that creates the first item.
  - **Filtered to nothing** — the data exists and the query hid it. Show the active filter and a visible way to clear it.
  - **Failed to load** — an error wearing an empty state's clothes, and the most damaging of the four, since the user reads a broken request as a real absence. Say it failed, and offer a retry.
  - **Cleared everything** — the earned empty, and the opposite of the first: nothing is missing, the user finished. Acknowledge it rather than rendering completion as absence. Motion is a fair way to mark the moment, and this is the rare case that survives the deletion test above — check it by turning motion off, since the screen still has to read as _finished_ rather than _broken_ with no animation at all. Once, at a genuine completion; a flourish on every empty collection is decoration in a friendlier costume.
- **Destructive actions need more than a red button.** Anything that deletes a record, cancels an order, or changes someone else's access — admin tools most of all, but a settings screen and an account page too. Prefer undo where the action can be reversed: a brief window with a clear affordance beats a modal nobody reads. Where it genuinely can't be undone, make confirmation cost something proportionate — typing the resource name, not clicking "Confirm" — and state what is actually in scope ("deletes 1,204 records and 3 API keys"). Never let the destructive control be the visually dominant one in its row.
- Ease transitions at 150–250ms with non-linear easing. Buttons should never snap between states, and hover feedback should be more than a color swap. Prefer CSS-only motion in plain HTML. In React, use whatever animation library the project already has; where there is none, CSS still covers most of what's described here, and Motion is the one to reach for when orchestration genuinely needs a library — that's a new dependency, so confirm it first.

### Expressive motion and scroll

For argue-kind pages, portfolios, launches, and anything whose job includes being remembered. Skip the whole subsection for operational and transactional screens — an admin table with a parallax header is a worse admin table.

- **Claimed motion has to be shipped motion, and stillness has to be chosen.** A page that argues and never visibly moves has usually not exercised restraint, it has just avoided the work — and because every rule above pushes toward deleting motion, that is the easy place to land. Decide it explicitly. The floor for an expressive page is three things actually working: something resolves on the first screen without the user doing anything, one signature moment they could describe to someone afterwards, and interaction feedback that is more than a color swap. If the scope genuinely won't fit them, ship it still on purpose and say so at handoff. What you must not do is ship the half-built version — a reveal that never fires, a pinned section that releases early, a scrubbed scene that lands on the wrong frame — because that reads as broken rather than as restrained, and a visibly broken effect costs more than the effect ever earned.
- **Build one signature moment, and let everything else support it.** The difference between an award-site and a Webflow template is not the quantity of animation, it's that one thing was genuinely built and the rest was left alone. A hero that assembles from its parts, a scroll sequence where the product turns as you descend, type that sets itself line by line, a transition that makes two pages feel like one surface. Pick it, give it disproportionate effort, and keep the rest of the page quiet enough that it reads as the point rather than as more of the same.
- **Scroll-driven, never scroll-hijacked.** Tie animation to scroll _position_ while leaving scrolling itself alone. Taking over the wheel, easing the scrollbar, snapping the viewport between full-screen panels, or making a page wait while a scene plays are the reliable way to make expressive motion hated rather than admired — the user loses the one control they had.
- **Decide first whether the effect is discrete or continuous — they need different mechanisms, and using the wrong one is the usual reason a scroll effect "doesn't work".** Discrete means a threshold was crossed and something changes once: a section reveals, a header condenses, a counter starts. That is `IntersectionObserver`, which fires on crossings and nothing else. Continuous means the effect is a _function of scroll position_ — a scrubbed scene, parallax, a progress bar, anything that must run backwards exactly when the user scrolls back up. Observers cannot express that, and faking it with more and more thresholds gets erratic at speed.
- **Prefer CSS scroll-driven animation for both**: `animation-timeline: view()` for enter and exit tied to an element's own visibility, `scroll()` for progress along a container. It runs off the main thread and needs no library. Where you need a JS fallback for continuous work, compute progress from one `getBoundingClientRect()` per frame inside `requestAnimationFrame`, on a `{passive:true}` listener, and write it to a custom property the CSS reads. What you should not write is a `scroll` handler doing layout reads and style writes for every element every frame — that's the source of most janky parallax.
- **Reach for a library when the orchestration outgrows the primitives, not by default.** Long timelines with overlapping sequencing, pinning that has to compensate layout and survive resize, velocity or inertia in the scrub, or splitting text into per-character targets are all genuinely hard by hand — **GSAP with ScrollTrigger** is the standard answer and handles pin spacing and refresh correctly, which hand-rolled sticky scenes routinely get wrong. **Motion** covers component-level transitions and layout animation, in React or vanilla, and its `layout` prop handles reflow between two states, which is impractical by hand. **Anime.js** is the one to know for standalone HTML with no framework and no build step, and specifically for SVG: shape morphing, line drawing, and motion paths are things CSS cannot express at all and GSAP puts behind a paid plugin. **Lenis** smooths scrolling itself, and deserves more suspicion than the others: it replaces the one behaviour every user already knows, so use it only where the design genuinely depends on it. **Three.js** (React Three Fiber in React) when the concept actually needs 3D rather than wanting depth. Each is a dependency and a payload, so confirm before adding one — and none of them makes motion good. The orchestration does; a library just makes the good version reachable.
- **Parallax is differential `translate3d`, and nothing else.** Never animate `background-position`, `top`, or anything else that forces layout. Move background layers further than foreground ones, keep the delta small on anything containing text, and never parallax an element that holds a focus target or a tap target — it will move out from under the pointer. Disable it on touch, where it fights momentum scrolling, and under reduced motion.
- **Orchestrate rather than uniform-ify.** Stagger derived from position in the group, duration varying with distance travelled, easing curves you actually chose — overshoot for something arriving, sharp deceleration for something settling. The same 600ms ease-out applied to everything is reflex motion wearing expressive clothes.
- **Two or three real moments per page, maximum.** Motion competes with itself: five impressive things sequentially is five things nobody remembers. Everywhere between them, motion should be informational or absent.
- **Stay on the compositor and check it on a mid-range phone.** `transform` and `opacity` only, `will-change` sparingly and removed once idle, no layout reads inside animation frames. A signature moment that runs at 30fps on the device most visitors hold is worse than not building it.
- **`prefers-reduced-motion` needs a designed answer, not an off switch.** Cutting straight to the final state is right for reveals; for a scroll sequence whose content only exists across frames, the reduced answer is the sequence's endpoint plus whatever text conveyed the point. Look at that version too — it is what a real share of people will see.

### Forms

A form is almost entirely states, which makes it the purest case of screenshot bias: it screenshots perfectly at rest — a stack of well-spaced inputs and a styled button — and everything that makes it usable happens after the first keystroke.

- **The label stays visible, and it carries more than the field's name.** Placeholder-as-label is the standard failure: the text vanishes the moment anyone types, so the field is unlabelled precisely while it's being filled, and it degrades screen readers and autofill on the way out. Keep a real `<label>`. Where most fields are required, mark the **optional** ones rather than asterisking everything else. Let width hint at the expected input, too — a postcode box as wide as an address box tells the user nothing about what fits.
- **Validate on blur, not on keystroke.** An email address is invalid right up until it isn't, so flagging it mid-word is scolding someone for a sentence they haven't finished. Wait until they leave the field. Once a field _has_ errored, switching that one field to live validation is right, because now the user needs to see the moment it clears.
- **Errors sit next to the field, in words, and say how to fix it.** A red border plus a summary at the top of the page makes the user hunt for the thing they already know is wrong. "Invalid input" says nothing; "Password needs at least one number" says what to do. And never color alone: a red outline with no message is a field that failed silently for anyone who can't see the red.
- **One column.** Side-by-side fields break the vertical scan and double the number of places the eye has to land. The exception is genuinely paired data that reads as a single line: city and postcode, expiry and CVC.
- **A long form is a sequence, not a wall.** Twenty fields on one screen get read as work before they get read as fields, and the drop-off happens at the scroll bar rather than at any particular question. Break it into steps grouped by what the user is thinking about — contact, then shipping, then payment — and show where they are and how much is left. Two caveats: don't split a form that isn't long, since three steps of four fields is more friction than twelve fields on one screen; and every step has to keep its values when the user goes back, for the same reason a failed submit must never wipe them.
- **Submitting must resolve, and must not destroy anything.** Silence after submit reads as broken and gets clicked again, so success needs a state of its own rather than a quiet redirect. A rejected submit that clears the fields is the most punishing thing a form can do — keep every value exactly as typed. (The pending state on the button itself is covered by the loading bullet above.)

### Modals and overlays

- **First ask whether it needs to be a modal.** Reaching for one whenever content doesn't fit the current screen is the same reflex as boxing: a wrapper used because it was available. Modals interrupt, can't be linked to, break the back button, and are the worst available form factor on a phone — and a modal that opens another modal is a flow that needed a page. Consider a page, an inline expansion, or a drawer before defaulting to one.
- **Focus is the whole accessibility story here.** On open, move focus into the dialog; while it's open, keep focus inside it; on close, return focus to the element that opened it. Skip this and a keyboard user tabs straight into the page behind an opaque overlay — that content is still present and still focusable, just invisible to them. `<dialog>` with `showModal()` gives you the focus trap, Escape, the backdrop, and inertness of the rest of the page for free; hand-rolling means `role="dialog"`, `aria-modal="true"`, a label, and writing the trap yourself.
- **Escape always closes it. Click-outside does not.** Escape is unconditional. Dismissing on a backdrop click is right for a lightbox or a preview and wrong for anything holding entered data — losing a half-filled dialog by clicking a few pixels off its edge is the never-wipe rule broken by a different route. Confirm or refuse to close; don't discard silently.
- **Lock the page behind it, and expect two bugs.** Without a scroll lock the page scrolls behind the overlay. With a naive one, the layout shifts as the scrollbar disappears — compensate with padding — and iOS ignores `overflow: hidden` on `body`, so it needs its own handling.

## Copy & content

**A site expresses as much through its words as through its design.** The words are also the only part that can say something _specific_ — a layout can feel precise, but only a sentence can make a claim someone could check. So write the copy on the same pass as the design, from the same direction, rather than pouring text into finished boxes.

What good copy does here: it says something only this product could say; it takes a position the reader could disagree with; it names things precisely, because one exact noun outperforms three adjectives; and it varies sentence length on purpose — rhythm is to prose what spacing is to layout, and uniform sentence length reads as flat for exactly the reason uniform padding does. Saying the hard part out loud — the limit, the price, the thing it doesn't do — is the most reliable signal available that someone who knows the product wrote this.

Copy is also where a model is most easily caught, because language models leave more distinctive traces in prose than in CSS.

**Which of this applies where.** The vocabulary and register rules — banned openers, LLM filler, negation pivots, fabricated content — are universal, and hold in a button label, a tooltip, and an error message exactly as they do in a headline. The headline, feature-title, and social-proof material is written for pages that argue. In an operational interface the copy carrying the weight is smaller and lives elsewhere in this file: field labels and validation messages under Forms, empty-state wording and the text on a destructive confirmation under Behavior & interaction. Nothing below licenses a dashboard to grow a hero headline.

- **Headlines need weight.** "Build the future of work." / "Scale without limits." / "Your all-in-one platform." / "Build faster. Ship smarter." are grammatically perfect and semantically empty — the _average_ of every SaaS headline, so they describe no product in particular. **The test: if the headline could sit unchanged on a competitor's site, it says nothing.** Require at least one specific, checkable claim in the hero, ideally with a number. The work in a strong headline is done by a specific noun that claims a category — "financial infrastructure" — not by the aspiration attached to it.
- **Ban the opener verbs**: _Empower, Unlock, Transform, Elevate, Revolutionize, Supercharge._
- **Ban the LLM vocabulary**: _seamless, robust, leverage, delve, underscore, pivotal, cutting-edge, best-in-class, game-changing, tailored, holistic, comprehensive._
- **No negation pivots**: "It's not about X. It's about Y." / "It's not just X — it's Y." / "Most teams don't X. They Y." This is the most-flagged AI copy pattern, above em dashes. It manufactures profundity through rhetorical antithesis without adding information, and the X is usually a strawman nobody claimed. State Y directly; keep the contrast only if it clarifies something the reader would genuinely otherwise misunderstand, once per page maximum.
- **No landscaping openers**: "In today's fast-paced digital landscape…" / "In the dynamic world of…" / "In this rapidly evolving environment…" The most recognizable phrase family in AI prose, and pure throat-clearing. Delete the opening clause — the sentence almost always works better starting at the verb.
- **No reflexive threes.** "Fast. Simple. Secure." plus three feature cards plus three pricing tiers plus three benefit bullets. The rule of three is a real rhetorical device; the tell is choosing three by rhythm rather than by content. This is the same impulse that produces the three-card layout. Use two, or five. Break the rhythm deliberately.
- **Rewrite two-noun feature titles as sentences that say what the thing does.** "Seamless Integration" / "Robust Security" / "Intelligent Automation" name nothing.
- **Avoid rhetorical authority and motivational closes**: "The reality is…" / "The truth is…" / "The key is…" asserting universal truths without evidence, and "The question isn't whether X will happen. It's whether you're ready." Yellow flags individually, damning in a cluster.
- **Em dashes are not the tell — density is.** Skilled human writers use them constantly. The tell is three or four unspaced em dashes per paragraph, wedged between clauses that wanted commas or periods: the dash as rhythmic crutch. Never treat em dashes alone as evidence of AI authorship; it's the most over-claimed signal in circulation.
- **Do not fabricate content.** Fabricated testimonials with generated avatars, "Trusted by" clouds of placeholder logos, round-number stats with no source ("10,000+ happy customers"), lorem ipsum surviving into production, team pages with generated headshots. These exist because the template had a slot for them, so they get filled with plausible fiction rather than removed — and users notice. **Cut every section that can't be filled with something real.** An honest page with four sections beats a template with twelve. Where placeholders are genuinely needed, make them obviously placeholder and flag them in the handoff.

  > **This one is not only a taste problem.** In the US, the FTC's Rule on the Use of Consumer Reviews and Testimonials (effective 21 October 2024) explicitly bans fake and **AI-generated** reviews and testimonials, including any that misrepresent the reviewer's identity, experience, or existence. It carries substantial per-violation civil penalties, adjusted annually. Placeholder testimonials are for mockups; shipping them is legal exposure.

## Functional & code-level tells

These are what a developer sees, and they're often more damning than the visuals.

- **Polish/depth mismatch.** A beautifully finished marketing surface attached to a product whose actual functions don't work intuitively — immaculate hero, broken flow. Aesthetics are heavily represented in training data and usability is not, so models optimize what they can see. This asymmetry is one of the most reliable signals available, and the only defence against it is exercising the interface rather than looking at it — see the operate step in Verification.
- **Missing form and accessibility fundamentals.** Everything in the Forms section above, plus every item in the Verification accessibility checks below. Same cause: it lives in code that screenshots never show. Treat it as part of the definition of done, not a follow-up pass.
- **Explicit artifacts.** Comments left in the source labeling generated sections, unedited placeholder metadata, meta tags with odd phrasing, duplicated utility class strings that reveal copy-paste generation. Strip these before handing off.
- **The maximum-likelihood stack** — React + Next.js + Tailwind + shadcn/ui + lucide-react for a five-page brochure site. Nuance: this is a legitimate and popular choice, and its presence alone proves nothing. It's corroborating evidence, not a fingerprint. Don't reject it reflexively; just don't reach for it by default when the project doesn't need it.

## The second-order trap: the "tasteful default"

There is a second-generation AI aesthetic, and it is the most likely place to land while trying to escape the first: cream and off-white backgrounds, a serif display face, sage/olive/terracotta accents, generous whitespace, subtle grain texture, editorial layout, muted photography. Adjacent variants are "code brutalism" (monospace, high-contrast monochrome, terminal energy) and "imperfect by design" (visible grain, friction, nostalgia).

It exists because it is the _correction_ — a deliberate rejection of glossy purple polish. And because it is now the well-known correction, it has itself become a template. Cream + serif + sage is trading one template for another.

**There is no safe aesthetic.** Any aesthetic adopted _because it isn't the AI one_ is still a default, just a more recent one. The problem was never purple; it was choosing without a reason. A cream-and-serif page picked for no reason is exactly as generic as a purple one, and increasingly as recognizable.

So the derivability test applies to the correction as much as to what it corrects. Practically: if the palette and pairing arrived because they are the tasteful ones rather than because this subject produced them, they are a default. Within a session, that is checkable — do not clone the palette, pairing, or layout you produced an hour ago onto an unrelated brief just because it worked. Reaching for the same warm-neutral-and-serif answer every time is not consistency, it is the second-generation template with a personal accent.

## Anti-default audit

Run this on the result; it is not a brief. Nothing in it will produce a direction — it only detects choices that never had one, which is why it comes last and why designing _to_ it produces its own recognizable style: asymmetry because symmetry is listed, five cards because three is listed, an unusual typeface for no reason but that the usual ones are named. That is still choosing without a reason.

So each hit is a question, not a failure — ask what the choice traces back to. But the audit runs after the work exists, which makes reasons cheap: a justification invented while auditing reads exactly like one that drove the decision. Two things separate them. A real reason was **already in the chain you wrote down before building**, and it points back at the subject; a rationalization arrives now, and points at the artifact — "three reads cleanly," "it felt balanced," "the grid wanted it." **A hit that traces to the chain is not a hit** — cross it off and put the trace in the handoff. Everything else counts, including the hits you can argue with. Of those: one or two are worth fixing individually; three or more clustered usually means there is no direction for them to trace back to, and then the fix is the direction rather than the items.

**Color** — purple/indigo→blue gradient anywhere · pure `#fff` or `#000` backgrounds · accent unrelated to the brand or subject · extra hues in play that aren't doing semantic or functional work

**Type** — Inter/Roboto/Poppins/Geist at default settings · single typeface with bold as the only hierarchy tool · serif-italic accent word in the headline · all-caps letterspaced labels above more than one section in three

**Layout** — centered hero with a pill badge above the H1 · exactly three evenly-weighted feature cards · the full stock skeleton in stock order · identical padding everywhere; fails the squint test

**Components** — `rounded-2xl shadow-lg p-6` untouched · one uniform radius on every element · border _and_ shadow on every card · floating glowing social-proof badges

**Effects** — gradient text on the headline · unprompted neon glow · dark mode by reflex rather than by decision

**Imagery** — emoji as icons · default-styled icons that fail the swap test · abstract 3D blobs or laptop-in-a-bright-office stock · untreated AI illustration with a plastic sheen

**Motion** — the same fade-up on every element · buttons snap between states · hover feedback that is only a color swap · animation that carries nothing and survives only because nobody applied the deletion test · a page that argues and never moves at all, which is the same omission from the other end

**Copy** — headline works unchanged on a competitor's site · "It's not X — it's Y" · reflexive threes · "In today's [x] landscape" · seamless/robust/leverage/unlock/empower/elevate · two-noun feature titles · zero specific or checkable claims · placeholder testimonials, logos, or stats still present

Functional defects are not on this list — broken keyboard navigation is not a matter of taste and does not belong in a rubric where it can be outvoted by a typeface. They are pass/fail, and they live in Verification.

---

## Design Responsiveness

**Derive breakpoints from the content, not from device names.** Widen the window until the layout stops working, and put a breakpoint where it broke. Naming breakpoints after phones and tablets bakes in a device landscape that changes every year, and it leaves the awkward in-between widths untested — 600px, 900px, and 1100px are where layouts actually fall apart, not at the round numbers everyone checks.

- **Mobile is not the desktop layout scaled down.** A narrow viewport changes what matters, not just what fits: order shifts, secondary content collapses or moves below, multi-column becomes single-column in a deliberate reading order — check what `flex-wrap` and grid auto-placement actually do to the sequence, since the DOM order they fall back to is rarely the order you want. Hiding the difficult part with `display: none` is the failure mode; if something doesn't fit, it needs a different form, not an exit.
- **The type scale has to respond too.** A 72px display headline is not a 72px display headline at 375px wide. Scale display type, section padding, and grid gaps across breakpoints — `clamp()` expresses this in one declaration — and re-check measure at each one, since 60–75 characters is still the target when the column narrows.
- **Anything hover-only does not exist on touch.** Tooltips, hover-revealed actions, and hover-triggered menus have no equivalent for a finger. Either the information gets a persistent home or the interaction gets a tap path. Gate hover styling behind `@media (hover: hover)` so touch devices don't inherit stuck hover states after a tap.
- **Question the hamburger.** Collapsing navigation into an icon is the reflex, and on desktop it hides the site's structure to buy space that isn't needed. Even on mobile it costs a tap before anyone can see where they are. Keep two or three primary destinations visible wherever the width allows. If there are too many destinations to show any of them, the problem is the navigation's breadth rather than the viewport's — group them under a few top-level entries with the depth browsable or filterable underneath, instead of listing everything and then hiding the list behind an icon.
- **`100vh` is wrong on mobile.** It measures the viewport without browser chrome, so full-height sections sit partly under the URL bar. Use `100dvh` for anything meant to fill the screen, with a `vh` fallback for older engines.
- **Use container queries when a component's width isn't the viewport's.** The same card in a sidebar and in a main column needs different internal layouts, and `@container` responds to the space the component is actually in — which is the thing the component actually cares about.

### Images: getting `sizes` right

Applies whenever the build uses `srcset`. An under-declared `sizes` hint makes the browser fetch a file narrower than the element actually renders and upscale it — soft, blurry images on large or high-DPR displays, invisible in a screenshot taken at 1×, and easy to miss by eye. It is a visible design failure with a plumbing cause, which is why it's here.

`sizes` declares **how wide the image will render**, so the browser can choose a file before layout has happened. Two consequences of that do most of the damage:

- **It is evaluated before layout**, so it knows nothing about containers, grids, or flex. Every px hint is a hardcoded duplicate of a layout fact and goes stale the moment the layout changes — re-declare it at each breakpoint that changes the container's real width, and leave a comment tying the two together. Prefer `vw` wherever the image genuinely is viewport-proportional; that version is self-correcting and needs no maintenance.
- **Font-relative units resolve against the initial 16px**, not your actual root, so `rem` inside `sizes` silently lies in any project that scales the root font-size. The classic case: rem-based containers widen on large displays while the px hints stay put, and the browser keeps serving the laptop-sized file.

Under-declaring costs sharpness and over-declaring costs bytes, so round up when unsure — a soft image is more noticeable than a slightly larger download. Then **verify on the wire, not by eye**: with a browser automation tool available, evaluate in the page and flag anything where `served < rendered * dpr`.

```js
[...document.images].map((i) => ({
  src: i.currentSrc,
  served: i.naturalWidth,
  rendered: i.getBoundingClientRect().width,
  dpr: devicePixelRatio,
}));
```

Without one, hand the check to the user: DevTools → Network → Img, comparing the served width against the element's rendered width.

## Redesign procedure

"Redesign" spans everything from a tune-up to a replacement, and picking the wrong end of that range is the characteristic failure — arriving with a whole new aesthetic when the page needed its hierarchy fixed, or repainting a page whose problem was structural.

- **Audit first, then decide the range.** Run the anti-default audit against the current page. Hits that trace back to a reason mean the page has a direction and the job is _within_ it. Hits with nothing behind them, three or more clustered, mean there is no direction to work within, and that is the case where replacing it is the right call rather than the ambitious one.

- **Sort what's there into four piles, explicitly.** _Preserve_ — what works, what users recognize, what the brand owns. _Remove_ — what is decoration, duplication, or a default nobody chose. _Reframe_ — right content, wrong hierarchy, weight, or order; this pile is usually the largest and delivers most of the improvement. _Rebuild_ — genuinely broken, and the only pile that needs new primitives. Say which pile each major element landed in when you hand off; that list _is_ the plan.

- **Re-derive the direction only if the inputs changed.** Purpose, kind, tone, constraints, and differentiation from Design Thinking — check each against what the user is now asking for. If they haven't changed, the existing direction stands and this is an execution job. If they have, derive the new one properly rather than substituting a fashionable aesthetic for the old fashionable aesthetic.

## Verification

Do not hand off a design you have not actually looked at. What that costs scales with the change, in three tiers:

- **Core — every handoff, down to a one-line CSS change.** What you touched is still keyboard-reachable with a visible focus ring; its contrast still passes; nothing you added is fabricated content; and you introduced no horizontal scroll. Four checks, seconds to run, no exceptions — a gate that gets skipped as disproportionate teaches that the rest of this file is optional too.
- **Page-level — anything that changes layout, adds a component, or touches a whole screen.** Everything below.
- **Full build — a page or app designed from scratch.** Everything below, ending with the self-check against the brief.

### The checks

- **Render it.** If a browser automation tool is available (Chrome DevTools MCP, Playwright, Puppeteer), load the page and screenshot it at roughly 375px, 768px, and 1440px wide, then inspect the screenshots. Where none is available — artifacts and most sandboxed contexts, which is the common case rather than the edge one — say so plainly in the handoff and name what it leaves unverified. **The disclaimer is not the check.** It covers what you genuinely cannot see; it does not cover what you can still read in your own code: heading order, focus handling, contrast between values you chose yourself, the states you did or didn't write.

- **Operate it.** A screenshot only ever proves the resting state. Click the buttons, tab through the whole page, submit the form empty, open and close every overlay while watching where focus lands, watch what a slow action does, and resize mid-interaction. This is where the polish/depth mismatch shows up, and nothing else in this list catches it.

- **Layout**: No horizontal scroll on the body at any width. Nothing overlaps or clips unintentionally. Text stays readable at the smallest breakpoint. Wide content — tables, code blocks, diagrams — scrolls inside its own container instead of pushing the page.

- **Accessibility**: Semantic HTML with a sensible heading order. Contrast of at least 4.5:1 for body text and 3:1 for large text and UI boundaries. Every interactive element reachable by keyboard with a visible focus ring — never `outline: none` without a replacement. Touch targets of 44×44 CSS px (24×24 is the absolute floor). Alt text on meaningful images, and `aria-hidden` on decorative ones. Any graphic carrying data — a chart, a timeline, a comparison grid, anything assembled from bare `<div>`s — needs its finding available as text, since a screen reader gets nothing from shaded boxes; the shortest fix is usually a sentence stating the conclusion, in an `aria-live` region if it changes.

- **Function**: Pass/fail, not a matter of taste. Forms validate and show errors where the error is. No field uses placeholder text as its label. A failed submit keeps every value typed. Focus is always visible and keyboard navigation reaches everything. An open modal cannot be tabbed out of. Async actions show pending state on the control that triggered them. And the functional depth matches the visual polish — a finished-looking surface over a flow that doesn't work is the most damning single outcome here.

- **Buttons and calls to action**: three checks that read as fine in isolation and are caught by looking, not by taste.
  - **Label contrast against its own background.** Check each button against the surface it actually sits on, including ghost and outline buttons over photographs or gradients, where the label passes over one part of the image and vanishes over another. A scrim, a solid fill, or a stroke fixes it.
  - **No CTA label wraps at desktop.** A primary action broken across two lines is a broken control. Shorten the label to two or three words rather than widening the button, and never constrain a CTA's width to force the wrap.
  - **One label per intent, everywhere on the page.** "Get in touch" in the nav, "Let's talk" in the hero, and "Start a project" in the footer are one action wearing three names, which makes a page read as assembled from parts. Pick the wording once and repeat it exactly — repetition is the point, not a lack of imagination.

- **Performance**: Sized and optimized images, no layout shift on load, no animation of properties that force layout — prefer `transform` and `opacity`.

- **Content**: Nothing fabricated ships. No invented testimonials, reviews, logos, or statistics, and anything standing in for real content is obviously placeholder and named as such in the handoff. This is the one item here with legal exposure attached rather than only a quality cost — see the FTC note above.

- **Self-check against the brief**: Before handing off, run the anti-default audit above and make sure every hit it returns has an answer you can state, that the design still expresses the direction you committed to at the start, and that each major choice traces back to a reason specific to this project.

**ALWAYS** hand off the finished design to the user for review and feedback. State the direction you chose, what drove it, any placeholder content, and anything you could not verify. Iterate based on their input.
