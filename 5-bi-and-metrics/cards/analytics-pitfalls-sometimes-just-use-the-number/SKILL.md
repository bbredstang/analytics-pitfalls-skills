---
name: analytics-pitfalls-sometimes-just-use-the-number
description: "\"Sometimes Just Use the Number\" (When a Chart Makes Things Worse): a principle card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project needs it."
license: CC-BY-4.0
---

# Sometimes Just Use the Number (When a Chart Makes Things Worse)

A principle card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/59

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work could use this principle.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/59

## The problem

Dashboard showing "Customer Satisfaction Score." It's a gauge chart. With gradients. And a needle pointing to 8.2. Looks fancy. But here's the problem: the gauge took up 20% of the dashboard space to show ONE number. And it's harder to read than just showing "8.2" in big text. Worse: comparing this month's gauge to last month's gauge requires mental math—you can't see the change easily. You built visualization theater. It looks like you're doing analysis, but actually you just made a number harder to read. Sometimes the simplest solution—just showing the actual number—is the best solution.

## The principle

Not everything needs a chart. If you're showing 1-3 numbers, especially a key metric, just show the number. Big. Bold. Add context with small text ("+0.4 vs last month"). That's it. Gauge charts, donut charts with numbers in the center, progress bars for single metrics—usually worse than just the number. The magic happens when you realize that 67% of dashboard space can often be simplified to large numbers with small context. Think manufacturing: you don't build a complex machine to measure one thing when a simple gauge works better. Same with viz—use the simplest tool that communicates clearly.

## The steps

1. **Audit Single-Metric Visualizations**

Find every chart showing ONE number:
- Gauge charts
- Donut charts with number in center
- Progress bars (just showing % complete)
- Single-bar charts
- Pie charts with 2 values

Ask: Would a large number with context be clearer?

Test: Show both versions to 3 users. Time how fast they read the value. Numbers are usually 3-5x faster.
2. **Replace with Big Numbers + Context**

For single metrics:
- Show the number large (40-60pt font)
- Add small context below:
  * Change vs last period: "+2.3 vs last month"
  * Target: "Target: 8.0"
  * Trend indicator: ↑ ↓ → arrows
  * Sparkline (tiny line chart) if showing recent trend

Example:
```
8.2
↑ +0.4 vs Nov | Target: 8.0
```

Simple. Fast. Clear.
3. **Reserve Charts for Complexity**

Use charts when they add value:
- Trends over time (line charts)
- Comparisons (bar charts)
- Distributions (histograms)
- Relationships (scatter plots)
- Geographic patterns (maps)

DON'T use charts for:
- Single numbers (just show the number)
- 2-3 categories (table or numbers work fine)
- Decoration (to "make it visual")

Rule: Chart must answer a question numbers can't. If a table or number is clearer, use that.

Bonus: Dashboards become scannable. Execs read KPIs in seconds instead of minutes.

## In practice

A healthcare analytics team had an executive dashboard with 12 KPIs. Each was a gauge chart, donut chart, or progress bar. Looked impressive. Execs complained: "Takes too long to read." Team redesigned: Each KPI became a large number with small trend indicator. "8.2 ↑ +0.4" instead of a gauge chart. Dashboard went from 12 complex visualizations to 12 simple numbers. Comprehension test: executives found and interpreted KPIs 4x faster with numbers vs charts. Space freed up was used for 2 actual trend charts showing the WHY behind changes. One exec said: "Now I spend 10 seconds reading KPIs and 2 minutes understanding trends, instead of 2 minutes decoding gauges." Simple numbers aren't boring—they're efficient. Save charts for when they actually add value (trends, comparisons, distributions). For single-point metrics? Just use the number.

## Inspired by

Stephen Few's guidance on dashboard design. Edward Tufte's principle of maximizing data density. Visual perception research showing numbers are fastest for single values.

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
