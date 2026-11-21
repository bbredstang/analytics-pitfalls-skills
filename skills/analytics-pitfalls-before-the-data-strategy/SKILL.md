---
name: analytics-pitfalls-before-the-data-strategy
description: "Before the data strategy: 17 cards from Analytics Pitfalls & Principles, by Brian Cariveau, to check a data strategy, a data platform plan or a data roadmap."
license: CC-BY-4.0
---

# Before the data strategy

From Analytics Pitfalls & Principles, by Brian Cariveau: 17 cards and 4 frameworks for a data strategy, a data platform plan or a data roadmap. Every card, free: https://www.analyticspitfalls.com/library

## How to use it

Use it when someone shares or describes a data strategy, a data platform plan or a data roadmap, before it goes any further.

Walk it like a factory floor. Data comes in as raw material, goes down a line, and comes out as something people act on. Find the waste and get rid of it. Make what’s left stupidly simple.

1. Take Brian Cariveau's questions below in order, against their actual work, and ask them in his words rather than your own. For each, open the files it names and answer from them.
2. Hold every answer to the lens above.
3. Skip a question the work already answers well. Say so in a line and move on.
4. Then pick the one or two cards that matter most for this work, say why in a sentence each, and give their principles in the cards' own words. Never hand someone the whole list.
5. Say the work looks like a pitfall; never tell someone they have it. If nothing fits, say so.
6. Then put it on the canvas, and offer the board (below).
7. Finish with the links of the cards you used, and say which skill comes next (Where this fits, below).

## Brian Cariveau's questions

1. What raw data comes in, what comes off the line, and who acts on it? Name the data before you name the platform. From: A Logo Before the Data (`cards/a-logo-before-the-data.md`), The Analytics Assembly Line (`cards/analytics-assembly-line.md`), Manufacturing Mindset (`frameworks/manufacturing-mindset.md`).
2. Where’s the waste? Tables nobody’s touched in 90 days, columns pulled in just in case, copies of copies. Touch a table, take a table is how you end up with a hoarder’s warehouse. From: The 80% Warehouse (`cards/80-warehouse.md`), The Hoarder's Warehouse (`cards/hoarders-warehouse.md`), The Messy Garage (`cards/messy-garage.md`), Kill the Waste (`cards/kill-the-waste.md`).
3. Who inspects the raw materials before they go on the line? Clean, simple data beats sophisticated models on dirty data every single time. From: Garbage In, Powerhouse Out? (`cards/garbage-in-powerhouse-out.md`).
4. Is there one definition of each thing that matters? If Finance has a different number, the line is already making defects. From: The Wild West of Data (`cards/wild-west-of-data.md`).
5. Can people tell which data is good without asking someone? Rate it, promote one, retire the rest. From: Seven Versions of the Truth (`cards/seven-versions-of-the-truth.md`).
6. Would your grandmother understand the names? fact_trx_dtl_v3 is hieroglyphics, and bronze, silver and gold describe the plumbing, not what’s in it. And who keeps the names true? If it’s only your team, it’s already wrong. From: Database Hieroglyphics (`cards/database-hieroglyphics.md`), Bronze, Silver, Gold Means Nothing (`cards/bronze-silver-gold-means-nothing.md`), Crowdsource the Metadata (`cards/crowdsource-the-metadata.md`), Data Tables as Hieroglyphics (`frameworks/data-tables-as-hieroglyphics.md`), Medallion Architecture Disdain (`frameworks/medallion-architecture-disdain.md`).
7. Is it stupidly simple? A new hire should find their way around in a week, not six months. If someone’s drawing 412 boxes before anyone’s asked a question, stop. From: Everything Complex Can Seem Simple (`cards/everything-complex-can-seem-simple.md`), The Goldilocks Data Model (`cards/goldilocks-data-model.md`), Four Hundred and Twelve Boxes (`cards/four-hundred-and-twelve-boxes.md`).
8. Where’s the sensitive data, who can see it, and what will the agents read? Planned isn’t in stock. From: The Breach We Didn't See Coming (`cards/breach-we-didnt-see-coming.md`), Planned Isn't In Stock (`cards/planned-isnt-in-stock.md`).
9. Who has to change how they work for this data to be trusted, and what are they giving up? It was never about the tech. From: It Was Never About the Tech (`frameworks/it-was-never-about-the-tech.md`).
10. Who’s on your board? Before this goes to anyone, convene a few people who’d poke holes in it, and hear them out now. It’s a lot cheaper than hearing it later.

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
- An analyst who lives in the data every day
- Whoever owns security and privacy
- Whoever has to build and run it

## Where this fits

These run in order: the strategy, then the work, then the results.

1. **The strategy**: Before the AI strategy (`analytics-pitfalls-before-the-ai-strategy`), Before the data strategy (`analytics-pitfalls-before-the-data-strategy`), Before the BI strategy (`analytics-pitfalls-before-the-bi-strategy`). Pick the one you’re writing. They sit side by side; there’s no order between them. This one is here.
2. **The work**: Before the dashboard (`analytics-pitfalls-before-the-dashboard`). Once for each dashboard the strategy calls for.
3. **The results**: Before the readout (`analytics-pitfalls-before-the-readout`). When the first numbers go to leadership.

When you're done, say what comes next, by name: Before the dashboard (`analytics-pitfalls-before-the-dashboard`). Once for each dashboard the strategy calls for.

## The cards

