---
name: analytics-pitfalls-data-ink-ratio
description: "\"The Data Ink Ratio\" (Every Pixel Must Earn Its Place): a principle card from Analytics Pitfalls & Principles, by Brian Cariveau. Use when a plan, request, dashboard, metric or AI project needs it."
license: CC-BY-4.0
---

# The Data Ink Ratio (Every Pixel Must Earn Its Place)

A principle card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/57

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work could use this principle.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/57

## The problem

Dashboard has 3D charts with shadows. Gradient fills. Grid lines every 5 units. Decorative borders. Background images. Looks "fancy." But here's what happened: users spent 40 seconds finding the actual data point they needed because all the decoration obscured it. That 3D effect? Makes values impossible to read accurately. Those grid lines? Competing for attention with your actual data. The gradient fill? Pure decoration adding zero information. It's like manufacturing a car and adding decorative bolts that don't hold anything—they're just there to look mechanical. Every pixel that isn't showing data is clutter. And clutter kills comprehension.

## The principle

Data-ink ratio: the proportion of ink (pixels) used to show actual data vs decoration. Aim for 80%+. Remove everything that doesn't represent data: 3D effects, shadows, gradients, excessive grid lines, decorative borders, background images, redundant labels. The magic happens when your visualization is so clean that the data jumps off the page. Think manufacturing: Toyota's production lines are spotless—every tool has a place, nothing extra. Same with visualizations. Tufte said it best: "Perfection is achieved not when there is nothing more to add, but when there is nothing left to take away."

## The steps

1. **Calculate Your Data-Ink Ratio**

For key visualizations:
- Print them in grayscale
- Circle every pixel showing actual data
- Everything else is decoration

Estimate: What % of ink represents data vs decoration?

If <50%, you have a clutter problem.

Target: 80%+ of pixels show data. The rest should be minimal: axis, labels, white space.
2. **Remove Chart Junk Systematically**

Go through each chart element:
- 3D effects? Remove (makes values inaccurate)
- Shadows? Remove (pure decoration)
- Gradients? Remove (use solid colors)
- Grid lines? Keep 0-2 reference lines max
- Borders? Remove unless necessary
- Background images/patterns? Remove
- Decorative logos? Remove from chart area
- Redundant labels? Remove

Rule: If removing it doesn't lose information, remove it.
3. **Test Comprehension Improvement**

Before/after test:
- Show 5 users old chart: "Find the value for Q3 sales"
- Time them
- Show new cleaned chart: same question
- Time them

Typically: Clean charts are 2-4x faster.

Make it a review standard: Every chart must pass data-ink ratio check (>70% data, <30% decoration).

Bonus: Cleaner charts are faster to build and easier to update.

## In practice

A financial services team had executive dashboards with 3D bar charts, gradient backgrounds, decorative logos on every chart, grid lines every 2 units, shadows on every element. It looked "professional." User testing revealed: executives took 45 seconds average to find a specific number. Charts were pretty but hard to read. They applied data-ink ratio principle: removed 3D (flat bars only), removed gradients (solid colors), removed decorative elements, reduced grid lines to 0 (just axis), removed shadows. Same data, cleaner presentation. Re-tested: executives found numbers in 8 seconds (82% reduction). More importantly: they noticed trends instantly because nothing competed for attention. One exec said: "Finally, I can just look at the data instead of decoding the chart." The team tracked time-to-action: dropped 65% across all dashboards. Less decoration = more comprehension.

## Inspired by

Edward Tufte's data-ink ratio principle. Antoine de Saint-Exupéry: "Perfection is achieved when there is nothing left to take away."

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
