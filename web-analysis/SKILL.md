---
name: web-analysis
description: Analyzes the structure and content of a website or application. Use when the user asks to analyze a website or application (usually through a link to the website itself).
---

## Check for design patterns and colors used

Before you start, please make sure to check the website or application for any design patterns and colors used. This will help you identify the design pattern more accurately.

1. Fetch the page. Prefer a browser automation tool if one is available (Chrome DevTools MCP, Playwright, Puppeteer) — it runs the page's JavaScript and exposes computed styles, which is what the color and typography read below actually needs. Plain fetch is the fallback.
2. Check what you actually got back before analyzing it. A client-rendered site returns a near-empty shell over plain fetch, and a login wall returns the login page rather than the page you asked for. If the markup has no real content, say so and stop — do not describe a page you could not see.
3. Analyze the layout, structure, and visual elements. Look for any recurring patterns or styles that may indicate a specific design pattern.
4. Look for common design patterns such as:
   - Navigation menus
   - Buttons and forms
   - Layouts and grids
   - Typography and font styles
   - Color schemes and palettes
5. Take note of any recurring elements or styles that may indicate a specific design pattern.

## Identify important information in the website or application

Once you have analyzed the website or application design patterns and colors, you can start identifying important information. Look for the following:

- Name of the website or application and its purpose
- Key features and functionalities such as search, filtering, and sorting options
- Locations and maps showing the location of the business or service
- Contact information such as phone numbers, email addresses, and social media links or contact forms
- Opening hours and availability of the business or service or any calendar or scheduling features

## Provide a summary of the web pattern

After analyzing the website or application, provide a summary of the web pattern you have identified. Include the following information:

- The name of the website or application and its purpose
- The design pattern used and any recurring elements or styles
- The color scheme and palette used
- Any important information you have identified

Compact all of this information into a concise summary that can be easily understood by the user.

**Say how you read the page and what that left unseen.** State which method was used — rendered browser or plain fetch — and name anything it could not reach: content behind a login, sections that only load on interaction, styles you inferred from markup rather than read from computed values. A reader has no way to tell an observation from an assumption once both are in the same summary, so mark the difference rather than leaving it to be guessed.
