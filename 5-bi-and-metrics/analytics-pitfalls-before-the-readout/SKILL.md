---
name: analytics-pitfalls-before-the-readout
description: "Before the readout: 17 cards from Analytics Pitfalls & Principles, by Brian Cariveau, to check a number, an analysis or a deck before it goes to leadership."
license: CC-BY-4.0
---

# Before the readout

From Analytics Pitfalls & Principles, by Brian Cariveau: 17 cards and 1 framework for a number, an analysis or a deck before it goes to leadership. Every card, free: https://www.analyticspitfalls.com/library

## How to use it

Use it when someone shares or describes a number, an analysis or a deck before it goes to leadership, before it goes any further.

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

- Who’s in the room, and what do they care about most right now?
- What do you want them to do when it’s over?
- How does it go out: a deck, a document, a live walk-through? How much time do you get?

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

1. If this number goes up, does the business actually win? A million signups or 41,000 hours saved can both go nowhere. From: The Million User Mirage (`cards/million-user-mirage.md`), The 41,000 Hours (`cards/41000-hours.md`).
2. What else could explain it? Correlation is a clue, not proof. From: Ice Cream Causes Drowning (`cards/ice-cream-causes-drowning.md`), The Rain Dance That Worked (`cards/rain-dance-that-worked.md`).
3. Is the change bigger than the noise, or did we just flip a coin a few times? From: The Coin Flip Fallacy (`cards/coin-flip-fallacy.md`).
4. What’s the average hiding? Remember the statistician who drowned in a river three feet deep, on average. From: The Statistician Who Drowned (`cards/statistician-who-drowned.md`).
5. Did we set out to prove what somebody already wanted to hear? Write down what you expect before you look. From: Finding What You Wanted to Find (`cards/finding-what-you-wanted-to-find.md`).
6. What should someone do on Monday because of this? If it only looks in the rearview mirror, nobody will do anything. From: Rearview vs Windshield (`cards/rearview-vs-windshield.md`).
7. Does every slide pass the chart standard? One chart, one message, and a title that says what’s happening. Reserve pies for Thanksgiving. If it needs a laser pointer to read, it fails. From: Pie Charts Are for Thanksgiving (`cards/pie-charts-are-for-thanksgiving.md`), The Data Ink Ratio (`cards/data-ink-ratio.md`), Story First, Data Second (`cards/story-first-data-second.md`), Sometimes Just Use the Number (`cards/sometimes-just-use-the-number.md`).
8. Does it need to be certain? Seventy percent on time beats ninety-five percent too late. Would a quick test settle it? From: The 95% Confidence Trap (`cards/95-confidence-trap.md`), Hope is Not a Strategy (`cards/hope-is-not-a-strategy.md`), The 70% Confidence Principle (`frameworks/seventy-percent-confidence.md`).
9. If AI wrote any of it, did someone actually read it? And is it inside the tolerance you set, or are you still asking whether it’s right? From: Confident, With Formatting (`cards/confident-with-formatting.md`), Is It Right? (`cards/is-it-right.md`).
10. Say the number’s right. What has to change in how people work for it to move? That’s the part a readout can’t do for you. From: We're in the Behavior Change Business (`cards/were-in-the-behavior-change-business.md`).

## Where this fits

These run in order: the strategy, then the data, then the work, then the results.

1. **The strategy**: Before the AI strategy (`analytics-pitfalls-before-the-ai-strategy`), Before the data strategy (`analytics-pitfalls-before-the-data-strategy`), Before the BI strategy (`analytics-pitfalls-before-the-bi-strategy`). Pick the one you’re writing. They sit side by side; there’s no order between them.
2. **The data**: The data layers (`analytics-pitfalls-data-layers`), Bronze, the cleaned raw layer (`analytics-pitfalls-bronze-cleaned-raw`), Silver, the system-specific layer (`analytics-pitfalls-silver-system-specific`), Gold, the system-agnostic layer (`analytics-pitfalls-gold-system-agnostic`). Start with the data layers, then bronze, silver and gold, in that order.
3. **The work**: Before the dashboard (`analytics-pitfalls-before-the-dashboard`). Once for each dashboard the strategy calls for.
4. **The results**: Before the readout (`analytics-pitfalls-before-the-readout`). When the first numbers go to leadership. This one is here.

This is the last of them. When you're done, say so: the next round starts again with the strategy.

## The cards

