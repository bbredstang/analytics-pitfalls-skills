---
name: analytics-pitfalls-before-the-dashboard
description: "Before the dashboard: 11 cards from Analytics Pitfalls & Principles, by Brian Cariveau, to check a dashboard request or a draft dashboard."
license: CC-BY-4.0
---

# Before the dashboard

From Analytics Pitfalls & Principles, by Brian Cariveau: 11 cards and 2 frameworks for a dashboard request or a draft dashboard. Every card, free: https://www.analyticspitfalls.com/library

## How to use it

Use it when someone shares or describes a dashboard request or a draft dashboard, before it goes any further.

1. First, get their situation (below), so everything after fits their company, not a generic one.
2. Take Brian Cariveau's questions below in order, against their actual work, and ask them in his words rather than your own. For each, open the files it names and answer from them.
3. Hold the work to Brian Cariveau's standard (the sections before the questions). Where it falls short, say where, in his words.
4. Skip a question the work already answers well. Say so in a line and move on.
5. Then pick the one or two cards that matter most for this work, say why in a sentence each, and give their principles in the cards' own words. Never hand someone the whole list.
6. Say the work looks like a pitfall; never tell someone they have it. If nothing fits, say so.
7. Finish with the links of the cards you used, and say which skill comes next (Where this fits, below).

## First, their situation

The cards are general. Their work isn't. The first time this comes up with someone, find out enough that every answer fits their company, their systems and their people, not everyone's.

1. Start with what you already know: this conversation, what they pasted, and anything your tool remembers about them. Never ask what you can already see.
2. Ask only what would change your answer. Three questions at most, in one short message, in plain words. Never a form.
3. If they'd rather just go, go. Say in a line what you're assuming (seventy percent is enough to start) and correct it as you learn.
4. Don't ask for anything confidential: no names of people, no customer data. A sentence in general terms is plenty.
5. Then use what they told you, by name, in every answer: their industry, their systems, their tools, their teams. Never "your organization."
6. If your tool keeps memory and they're happy for it to, remember the answers, so the next skill doesn't ask again.

What to find out, if you can’t already see it:

- Who is it for, and what do they do in a normal week?
- Where will it live: Power BI, Tableau, Looker, a deck, an artifact or app your AI builds?
- What do they use today instead, and is there a sketch or a draft yet?

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

1. What action will someone take when they see it? Name the person and the action. If nobody can, don’t build it. From: The Sexy Map Trap (`cards/sexy-map-trap.md`), Story First, Data Second (`cards/story-first-data-second.md`).
2. Is there already a dashboard for this, and would one number do the job? If you’re adding one, kill one nobody uses. From: Death by Dashboard (`cards/death-by-dashboard.md`), Sometimes Just Use the Number (`cards/sometimes-just-use-the-number.md`).
3. Has anyone reacted to a sketch yet? Build the picture first. Nobody gets excited approving a bullet point. From: Build the Picture First (`cards/build-the-picture-first.md`), Build That! (`frameworks/build-that.md`).
4. Will they act on it right there, or export it to Excel and act somewhere else? If it’s the export, ask why. From: The Data Export Trap (`cards/data-export-trap.md`).
5. How will you know it’s used? Usage is the receipt. Set the date it goes if nobody opens it. From: Usage Is the Receipt (`frameworks/usage-is-the-receipt.md`).
6. Is every chart the right one? Name what each compares, then pick the chart for it (the chart standard, above). Reserve pies for Thanksgiving. One number gets the number, not a gauge. A map only when where is the point. From: Pie Charts Are for Thanksgiving (`cards/pie-charts-are-for-thanksgiving.md`), Sometimes Just Use the Number (`cards/sometimes-just-use-the-number.md`), The Sexy Map Trap (`cards/sexy-map-trap.md`).
7. If there’s a draft, does every pixel earn its place? No 3D, no gradients, no decoration, gray unless it needs acting on, and nothing an executive needs a ruler and a highlighter to read. From: The Data Ink Ratio (`cards/data-ink-ratio.md`), The Ruler and Highlighter Test (`cards/ruler-and-highlighter-test.md`).
8. If AI builds the reports now, does each one change what someone does? Or is it the old report, faster? From: Faster at the Old Way (`cards/faster-at-the-old-way.md`).
9. Who has to work differently for this to get used, and what are they giving up? The dashboard is the easy part. From: We're in the Behavior Change Business (`cards/were-in-the-behavior-change-business.md`).

