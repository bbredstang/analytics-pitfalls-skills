---
name: analytics-pitfalls-pie-charts-are-for-thanksgiving
description: "\"Pie Charts Are for Thanksgiving\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# Pie Charts Are for Thanksgiving (When Circles Make Everything Harder)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/56

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/56

## The problem

Dashboard review. Someone shows market share by product. It's a pie chart. You stare at it. Which slice is bigger—the 23% green slice or the 21% blue slice? Can't tell. You have to read the labels. Now try comparing to last quarter's pie chart. Which slices grew? Shrank? Impossible to tell without doing mental math. Pie charts force humans to compare angles and areas—our brains are terrible at both. It's like asking someone to build a car by eyeballing measurements instead of using a ruler. A bar chart would've shown the comparison instantly. But pie charts "look nice" so we keep using them. And making every analysis harder.

## The principle

Bar charts are almost always better than pie charts. Period. Our brains compare lengths easily but struggle with angles and areas. When you need to show parts of a whole, use a stacked bar chart or just a table of numbers. The ONLY time pie charts work: showing exactly 2-3 categories where precision doesn't matter ("roughly half are X, half are Y"). Otherwise? Skip them. Think manufacturing: you wouldn't use a broken measurement tool just because it looks pretty. Same with visualization—use the tool that makes comparison easy, not pretty.

## The steps

1. **Audit Your Pie Chart Usage**

Find every pie chart in your reporting:
- Count the slices (if >3, it's automatically bad)
- Ask: Are users comparing values? (if yes, bar chart is better)
- Ask: Does precision matter? (if yes, table or bar chart)

Rule: If the pie has labels with numbers, you've admitted the pie itself doesn't communicate—just show the numbers.

Test: Cover the labels. Can you still rank the slices? If no, the chart failed.
2. **Replace with Better Alternatives**

For parts-of-a-whole:
- Stacked horizontal bar (easier to compare than pie)
- Simple table (if <6 categories)
- Regular bar chart (if comparing sizes)

For time series: Line chart or bar chart (never pie)
For ranking: Horizontal bar chart, sorted

Only keep pies for: True binary (50/50, yes/no) where rough proportion is the only message.
3. **Before/After Test**

For any pie chart replacement:
- Time 5 users answering a key question with the pie
- Time same 5 users with new chart
- Track: time + accuracy

Typically: Bar charts are 3-5x faster and more accurate.

Bonus: Train your team. Show the research. Make "pie charts are for Thanksgiving" a cultural meme. When someone proposes a pie, the team says "is it Thanksgiving?"

## In practice

A retail analytics team loved pie charts. Market share dashboard: 7-slice pie chart by region. Leadership meeting: "Which region grew most?" Team scrambles to calculate. Takes 3 minutes. Meeting derailed. They rebuilt it: horizontal bar chart, regions sorted by size, previous quarter shown as light gray bars behind. Leadership glanced at it: "West region jumped 4 points, South dropped 2." Took 5 seconds. No math required. The team ran an experiment: showed 20 analysts the same data in pie vs bar chart. Asked: "Which product has highest share?" Bar chart: average 2 seconds, 100% accuracy. Pie chart: average 12 seconds, 73% accuracy. Pie charts made analysis 6x slower and error-prone. They banned pie charts org-wide except for true binary splits (yes/no, pass/fail). Clarity improved immediately.

## Inspired by

Research on visual perception (Stephen Few, Edward Tufte, Cole Nussbaumer Knaflic). Human brains compare lengths easily, angles poorly.

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
