---
name: analytics-pitfalls-sexy-map-trap
description: "\"The Sexy Map Trap\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# The Sexy Map Trap (Just Because You Can, Doesn't Mean You Should)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/27

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/27

## The problem

Your designer shows you a gorgeous interactive geo map with animated bubbles and zoom controls. It looks incredible. You green-light it. Three months later, nobody uses it. Why? Because it takes up the entire screen, loads slowly, and doesn't actually make people want to do anything. Users stare at it, say "cool," and then... nothing. No action. No decisions. No change. Meanwhile, a boring-looking Pareto chart would've made them immediately say "we need to kill the bottom 80%" and actually take action. Just because you can build something sexy doesn't mean you should. Fancy visualizations are like putting a spoiler on a minivan—looks cool, doesn't make it faster, and actually makes it less practical.

## The principle

Ask the brutal question: "Does this visualization make someone want to take action?" If the answer is no, simplify it. A geo map showing sales by region? Cool. But does it make you want to fix underperforming regions? Probably not. A Pareto chart showing the same data? Boring. But it screams "80% of your revenue comes from 20% of regions—focus there or kill the rest!" That emotional punch drives action. The manufacturing mindset: your dashboard is a product. If it doesn't drive behavior change, it's waste. Prioritize clarity over creativity, action over aesthetics. Use maps only when geography actually matters (routing, proximity, coverage gaps). Otherwise, use the simplest chart that creates urgency. The magic happens when someone sees your dashboard and immediately knows what to do. That's the goal—not winning design awards.

## The steps

1. Ask the Action Question: "Does this viz make someone want to DO something?" If no, simplify. Replace fancy maps with boring charts that scream urgency.
2. Test with Real Users: Show your viz to actual users. Watch them. Do they immediately know what action to take? If they stare confused, you failed. Rebuild.
3. Default to Simplest Chart: Bar charts, line charts, Pareto charts. Only use maps when geography actually matters (routing, proximity). Otherwise, go simple.

## In practice

A retail analytics team built a stunning geo map showing store performance across 200 locations. Bubbles sized by revenue, color-coded by profit margin, interactive tooltips with 12 metrics. Executive team loved the demo. Launch day: 8% adoption. Why? Too much cognitive load. Users didn't know where to look or what to do. Rebuilt it as three simple charts: (1) Pareto of stores by revenue (focus on top 20%), (2) Bar chart of bottom performers (kill or fix these 10), (3) Trend lines for stores in the middle (monitor these). Adoption jumped to 67%. Why? Each chart screamed an action: "Focus here," "Fix these," "Watch this." Regional VPs started closing underperforming stores and reallocating resources to winners. Revenue per store increased 18% in 6 months. The sexy map gathered dust. The boring charts changed behavior. Just because you can build fancy doesn't mean you should.

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
