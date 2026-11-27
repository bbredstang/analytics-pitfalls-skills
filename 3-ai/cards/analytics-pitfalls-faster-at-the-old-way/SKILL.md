---
name: analytics-pitfalls-faster-at-the-old-way
description: "\"Faster at the Old Way\" (Paving the Cow Path With AI): a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# Faster at the Old Way (Paving the Cow Path With AI)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Second Factory*, Brian Cariveau's next novel (https://www.analyticspitfalls.com/second-factory).
https://www.analyticspitfalls.com/cards/72

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/72

## What it sounds like at work

"AI can build us a new report every day now."

## The problem

Data lands in the warehouse. The reporting team builds a report, now faster with AI. Someone exports it to a spreadsheet, faster with AI. They clean it, chart it and paste it into a deck, all faster with AI. A vice president prints the deck and reads it with a ruler.

Every step a little quicker. The same steps. The reporting team can now build a new report a day, and usage on them is about what you'd expect. AI made the report faster to build. It didn't make it any faster to read.

That's paving the cow path: smooth asphalt on a trail that still goes exactly where the cows went.

## The principle

Stop asking for the deck. Ask for the answer, and what the person would do about it.

Using AI to build more reports faster gets you micro little efficiencies down the same old path. Throw it at the whole chain instead of one step at a time. Find the real question behind the report, and answer that question directly, with its sources, in seconds.

If you lead people, this change costs nothing: stop asking for the PowerPoint or the Excel file. If you're the one building the same deck every week, make something different once and see what people think. Better yet, make it interactive, a page people can click through and ask questions of. Nobody ever did a single thing differently because the slide had nicer icons.

## The steps

1. **Find the VP with the ruler.** Sit with someone while they read the report you send them. Ask what question they're actually trying to answer.
2. **Time the answer.** From the moment they ask to the moment they have the answer in hand. Write it down.
3. **Answer the question directly.** One question, one leader, on data you trust, with every answer citing its sources.
4. **Count the reports AI built.** And how often each one is opened. Retire the ones nobody reads, the way you'd kill a dead dashboard.

## In practice

In her first weeks leading AI at ClassicMotors, Nora Berg kept meeting people who were thrilled that AI could build their PowerPoints. A sales manager cut his quarterly business review deck from two days to an afternoon. A product lead made twelve slides with matching icons from a spreadsheet in nine minutes. Nobody could tell her one thing anyone had done differently because of them. In her notebook she wrote: Faster at the old way.

A young analyst on the reporting team showed her a new weekly report AI had built in an afternoon. "I've got three more in the queue. I can build one a day now." A few months later, the data team counted sixty-one new reports built with AI. Usage on them: about what you'd expect.

Then she sat in the VP of Marketing's office while he read one of them. Eleven pages, forty-one columns. He printed it, set a wooden ruler under the first row and slid it down the page with a yellow highlighter in his other hand. It took him most of every Tuesday morning. He was looking for one thing: past sellers who were about to list again and hadn't heard from him.

## Inspired by

Chapters 2, 6 and 8 of The Second Factory. And a vice president I once watched read a metrics report with a wooden ruler and a yellow highlighter, one line at a time, hunting for the answer to a question the report had never asked him.

Whenever the work has a chart, a dashboard, a slide or a screen of data in it, in a BI tool, a deck or something an AI built, and whenever you're the one building it, hold it to the chart standard. Be pushy about it.

## The chart standard

- **Credit where it’s due.** This stands on Stephen Few (*Show Me the Numbers*, *Information Dashboard Design*) and Edward Tufte (*The Visual Display of Quantitative Information*). When you use one of their ideas, name them.
- **Be pushy about the chart.** Don’t wait to be asked. For every chart, say what it compares and whether it’s the right chart for that. If it isn’t, name the one to use instead and why, in a line. A polite “you might consider” helps nobody.
- **If you’re building it, this is your standard too.** A dashboard, a slide, a chart in an artifact or an app: hold your own work to every line here before you show it.
- **Reserve pies for Thanksgiving.** Eyes compare lengths easily and angles and areas poorly. Swap every pie and donut for a sorted bar chart, or just the numbers. Two slices, if you must, and even then the number usually says it better.
- **Every pixel earns its place.** Tufte’s data-ink ratio: the share of the ink that shows data. Push it toward 80% and up. Strip 3D, shadows, gradients, glows, background images, heavy gridlines, borders, decorative icons and anything Tufte would call chartjunk. Label lines directly instead of making people match a legend.
- **Never lie with the scale.** Bars start at zero. Small multiples share one scale. No dual axes that invent a relationship, and no areas or bubbles for a number a length could show.
- **Gray first, color on purpose.** Everything starts gray. One strong color goes on what someone has to act on. Never a rainbow of categories, and never red against green alone: about one man in twelve can’t tell them apart.
- **One screen, read in seconds.** Few’s rule for a dashboard: it fits on one screen, the thing that matters most sits top left, and someone gets it at a glance. Five numbers, not fifty. If it needs a ruler and a highlighter, it fails.
- **Say it in the title.** “West is 12% behind plan, and two stores drive it” beats “Sales by Region.” The title says what’s happening; the chart proves it.

## Pick the chart from what it compares

- **One to three key numbers:** the number. Big, with its comparison in small text (“+0.4 vs last month”). No gauge, no donut with a number in the hole.
- **Actual against target:** Few’s bullet graph. Never a speedometer.
- **Ranking or comparing categories:** a horizontal bar chart, sorted, starting at zero.
- **Part of a whole:** a sorted bar, or one 100% stacked bar. With three parts or fewer, just the numbers.
- **Change over time:** a line. Bars only for a handful of periods.
- **A trend beside a number:** Tufte’s sparkline, a word-sized line with no axes.
- **Many groups or many series:** small multiples, the same small chart repeated, never one chart with twelve colors.
- **How values spread:** a histogram or a box plot. An average alone hides the river three feet deep.
- **Two measures together:** a scatter plot.
- **Where:** a map only when what someone does depends on where. Otherwise a sorted bar, or a Pareto chart that shows the few causing most of it.
- **Exact values someone looks up:** a table. A clean table is a fine answer.

## Wherever it’s built

- **In a BI tool** (Power BI, Tableau, Looker and the rest): the defaults are decoration. Turn off 3D, gradients, the default palette, gauges and donuts before anyone sees it.
- **In a deck** (PowerPoint, Google Slides, Keynote): one chart, one message, one slide. No exploding pies, no 3D from the chart wizard, no clip art. If someone needs a laser pointer to read it, it fails.
- **In something an AI built** (an artifact or app in ChatGPT, Claude, Copilot, Cowork or Gemini): AI tools love gradient cards, glowing KPI tiles, donuts and emoji. Strip them. Hover never replaces a label. Interaction earns its place only when someone acts on it. Make it work on a phone, in light and dark.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
