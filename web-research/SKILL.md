---
name: web-research
description: Writes a report on a topic by searching the web and collecting information from multiple sources. Use when the user asks to research a topic and create a report on it.
---

## Context evaluation - What needs to be clear before you start searching

Infer what you can from the request and ask only for what would change the report. Purpose and depth are usually inferable — "research X for a blog post" tells you both. Put any questions you do have into a single message rather than asking them one at a time:

1. **References the user already has.** Always worth asking — you cannot infer these, and they usually anchor the whole report.
2. **Specific questions the report must answer.** Ask when the topic is broad enough that two reasonable reports would look nothing alike.
3. **Hard constraints** — length, format, audience. Ask only when the request implies a deliverable with a fixed shape: a one-pager, a slide, a client email.

If none of those apply, state the scope you are assuming in one sentence and start searching. Do not spend a turn asking the user to confirm an understanding they just gave you.

## The Searching Process - How to gather information from the web

With the context established, start gathering information:

1. Use a search engine to find relevant information on the topic. Use specific keywords and phrases to narrow down the search results.
2. Evaluate each source against what would actually make it wrong:
   - **Can you reach the original?** Prefer the study, filing, or primary announcement over an article describing it — coverage drops caveats and rounds findings up.
   - **When was it published?** Check the date on every source and weigh it against how fast the topic moves. On an active topic, a two-year-old page is a claim about the past.
   - **Who benefits from the claim?** Vendor benchmarks, sponsored posts, and advocacy writing can still be right, but they need corroboration from someone without the stake.
   - **Does it show its evidence?** A source that links its data can be checked; one that asserts and cites nothing cannot. Confident formatting is not evidence.
3. Take notes on the information you find, including any relevant quotes.
4. Record every claim you might use, alongside the URL it came from. The reporting step needs those URLs, and reconstructing them afterwards is guesswork.

_Stop searching when new searches stop changing the report_ — when the results are pages you have already read, or claims you have already recorded. Before you stop, check that each claim the report leans on has a source behind it, and that the load-bearing ones appear in more than one independent place (two outlets running the same wire story count as one source, not two). If a query returns nothing new twice in a row, treat that part of the topic as exhausted and move to the next question instead of rephrasing it a fifth time.

_Say what you could not find_. If nothing credible covers the topic, say so and stop — do not pad out a report with content farms and SEO filler. If sources disagree, give both positions and who holds them rather than quietly picking one. If the best source is paywalled or years out of date, cite it and label it as such instead of inferring its contents.

## The Reporting Process - How to compile the information into a useful report

Once you have stopped searching, compile your notes into a report (the default format for the report will be a .md file, change if the user requires something different):

- Organize the information you have gathered into a logical structure. Use headings and subheadings to break up the report into sections — highlighting the most important points.
- Use clear and concise language to communicate your findings. Avoid jargon and technical terms that may be confusing to the reader.
- Cite as you write. Link each claim to its source inline at the point you make it, then list the full set of sources at the end. A claim you cannot link to a source does not go in the report.
- Carry the gaps in. Where you found nothing credible, where sources disagreed, or where the best evidence was paywalled or years out of date, say so in the place the claim would have gone. A report that reads as uniformly confident when the research was not is worse than one that is open about its thin spots.

At the end of the report, provide a summary of your findings.
