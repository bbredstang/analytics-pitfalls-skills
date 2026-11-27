---
name: analytics-pitfalls-before-the-bi-strategy
description: "Before the BI strategy: 16 cards from Analytics Pitfalls & Principles, by Brian Cariveau, to check a BI strategy, a reporting roadmap or a self-service plan."
license: CC-BY-4.0
---

# Before the BI strategy

From Analytics Pitfalls & Principles, by Brian Cariveau: 16 cards and 5 frameworks for a BI strategy, a reporting roadmap or a self-service plan. Every card, free: https://www.analyticspitfalls.com/library

## How to use it

Use it when someone shares or describes a BI strategy, a reporting roadmap or a self-service plan, before it goes any further.

Walk it like a factory floor. Every dashboard and report is a product on the shelf, and usage is the sale. Find the waste and get rid of it. Make what’s left stupidly simple.

1. First, get their situation (below), so everything after fits their company, not a generic one.
2. Take Brian Cariveau's questions below in order, against their actual work, and ask them in his words rather than your own. For each, open the files it names and answer from them.
3. Hold every answer to the lens above.
4. Hold the work to Brian Cariveau's standard (the sections before the questions). Where it falls short, say where, in his words.
5. Skip a question the work already answers well. Say so in a line and move on.
6. Then pick the one or two cards that matter most for this work, say why in a sentence each, and give their principles in the cards' own words. Never hand someone the whole list.
7. Say the work looks like a pitfall; never tell someone they have it. If nothing fits, say so.
8. Then put it on the canvas, and offer the board (below).
9. Finish with the links of the cards you used, and say which skill comes next (Where this fits, below).

## First, their situation

The cards are general. Their work isn't. The first time this comes up with someone, find out enough that every answer fits their company, their systems and their people, not everyone's.

1. Start with what you already know: this conversation, what they pasted, and anything your tool remembers about them. Never ask what you can already see.
2. Ask only what would change your answer. Three questions at most, in one short message, in plain words. Never a form.
3. If they'd rather just go, go. Say in a line what you're assuming (seventy percent is enough to start) and correct it as you learn.
4. Don't ask for anything confidential: no names of people, no customer data. A sentence in general terms is plenty.
5. Then use what they told you, by name, in every answer: their industry, their systems, their tools, their teams. Never "your organization."
6. If your tool keeps memory and they're happy for it to, remember the answers, so the next skill doesn't ask again.

What to find out, if you can’t already see it:

- What business are you in, and roughly how big is it?
- Which BI tools are in use, and roughly how many dashboards? Do you know how many get opened?
- Who reads them: executives, managers, front-line teams, customers?
- Is it one central team building, self-service, or both?
- What’s pushing this now: a tool change, cost, an AI push, people not using what’s there?

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

## Brian Cariveau's questions

1. Does it put engagement first, before experience, effectiveness and efficiency? The order is non-negotiable. From: The Four E's (`frameworks/four-es.md`).
2. Which products on the shelf actually sell? Usage is the receipt. Count who acts on it, not what you shipped. From: The Sugar High Syndrome (`cards/sugar-high-syndrome.md`), The Analytics Assembly Line (`cards/analytics-assembly-line.md`), Usage Is the Receipt (`frameworks/usage-is-the-receipt.md`), Manufacturing Mindset (`frameworks/manufacturing-mindset.md`).
3. Where’s the waste? Kill the dashboards nobody’s opened in 90 days before you build one more. Five beloved dashboards beat forty-seven mediocre ones. From: Death by Dashboard (`cards/death-by-dashboard.md`), Kill the Waste (`cards/kill-the-waste.md`).
4. Is it stupidly simple? One page, the key numbers, clear actions. From: Everything Complex Can Seem Simple (`cards/everything-complex-can-seem-simple.md`), The Sophistication Trap (`cards/sophistication-trap.md`).
5. Is there one chart standard every team builds to, in the BI tool, the decks and whatever AI builds? Reserve pies for Thanksgiving, and make every pixel earn its place. If every team picks its own charts, every report reads differently. From: Pie Charts Are for Thanksgiving (`cards/pie-charts-are-for-thanksgiving.md`), The Data Ink Ratio (`cards/data-ink-ratio.md`), The Ruler and Highlighter Test (`cards/ruler-and-highlighter-test.md`).
6. Is there one front door, or a scattered treasure map? Show people the twenty they’ll want, not all 2,154. From: The Scattered Treasure Map (`cards/scattered-treasure-map.md`), The Netflix Principle (`cards/netflix-principle.md`).
7. One way of working, or a tool circus running in all directions? And do the pieces feed each other, or sit on their own islands? From: Running in All Directions (`cards/running-in-all-directions.md`), The Island of Misfit Dashboards (`cards/island-of-misfit-dashboards.md`), Ecosystems Over Products (`frameworks/ecosystems-over-products.md`).
8. Who’s already built a better one in Excel? They aren’t risk creators, they’re value creators without the right tools. Start with them. From: The Risk Creator Paradox (`cards/risk-creator-paradox.md`).
9. When did you last walk the catwalk and use it like someone who has to? From: Walk the Catwalk (`cards/walk-the-catwalk.md`).
10. Who has to work differently for this to stick, and what are they giving up? We’re in the behavior change business. From: We're in the Behavior Change Business (`cards/were-in-the-behavior-change-business.md`), It Was Never About the Tech (`frameworks/it-was-never-about-the-tech.md`).
11. Who’s on your board? Before this goes to anyone, convene a few people who’d poke holes in it, and hear them out now. It’s a lot cheaper than hearing it later.

