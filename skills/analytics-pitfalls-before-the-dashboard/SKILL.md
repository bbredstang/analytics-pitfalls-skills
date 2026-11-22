---
name: analytics-pitfalls-before-the-dashboard
description: "Before the dashboard: 11 cards from Analytics Pitfalls & Principles, by Brian Cariveau, to check a dashboard request or a draft dashboard."
license: CC-BY-4.0
---

# Before the dashboard

From Analytics Pitfalls & Principles, by Brian Cariveau: 11 cards and 2 frameworks for a dashboard request or a draft dashboard. Every card, free: https://www.analyticspitfalls.com/library

## How to use it

Use it when someone shares or describes a dashboard request or a draft dashboard, before it goes any further.

1. Take Brian Cariveau's questions below in order, against their actual work, and ask them in his words rather than your own. For each, open the files it names and answer from them.
2. Skip a question the work already answers well. Say so in a line and move on.
3. Then pick the one or two cards that matter most for this work, say why in a sentence each, and give their principles in the cards' own words. Never hand someone the whole list.
4. Say the work looks like a pitfall; never tell someone they have it. If nothing fits, say so.
5. Finish with the links of the cards you used, and say which skill comes next (Where this fits, below).

## Brian Cariveau's questions

1. What action will someone take when they see it? Name the person and the action. If nobody can, don’t build it. From: The Sexy Map Trap (`cards/sexy-map-trap.md`), Story First, Data Second (`cards/story-first-data-second.md`).
2. Is there already a dashboard for this, and would one number do the job? If you’re adding one, kill one nobody uses. From: Death by Dashboard (`cards/death-by-dashboard.md`), Sometimes Just Use the Number (`cards/sometimes-just-use-the-number.md`).
3. Has anyone reacted to a sketch yet? Build the picture first. Nobody gets excited approving a bullet point. From: Build the Picture First (`cards/build-the-picture-first.md`), Build That! (`frameworks/build-that.md`).
4. Will they act on it right there, or export it to Excel and act somewhere else? If it’s the export, ask why. From: The Data Export Trap (`cards/data-export-trap.md`).
5. How will you know it’s used? Usage is the receipt. Set the date it goes if nobody opens it. From: Usage Is the Receipt (`frameworks/usage-is-the-receipt.md`).
6. If there’s a draft, does every pixel earn its place? Pie charts are for Thanksgiving. No 3D, no decoration, no map just because you can, and nothing an executive needs a ruler and a highlighter to read. From: Pie Charts Are for Thanksgiving (`cards/pie-charts-are-for-thanksgiving.md`), The Data Ink Ratio (`cards/data-ink-ratio.md`), The Sexy Map Trap (`cards/sexy-map-trap.md`), The Ruler and Highlighter Test (`cards/ruler-and-highlighter-test.md`).
7. If AI builds the reports now, does each one change what someone does? Or is it the old report, faster? From: Faster at the Old Way (`cards/faster-at-the-old-way.md`).
8. Who has to work differently for this to get used, and what are they giving up? The dashboard is the easy part. From: We're in the Behavior Change Business (`cards/were-in-the-behavior-change-business.md`).

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