- **A Logo Before the Data (When the Platform Is Really a Query)** (`cards/a-logo-before-the-data.md`): pitfall, Strategy & Focus. Name the data before you name the platform. Most big asks are a few kinds of data and one question nobody asked: joined around what?
- **The Analytics Assembly Line (Why Your Data is Just Raw Materials)** (`cards/analytics-assembly-line.md`): principle, Delivery & Execution. Treat your data ecosystem like a clean manufacturing line with zero waste. Raw materials (data) enter on the left—inspect for quality, reject defects.
- **The 80% Warehouse (When Most of Your Data Just Sits There)** (`cards/80-warehouse.md`): pitfall, Data Foundations. Track data usage like inventory turnover. Manufacturing plants obsess over "inventory turns"—how fast raw materials move through the system.
- **The Hoarder's Warehouse (Touch a Table, Take a Table)** (`cards/hoarders-warehouse.md`): pitfall, Data Foundations. Be ruthlessly focused: only pull in columns you'll actually use for the current use case.
- **The Messy Garage (When Clutter Holds You Back)** (`cards/messy-garage.md`): pitfall, Data Foundations. Clean the garage. Manufacturing plants run "5S" programs (Sort, Set in order, Shine, Standardize, Sustain)—regular cleanup cycles to eliminate waste.
- **Kill the Waste (The Lean Analytics Playbook)** (`cards/kill-the-waste.md`): principle, Delivery & Execution. Adopt a lean manufacturing mindset: identify waste, eliminate it ruthlessly, free up capacity for value creation.
- **Garbage In, Powerhouse Out? (Nope.)** (`cards/garbage-in-powerhouse-out.md`): pitfall, Data Foundations. Clean, simple data beats sophisticated models on dirty data every single time. Treat data quality like you'd treat raw materials in manufacturing—inspect, validate, reject defects before they enter the line.
- **The Wild West of Data (When Everyone Does Whatever They Want)** (`cards/wild-west-of-data.md`): pitfall, Data Foundations. Set clear rules and enforce them. Define metrics once, centrally, and make that the source of truth. At work: "Finance has a different number."
- **Seven Versions of the Truth (When Nobody Can Say Which Data Is Good)** (`cards/seven-versions-of-the-truth.md`): pitfall, Data Foundations. Rate your data, promote one, retire the rest. Every domain needs one data product people can trust without asking, and a rating that says how far to trust it.
- **Database Hieroglyphics (When Nobody Can Read Your Schema)** (`cards/database-hieroglyphics.md`): pitfall, Data Foundations. Name everything like you're explaining it to your grandmother—clear, complete, obvious. At work: "What does fact_trx_dtl_v3 even mean?"
- **Bronze, Silver, Gold Means Nothing (When Layer Names Don't Help)** (`cards/bronze-silver-gold-means-nothing.md`): pitfall, Data Foundations. Name layers by what they contain, not processing stage. Use names that self-document: Raw (exactly as source systems sent it), Curated_SystemName (cleaned, usable, still system-specific), Integrated_TopicName (cross-system, business-ready).
- **Crowdsource the Metadata (Stop Being the Bottleneck)** (`cards/crowdsource-the-metadata.md`): principle, Data Foundations. Let users document what they know. Wikipedia works because millions contribute, not because one team writes everything.
- **Everything Complex Can Seem Simple (The Art of Ruthless Simplification)** (`cards/everything-complex-can-seem-simple.md`): principle, Strategy & Focus. Relentlessly simplify. Every metric, model, and process—ask: "Can this be simpler?"
- **The Goldilocks Data Model (Too Hot, Too Cold, Never Just Right)** (`cards/goldilocks-data-model.md`): pitfall, Data Foundations. A data model has ONE job: make data easier to use for those crafting solutions with it—the BI analysts and data scientists.
- **Four Hundred and Twelve Boxes (Building the AI Ontology From the Top Down)** (`cards/four-hundred-and-twelve-boxes.md`): pitfall, Data Foundations. Simple for humans is simple for agents. Build the map one trusted domain at a time, in words a new hire would understand.
- **The Breach We Didn't See Coming (Until It Was Too Late)** (`cards/breach-we-didnt-see-coming.md`): pitfall, Data Foundations. Implement defense in depth: encryption at rest and in transit, role-based access controls (principle of least privilege), monitoring and auditing, regular security reviews.
- **Planned Isn't In Stock (When an Agent Reads Data Nobody Defined)** (`cards/planned-isnt-in-stock.md`): pitfall, Data Foundations. Customer-facing agents read only from defined, trusted data. If a word matters to the business, write down what it means before an agent acts on it. At work: "Just point the agent at the shared drive."

## The frameworks

- **Manufacturing Mindset** (`frameworks/manufacturing-mindset.md`): The Manufacturing Mindset treats data work as factory work — measuring throughput, cycle time, waste, and yield instead of counting deliverables.
- **Data Tables as Hieroglyphics** (`frameworks/data-tables-as-hieroglyphics.md`): Data Tables as Hieroglyphics is the argument that cryptic schema names like fact_trx_dtl_v3 are gatekeeping dressed up as rigor, not a technical necessity.
- **Medallion Architecture Disdain** (`frameworks/medallion-architecture-disdain.md`): Medallion Architecture Disdain argues that Bronze/Silver/Gold layer naming describes processing stage, not content — call it the Paint Department instead, a name that tells you what happens there.
- **It Was Never About the Tech** (`frameworks/it-was-never-about-the-tech.md`): It Was Never About the Tech is the observation that analytics transformations fail on politics, people, and principles far more often than on tooling — the technology is rarely the binding constraint.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