## Put it on the canvas

When the questions are done, shuffle the strategy onto one page: four boxes. This isn't the business lean canvas. It's People, Process, Technology and Agentic.

- **People**: Who has to change, who leads it, who pushes back, and what they have to learn or give up.
- **Process**: How the work flows, where it waits, and what stops.
- **Technology**: The platforms, the data and the definitions it runs on.
- **Agentic**: Anything in the new agentic world: which agents, what they do on their own, the tolerance they work within, and who watches them.

Three to five short lines a box, in the person's own words where you can. Under each box, one line for the adaptive part: what has to change in people for that box to work.

Draw it as a visual. Where you can make an artifact or a web page, fill in `canvas.html`: replace every {{…}} (each _LINES with `<li>` items) and keep the credit line. Anywhere else, draw it as a two-by-two table.

## Convene the board

Offer it, don't spring it. If they say yes, play each member in turn: each asks their hardest question about the canvas and says what would change their mind. Then say what you'd change on the canvas, and draw it again.

The board, until they swap anyone (ask):

- The CFO
- The most skeptical leader in the building
- Someone who opens the reports every Monday
- The analyst who already built a better one in Excel
- Whoever has to build and run it

## Where this fits

These run in order: the strategy, then the data, then the work, then the results.

1. **The strategy**: Before the AI strategy (`analytics-pitfalls-before-the-ai-strategy`), Before the data strategy (`analytics-pitfalls-before-the-data-strategy`), Before the BI strategy (`analytics-pitfalls-before-the-bi-strategy`). Pick the one you’re writing. They sit side by side; there’s no order between them. This one is here.
2. **The data**: The data layers (`analytics-pitfalls-data-layers`), Bronze, the cleaned raw layer (`analytics-pitfalls-bronze-cleaned-raw`), Silver, the system-specific layer (`analytics-pitfalls-silver-system-specific`), Gold, the system-agnostic layer (`analytics-pitfalls-gold-system-agnostic`). Start with the data layers, then bronze, silver and gold, in that order.
3. **The work**: Before the dashboard (`analytics-pitfalls-before-the-dashboard`). Once for each dashboard the strategy calls for.
4. **The results**: Before the readout (`analytics-pitfalls-before-the-readout`). When the first numbers go to leadership.

When you're done, say what comes next, by name: The data layers (`analytics-pitfalls-data-layers`). Start with the data layers, then bronze, silver and gold, in that order.

## The cards