- **The Million User Mirage (Celebrating the Wrong Wins)** (`cards/million-user-mirage.md`): pitfall, Metrics & Evidence. Track what matters, not what looks good on a slide. Ask: "If this metric goes up, does revenue go up? Do customers get happier? Does the business actually win?"
- **The 41,000 Hours (Saved From What, Spent Where?)** (`cards/41000-hours.md`): pitfall, Metrics & Evidence. Never skip the middle. Engagement, experience, effectiveness, efficiency: in that order, every time. At work: "AI saved us 41,000 hours this year."
- **Ice Cream Causes Drowning (When Numbers Lie)** (`cards/ice-cream-causes-drowning.md`): pitfall, Metrics & Evidence. Always ask: "What else could explain this relationship?" Correlation is a clue, not proof.
- **The Rain Dance That Worked (When You Credit the Wrong Thing)** (`cards/rain-dance-that-worked.md`): pitfall, Metrics & Evidence. Before you credit success to your action, ask: "What would have happened anyway?" At work: "Sales went up right after we launched it, so it worked."
- **The Coin Flip Fallacy (When Noise Looks Like Signal)** (`cards/coin-flip-fallacy.md`): pitfall, Metrics & Evidence. Don't confuse noise with signal. Before you react to a change, ask: "Is this statistically significant or just random fluctuation?"
- **The Statistician Who Drowned (in a River with Average Depth 3 Feet)** (`cards/statistician-who-drowned.md`): pitfall, Metrics & Evidence. Dig into the distribution, not just the average. Look at medians, percentiles, outliers.
- **Finding What You Wanted to Find (Even When It Wasn't There)** (`cards/finding-what-you-wanted-to-find.md`): pitfall, Metrics & Evidence. Seek to be proven wrong, not right. Before you analyze, write down what you expect to find.
- **Rearview vs Windshield (Stop Driving While Staring Backwards)** (`cards/rearview-vs-windshield.md`): principle, Metrics & Evidence. Balance rearview (lagging) with windshield (leading) metrics. Lagging metrics tell you what happened (revenue, conversions, churn).
- **Pie Charts Are for Thanksgiving (When Circles Make Everything Harder)** (`cards/pie-charts-are-for-thanksgiving.md`): pitfall, Dashboards & Visualization. Bar charts are almost always better than pie charts. Period. Our brains compare lengths easily but struggle with angles and areas.
- **The Data Ink Ratio (Every Pixel Must Earn Its Place)** (`cards/data-ink-ratio.md`): principle, Dashboards & Visualization. Data-ink ratio: the proportion of ink (pixels) used to show actual data vs decoration.
- **Story First, Data Second (Storyboard Before You Build)** (`cards/story-first-data-second.md`): principle, Dashboards & Visualization. Storyboard first, build second. Before touching any tools, grab a pencil and sketch: What's the hook?
- **Sometimes Just Use the Number (When a Chart Makes Things Worse)** (`cards/sometimes-just-use-the-number.md`): principle, Dashboards & Visualization. Not everything needs a chart. If you're showing 1-3 numbers, especially a key metric, just show the number.
- **The 95% Confidence Trap (Perfection is the Enemy of Progress)** (`cards/95-confidence-trap.md`): pitfall, Metrics & Evidence. Ship at 70% confidence and learn fast. Set a decision deadline and work backward. At work: "Let’s wait until the data is perfect."
- **Hope is Not a Strategy (Why Guessing is Expensive)** (`cards/hope-is-not-a-strategy.md`): pitfall, Metrics & Evidence. Test everything. A/B test product changes, pricing, messaging, features—anything customers interact with.
- **Confident, With Formatting (When Nobody Reads What the AI Wrote)** (`cards/confident-with-formatting.md`): pitfall, Metrics & Evidence. Your name is on it, so read it. Checking is faster than doing, and it is never zero.
- **Is It Right? (The Wrong Question to Ask of AI)** (`cards/is-it-right.md`): pitfall, Metrics & Evidence. Ask whether it's within tolerance, and how you know. Nothing is right every time, in a factory or in AI.
- **We're in the Behavior Change Business (Not the Data Business)** (`cards/were-in-the-behavior-change-business.md`): principle, Adoption & Product. Apply consumer behavior principles to analytics adoption. Make it stupid simple to use—reduce friction, eliminate training requirements where possible.

## The frameworks

- **The 70% Confidence Principle** (`frameworks/seventy-percent-confidence.md`): The 70% Confidence Principle means shipping a directional answer at 70% confidence and learning fast, instead of chasing 95% certainty while the business waits.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
