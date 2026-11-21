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

1. Name the card by its title and say in a sentence why it fits. Say the work could use this principle.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. If the card doesn't fit, say so plainly. Don't stretch it.
5. Finish with the card's link: https://www.analyticspitfalls.com/cards/59

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

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
