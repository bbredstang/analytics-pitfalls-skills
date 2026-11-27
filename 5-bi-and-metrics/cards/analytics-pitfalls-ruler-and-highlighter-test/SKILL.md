---
name: analytics-pitfalls-ruler-and-highlighter-test
description: "\"The Ruler and Highlighter Test\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# The Ruler and Highlighter Test (When Executives Need Props to Read Your Report)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/54

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/54

## The problem

Executive meeting. You present your beautiful report. Data everywhere. Every KPI you could think of. Packed full of insights. Then you notice: the SVP pulls out a ruler. And a highlighter. She's physically drawing lines on her printed copy to track rows across the table. Using the highlighter to mark which numbers matter. You just watched a C-level executive need physical tools to decode your work. That's not analysis—that's archaeology. It's like building a car where drivers need a manual just to find the gas pedal. If executives need rulers and highlighters to read your report, your report is too dense. And you just lost the room.

## The principle

Pass the ruler test: if someone needs physical tools to follow your report, it fails. Less is more. White space is your friend. Show 5 numbers, not 50. Use visual hierarchy to guide the eye. Bold what matters. Gray out what doesn't. Add space between sections. Think manufacturing: a good assembly line doesn't make workers hunt for tools—everything is within arm's reach, clearly labeled. Same with reports. The magic happens when an executive can glance at your report for 30 seconds and know exactly what matters. No props required.

## The steps

1. **The Ruler Test**

Print your report. Hand it to someone unfamiliar with it.

Watch them read it. Do they:
- Use their finger to track across rows?
- Get lost in the data?
- Ask "what should I look at?"

If yes, it's too dense.

Rule: If >10 numbers are equally prominent, it fails. Pick the 3-5 that matter most. Make them big. Everything else is secondary.
2. **Apply Visual Hierarchy**

Before building:
- Identify the ONE thing that matters most
- Make it biggest/boldest
- Gray out supporting data (still there, but not competing for attention)
- Add white space between sections
- Use alignment to create visual flow

Test: Cover the report and ask "what's the point?" If you can't answer in 5 words, the hierarchy is wrong.
3. **The 30-Second Glance Test**

Can someone unfamiliar with your content:
- Glance at it for 30 seconds
- Tell you the main point
- Identify the key numbers

If no, simplify more.

Executives have 30 seconds. Make them count. Remove everything that doesn't support the main point.

Bonus: Dense reports get skipped. Simple reports get read and acted on.

## In practice

A Fortune 5 healthcare company's analytics team in 2019 presented quarterly results to C-suite. The report: 18 columns, 94 rows, tiny font, packed dense. No white space. A senior exec pulled out a ruler and highlighter mid-meeting to track data across rows. The team was mortified. They rebuilt it: 1 chart showing the trend, 3 key numbers (large font), 2 sentences explaining why. 90% reduction in data shown. Next meeting: exec spent 30 seconds, understood everything, asked great questions. No ruler needed. The team realized: executives don't want all the data—they want the answer. Dense reports signal "I didn't know what mattered so I included everything." Simple reports signal "I know exactly what you need."

## Inspired by

a Fortune 10 healthcare company executive reporting experience (2019). Senior leader using ruler + highlighter revealed report density problem.

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