- **The Sugar High Syndrome** (`cards/sugar-high-syndrome.md`): pitfall, Strategy & Focus. If nobody uses it, it's worth nothing. Think of your data assets like retail inventory.
- **The Analytics Assembly Line (Why Your Data is Just Raw Materials)** (`cards/analytics-assembly-line.md`): principle, Delivery & Execution. Treat your data ecosystem like a clean manufacturing line with zero waste. Raw materials (data) enter on the left—inspect for quality, reject defects.
- **Death by Dashboard (When More Became Less)** (`cards/death-by-dashboard.md`): pitfall, Dashboards & Visualization. Less is more. Seriously. Kill the dashboards nobody uses. I mean it—delete them. At work: "We need a dashboard for that."
- **Kill the Waste (The Lean Analytics Playbook)** (`cards/kill-the-waste.md`): principle, Delivery & Execution. Adopt a lean manufacturing mindset: identify waste, eliminate it ruthlessly, free up capacity for value creation.
- **Everything Complex Can Seem Simple (The Art of Ruthless Simplification)** (`cards/everything-complex-can-seem-simple.md`): principle, Strategy & Focus. Relentlessly simplify. Every metric, model, and process—ask: "Can this be simpler?"
- **The Sophistication Trap** (`cards/sophistication-trap.md`): pitfall, Strategy & Focus. Simple is what scales. Simple is what teams can execute. Simple is what actually transforms organizations.
- **Pie Charts Are for Thanksgiving (When Circles Make Everything Harder)** (`cards/pie-charts-are-for-thanksgiving.md`): pitfall, Dashboards & Visualization. Bar charts are almost always better than pie charts. Period. Our brains compare lengths easily but struggle with angles and areas.
- **The Data Ink Ratio (Every Pixel Must Earn Its Place)** (`cards/data-ink-ratio.md`): principle, Dashboards & Visualization. Data-ink ratio: the proportion of ink (pixels) used to show actual data vs decoration.
- **The Ruler and Highlighter Test (When Executives Need Props to Read Your Report)** (`cards/ruler-and-highlighter-test.md`): pitfall, Dashboards & Visualization. Pass the ruler test: if someone needs physical tools to follow your report, it fails.
- **The Scattered Treasure Map (When Nobody Can Find Anything)** (`cards/scattered-treasure-map.md`): pitfall, Adoption & Product. Build one front door. Amazon doesn't make you search 12 websites to buy a book. Create a single analytics portal with search, filters, categories, and ratings—just like eCommerce.
- **The Netflix Principle (Recommend, Don't Force)** (`cards/netflix-principle.md`): principle, Adoption & Product. Build a recommendation engine. Netflix doesn't show you 10,000 movies—it shows you 20 you'll probably like based on what others watched.
- **Running in All Directions (The Tool Circus Nobody Asked For)** (`cards/running-in-all-directions.md`): pitfall, Strategy & Focus. Progress requires everyone running down the SAME side of the road together. When everyone picks different paths, you see small pockets of value team by team, but as a whole it diminishes your organization's fitness. At work: "Let’s buy a tool for that."
- **The Island of Misfit Dashboards (When Nothing Talks to Anything)** (`cards/island-of-misfit-dashboards.md`): pitfall, Data Foundations. Build an ecosystem of interconnected solutions, not isolated products. Adopt a Product over Project mindset, but avoid monolithic systems—know when to erase a bubble and retire components when value diminishes.
- **The Risk Creator Paradox (Your "Shadow IT" is Creating All the Value)** (`cards/risk-creator-paradox.md`): principle, Leadership & Teams. Flip the narrative. Those Excel power users aren't risk creators—they're value creators who lack proper tools.
- **Walk the Catwalk (Go See the Work, Don't Just Read Reports)** (`cards/walk-the-catwalk.md`): principle, Leadership & Teams. Walk the catwalk. Manufacturing term: executives regularly walk the production floor (catwalk), watching work happen, talking to operators, spotting problems.
- **We're in the Behavior Change Business (Not the Data Business)** (`cards/were-in-the-behavior-change-business.md`): principle, Adoption & Product. Apply consumer behavior principles to analytics adoption. Make it stupid simple to use—reduce friction, eliminate training requirements where possible.

## The frameworks

- **The Four E's** (`frameworks/four-es.md`): The Four E's — Engagement, Experience, Effectiveness, Efficiency — describe the order analytics maturity actually moves through, and the order is non-negotiable: chase efficiency before anyone is engaged and you optimize something nobody uses.
- **Usage Is the Receipt** (`frameworks/usage-is-the-receipt.md`): Usage Is the Receipt means the only proof an analytics product worked is whether people actually use it — adoption is the receipt, everything else is a claim.
- **Manufacturing Mindset** (`frameworks/manufacturing-mindset.md`): The Manufacturing Mindset treats data work as factory work — measuring throughput, cycle time, waste, and yield instead of counting deliverables.
- **Ecosystems Over Products** (`frameworks/ecosystems-over-products.md`): Ecosystems Over Products means building an interconnected system of analytics assets that reference and reinforce each other, instead of a pile of isolated dashboards and models that each stand alone.
- **It Was Never About the Tech** (`frameworks/it-was-never-about-the-tech.md`): It Was Never About the Tech is the observation that analytics transformations fail on politics, people, and principles far more often than on tooling — the technology is rarely the binding constraint.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