## Where this fits

These run in order: the strategy, then the data, then the work, then the results.

1. **The strategy**: Before the AI strategy (`analytics-pitfalls-before-the-ai-strategy`), Before the data strategy (`analytics-pitfalls-before-the-data-strategy`), Before the BI strategy (`analytics-pitfalls-before-the-bi-strategy`). Pick the one you’re writing. They sit side by side; there’s no order between them.
2. **The data**: The data layers (`analytics-pitfalls-data-layers`), Bronze, the cleaned raw layer (`analytics-pitfalls-bronze-cleaned-raw`), Silver, the system-specific layer (`analytics-pitfalls-silver-system-specific`), Gold, the system-agnostic layer (`analytics-pitfalls-gold-system-agnostic`). Start with the data layers, then bronze, silver and gold, in that order.
3. **The work**: Before the dashboard (`analytics-pitfalls-before-the-dashboard`). Once for each dashboard the strategy calls for. This one is here.
4. **The results**: Before the readout (`analytics-pitfalls-before-the-readout`). When the first numbers go to leadership.

When you're done, say what comes next, by name: Before the readout (`analytics-pitfalls-before-the-readout`). When the first numbers go to leadership.

## The cards

- **The Sexy Map Trap (Just Because You Can, Doesn't Mean You Should)** (`cards/sexy-map-trap.md`): pitfall, Dashboards & Visualization. Ask the brutal question: "Does this visualization make someone want to take action?"
- **Story First, Data Second (Storyboard Before You Build)** (`cards/story-first-data-second.md`): principle, Dashboards & Visualization. Storyboard first, build second. Before touching any tools, grab a pencil and sketch: What's the hook?
- **Death by Dashboard (When More Became Less)** (`cards/death-by-dashboard.md`): pitfall, Dashboards & Visualization. Less is more. Seriously. Kill the dashboards nobody uses. I mean it—delete them. At work: "We need a dashboard for that."
- **Sometimes Just Use the Number (When a Chart Makes Things Worse)** (`cards/sometimes-just-use-the-number.md`): principle, Dashboards & Visualization. Not everything needs a chart. If you're showing 1-3 numbers, especially a key metric, just show the number.
- **Build the Picture First: Why Mockups Beat Requirements Documents** (`cards/build-the-picture-first.md`): pitfall, Delivery & Execution. Pictures are more powerful than words. Mockups are better specs than requirements documents. At work: "Send me the requirements doc first."
- **The Data Export Trap (When Your Dashboards Are Just CSV Machines)** (`cards/data-export-trap.md`): pitfall, Adoption & Product. Measure data export rate. If >40% of dashboard views end in data export, you built a data dump, not an analytics solution. At work: "Can I get that as an export to Excel?"
- **Pie Charts Are for Thanksgiving (When Circles Make Everything Harder)** (`cards/pie-charts-are-for-thanksgiving.md`): pitfall, Dashboards & Visualization. Bar charts are almost always better than pie charts. Period. Our brains compare lengths easily but struggle with angles and areas.
- **The Data Ink Ratio (Every Pixel Must Earn Its Place)** (`cards/data-ink-ratio.md`): principle, Dashboards & Visualization. Data-ink ratio: the proportion of ink (pixels) used to show actual data vs decoration.
- **The Ruler and Highlighter Test (When Executives Need Props to Read Your Report)** (`cards/ruler-and-highlighter-test.md`): pitfall, Dashboards & Visualization. Pass the ruler test: if someone needs physical tools to follow your report, it fails.
- **Faster at the Old Way (Paving the Cow Path With AI)** (`cards/faster-at-the-old-way.md`): pitfall, Dashboards & Visualization. Stop asking for the deck. Ask for the answer, and what the person would do about it. At work: "AI can build us a new report every day now."
- **We're in the Behavior Change Business (Not the Data Business)** (`cards/were-in-the-behavior-change-business.md`): principle, Adoption & Product. Apply consumer behavior principles to analytics adoption. Make it stupid simple to use—reduce friction, eliminate training requirements where possible.

## The frameworks

- **Build That!** (`frameworks/build-that.md`): Build That! means validating ideas with a mockup people can react to before writing requirements — the picture is the spec, not a document nobody can quite picture.
- **Usage Is the Receipt** (`frameworks/usage-is-the-receipt.md`): Usage Is the Receipt means the only proof an analytics product worked is whether people actually use it — adoption is the receipt, everything else is a claim.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
