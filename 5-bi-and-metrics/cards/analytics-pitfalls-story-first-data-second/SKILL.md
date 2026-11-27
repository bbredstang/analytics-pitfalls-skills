---
name: analytics-pitfalls-story-first-data-second
description: "\"Story First, Data Second\" (Storyboard Before You Build): a principle card from Analytics Pitfalls & Principles, by Brian Cariveau. Use when a plan, request, dashboard, metric or AI project needs it."
license: CC-BY-4.0
---

# Story First, Data Second (Storyboard Before You Build)

A principle card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/58

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work could use this principle.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/58

## The problem

Project kickoff: "Build a sales dashboard." Team immediately opens Tableau. Starts dragging fields. Builds 6 charts. Spends 40 hours. Presents to stakeholders. Response: "This is nice, but it doesn't answer my questions." Why? Because you built data visualizations, not a story. You threw charts at a problem without understanding the narrative. What action will they take? What question needs answering? What's the tension? The solution? You skipped all that and went straight to building. It's like a manufacturing plant starting production without a blueprint—you'll build something, but probably not what's needed.

## The principle

Storyboard first, build second. Before touching any tools, grab a pencil and sketch: What's the hook? What tension exists? What solution are you offering? What proof matters? How does it close? Map the narrative arc: Hook → Set Stage → Create Tension → Offer Solution → Provide Proof → Close with action. Then translate that story into data visualizations. Each chart should serve a part of the story. The magic happens when your dashboard tells a story, not just shows data. Think manufacturing: you don't start welding metal until the blueprint is done. Same with analytics—storyboard the narrative before building the viz.

## The steps

1. **Mandatory Storyboard Session**

Before building ANY executive presentation:
- Gather stakeholders
- Grab pencils, post-its, whiteboard
- Map the story arc:
  * Hook: Why should they care?
  * Set stage: What's the context?
  * Tension: What's the problem?
  * Solution: What are you proposing?
  * Proof: Why will it work?
  * Close: What's next?

Spend 60-90 minutes. Don't touch data tools yet.

Output: 6-8 post-its with key beats of the story.
2. **Map Data to Story Beats**

For each story beat:
- What data supports it?
- What visualization type? (one number? trend? comparison?)
- What's the main point? (write it in one sentence)

Example:
- Tension beat: "Problem is growing"
- Data: Member coverage gaps over time
- Viz: Line chart showing 40% increase
- Point: "Coverage gaps up 40% in 18 months"

Rule: Each chart must serve a story beat. If it doesn't, cut it.
3. **Test the Narrative**

Before building:
- Walk through the storyboard with someone unfamiliar
- Ask: "Does the story flow? Is anything missing? Confusing?"

After building:
- Show to a test audience
- Ask them to summarize the main point
- If they can't, the story failed

Goal: Anyone should be able to follow the narrative without explanation.

Bonus: Storyboards cut build time 50% (because you know exactly what to build and why).

## In practice

A Fortune 5 healthcare company's team got a request: "Show impact of coverage gaps on members." They almost started building dashboards. Instead, new leader said: "Storyboard it first." They grabbed pencils and post-its: Hook (member John's story of coverage gap), Set stage (how common is this?), Tension (growing problem, financial impact), Solution (proposed fix), Proof (pilot results), Close (next steps). Took 90 minutes. Then built the presentation: 1 slide per story beat. 6 slides total. 3 charts. When presented: exec team immediately understood, asked strategic questions, approved budget on the spot. Old approach would've been 20 slides of data with no narrative thread. The storyboard forced clarity: what's the ONE thing we're trying to communicate? Everything else fell into place. Time to approval: 1 meeting (vs typical 3-4). Storyboarding became mandatory for all executive presentations.

## Inspired by

Nancy Duarte's storytelling framework. Cole Nussbaumer Knaflic's "Storytelling with Data." a Fortune 10 healthcare company storyboarding practice (2019-2025).

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
