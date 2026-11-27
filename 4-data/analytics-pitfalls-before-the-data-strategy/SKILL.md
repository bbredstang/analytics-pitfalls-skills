---
name: analytics-pitfalls-before-the-data-strategy
description: "Before the data strategy: 18 cards from Analytics Pitfalls & Principles, by Brian Cariveau, to check a data strategy, a data platform plan or a data roadmap."
license: CC-BY-4.0
---

# Before the data strategy

From Analytics Pitfalls & Principles, by Brian Cariveau: 18 cards and 4 frameworks for a data strategy, a data platform plan or a data roadmap. Every card, free: https://www.analyticspitfalls.com/library

## How to use it

Use it when someone shares or describes a data strategy, a data platform plan or a data roadmap, before it goes any further.

Walk it like a factory floor. Data comes in as raw material, goes down a line, and comes out as something people act on. Find the waste and get rid of it. Make what’s left stupidly simple.

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
- Which systems does the data come from, and how many in each area (three call systems, two websites)?
- What platform are you on, or moving to: Snowflake, Databricks, Fabric, BigQuery, something on premises?
- Who acts on the data today: people in a BI tool, analysts, data scientists, AI agents?
- What’s pushing this now: a migration, a new leader, an AI push, a number nobody trusts?

## The modeling standard

- **Credit where it’s due.** This stands on Bill Inmon (*Building the Data Warehouse*, the Corporate Information Factory) and Ralph Kimball (*The Data Warehouse Toolkit*, with Margy Ross). When you use one of their ideas, name them.
- **Inmon is gold’s definition.** He said a warehouse is subject-oriented, integrated, time-variant and nonvolatile. That’s a system-agnostic layer: organized by domain, every system as one with one definition, history kept, never overwritten.
- **Kimball is how people read it.** Facts and dimensions, a star schema, the grain declared before anything else, conformed dimensions everyone shares. That’s the aggregated and presentation layer on top of gold, and his conformed dimensions are your master data.
- **Most businesses need both.** They argued for decades. Your data needs the best of each: Inmon’s integrated core in gold, Kimball’s stars on top where the BI tools read. In a small, simple domain, gold can be the star.
- **Declare the grain first, in every layer past bronze.** One row per what, per when. Kimball’s first rule, and it goes in the name: `_daily`, `_per_call`.
- **Keep the history on purpose.** Say how each thing that changes is kept: overwritten, or a new row for each change with the dates it was true (Kimball’s slowly changing dimensions). Inmon’s time-variant is the same promise.
- **Kimball’s shapes, Brian’s names.** No `fact_` or `dim_` prefixes, no abbreviations. A table is named layer first in full words, `system_agnostic_support_calls_daily`. If a team wants the role in the name, spell it out: `fact`, `dimension`.
- **Not too hot, not too cold.** Over-modeled and nobody can query it. Under-modeled and everybody rebuilds it. The only test: does the model make the data easier to use, yes or no?

## Ask before you pick the shape

- **Don’t pick a format until you know these.** Ask the ones their work doesn’t already answer, three at a time at most, then recommend one shape and say why in a line.
- **Who, or what, reads it?** People in a BI tool, analysts writing SQL, data scientists, an AI agent, or an application.
- **How many systems feed this domain, and do they disagree?** One is silver. Several, with different rules, is gold, and that’s Inmon’s integration work.
- **What grain do people act at?** Per call, per customer per day, per claim line.
- **What changes over time, and do they need to see what it was before?**
- **Is there master data for the anchors** (customer, member, product, provider), or will this be the first?
- **What platform and tools?** Snowflake, Databricks, Fabric, BigQuery or something on premises; dbt or not; Power BI, Tableau or Looker on top.
- **Who keeps it running?** The team’s size and modeling skills. A shape they can’t keep up is the wrong shape.

## What the answers point to

- **People slicing numbers in a BI tool:** a Kimball star on top of gold, facts at a declared grain, dimensions joined to the master data. Power BI in particular is built for a star.
- **Many systems that have to agree:** Inmon’s integrated, normalized core in gold, one definition per thing, the stars built from it.
- **One system, told straight:** silver, at that system’s own grain, events or entities as the system has them, its codes in words.
- **Data scientists and AI agents:** one wide table per thing at one grain, every column in full words, every definition written down. Few joins, no lookups. An agent can only use what it can read.
- **An application that writes back:** normalized, so every fact lives in one place.
- **A small team:** the simplest shape that holds. Fewer, wider tables beat a model nobody can keep up.

## Brian Cariveau's questions

1. What raw data comes in, what comes off the line, and who acts on it? Name the data before you name the platform. From: A Logo Before the Data (`cards/a-logo-before-the-data.md`), The Analytics Assembly Line (`cards/analytics-assembly-line.md`), Manufacturing Mindset (`frameworks/manufacturing-mindset.md`).
2. Where’s the waste? Tables nobody’s touched in 90 days, columns pulled in just in case, copies of copies. Touch a table, take a table is how you end up with a hoarder’s warehouse. From: The 80% Warehouse (`cards/80-warehouse.md`), The Hoarder's Warehouse (`cards/hoarders-warehouse.md`), The Messy Garage (`cards/messy-garage.md`), Kill the Waste (`cards/kill-the-waste.md`).
3. Who inspects the raw materials before they go on the line? Clean, simple data beats sophisticated models on dirty data every single time. From: Garbage In, Powerhouse Out? (`cards/garbage-in-powerhouse-out.md`).
4. Is there one definition of each thing that matters? If Finance has a different number, the line is already making defects. From: The Wild West of Data (`cards/wild-west-of-data.md`).
5. Can people tell which data is good without asking someone? Rate it, promote one, retire the rest. From: Seven Versions of the Truth (`cards/seven-versions-of-the-truth.md`).
6. Would your grandmother understand the names? fact_trx_dtl_v3 is hieroglyphics, and bronze, silver and gold describe the plumbing, not what’s in it. And who keeps the names true? If it’s only your team, it’s already wrong. From: Database Hieroglyphics (`cards/database-hieroglyphics.md`), Bronze, Silver, Gold Means Nothing (`cards/bronze-silver-gold-means-nothing.md`), Crowdsource the Metadata (`cards/crowdsource-the-metadata.md`), Data Tables as Hieroglyphics (`frameworks/data-tables-as-hieroglyphics.md`), Medallion Architecture Disdain (`frameworks/medallion-architecture-disdain.md`).
7. Is it stupidly simple? A new hire should find their way around in a week, not six months. If someone’s drawing 412 boxes before anyone’s asked a question, stop. From: Everything Complex Can Seem Simple (`cards/everything-complex-can-seem-simple.md`), The Goldilocks Data Model (`cards/goldilocks-data-model.md`), Four Hundred and Twelve Boxes (`cards/four-hundred-and-twelve-boxes.md`).
8. Is each layer the right shape for what reads it? Inmon’s integrated core in gold, Kimball’s stars on top for the BI tools, wide and plainly named for the agents. Ask who reads it before you pick. From: The Goldilocks Data Model (`cards/goldilocks-data-model.md`), One System in a Gold Costume (`cards/one-system-in-a-gold-costume.md`).
9. Where’s the sensitive data, who can see it, and what will the agents read? Planned isn’t in stock. From: The Breach We Didn't See Coming (`cards/breach-we-didnt-see-coming.md`), Planned Isn't In Stock (`cards/planned-isnt-in-stock.md`).
10. Who has to change how they work for this data to be trusted, and what are they giving up? It was never about the tech. From: It Was Never About the Tech (`frameworks/it-was-never-about-the-tech.md`).
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
- An analyst who lives in the data every day
- Whoever owns security and privacy
- Whoever has to build and run it

## Where this fits

These run in order: the strategy, then the data, then the work, then the results.

1. **The strategy**: Before the AI strategy (`analytics-pitfalls-before-the-ai-strategy`), Before the data strategy (`analytics-pitfalls-before-the-data-strategy`), Before the BI strategy (`analytics-pitfalls-before-the-bi-strategy`). Pick the one you’re writing. They sit side by side; there’s no order between them. This one is here.
2. **The data**: The data layers (`analytics-pitfalls-data-layers`), Bronze, the cleaned raw layer (`analytics-pitfalls-bronze-cleaned-raw`), Silver, the system-specific layer (`analytics-pitfalls-silver-system-specific`), Gold, the system-agnostic layer (`analytics-pitfalls-gold-system-agnostic`). Start with the data layers, then bronze, silver and gold, in that order.
3. **The work**: Before the dashboard (`analytics-pitfalls-before-the-dashboard`). Once for each dashboard the strategy calls for.
4. **The results**: Before the readout (`analytics-pitfalls-before-the-readout`). When the first numbers go to leadership.

When you're done, say what comes next, by name: The data layers (`analytics-pitfalls-data-layers`). Start with the data layers, then bronze, silver and gold, in that order.

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
- **Bronze, Silver, Gold Means Nothing (When Layer Names Don't Help)** (`cards/bronze-silver-gold-means-nothing.md`): pitfall, Data Foundations. Name layers by what they contain, not how refined they are. Four layers cover almost every business: raw (exactly what the system sent), cleaned raw (the same data, formats fixed; most teams call it bronze), system-specific (one system at a time, in its domain; silver) and system-agnostic (every system in a domain, one definition; gold).
- **Crowdsource the Metadata (Stop Being the Bottleneck)** (`cards/crowdsource-the-metadata.md`): principle, Data Foundations. Let users document what they know. Wikipedia works because millions contribute, not because one team writes everything.
- **Everything Complex Can Seem Simple (The Art of Ruthless Simplification)** (`cards/everything-complex-can-seem-simple.md`): principle, Strategy & Focus. Relentlessly simplify. Every metric, model, and process—ask: "Can this be simpler?"
- **The Goldilocks Data Model (Too Hot, Too Cold, Never Just Right)** (`cards/goldilocks-data-model.md`): pitfall, Data Foundations. A data model has ONE job: make data easier to use for those crafting solutions with it—the BI analysts and data scientists.
- **Four Hundred and Twelve Boxes (Building the AI Ontology From the Top Down)** (`cards/four-hundred-and-twelve-boxes.md`): pitfall, Data Foundations. Simple for humans is simple for agents. Build the map one trusted domain at a time, in words a new hire would understand.
- **One System in a Gold Costume (When "All of It" Is Really the Biggest System)** (`cards/one-system-in-a-gold-costume.md`): pitfall, Data Foundations. System-agnostic means every system, one definition. Most teams call it gold. It's the layer the business, the dashboards and the AI agents read, so it has to be all of it, one way.
- **The Breach We Didn't See Coming (Until It Was Too Late)** (`cards/breach-we-didnt-see-coming.md`): pitfall, Data Foundations. Implement defense in depth: encryption at rest and in transit, role-based access controls (principle of least privilege), monitoring and auditing, regular security reviews.
- **Planned Isn't In Stock (When an Agent Reads Data Nobody Defined)** (`cards/planned-isnt-in-stock.md`): pitfall, Data Foundations. Customer-facing agents read only from defined, trusted data. If a word matters to the business, write down what it means before an agent acts on it. At work: "Just point the agent at the shared drive."

## The frameworks

- **Manufacturing Mindset** (`frameworks/manufacturing-mindset.md`): The Manufacturing Mindset treats data work as factory work — measuring throughput, cycle time, waste, and yield instead of counting deliverables.
- **Data Tables as Hieroglyphics** (`frameworks/data-tables-as-hieroglyphics.md`): Data Tables as Hieroglyphics is the argument that cryptic schema names like fact_trx_dtl_v3 are gatekeeping dressed up as rigor, not a technical necessity.
- **Medallion Architecture Disdain** (`frameworks/medallion-architecture-disdain.md`): Medallion Architecture Disdain argues that Bronze/Silver/Gold layer naming describes processing stage, not content — call it the Paint Department instead: raw, cleaned raw, system-specific and system-agnostic, names that tell you what is there.
- **It Was Never About the Tech** (`frameworks/it-was-never-about-the-tech.md`): It Was Never About the Tech is the observation that analytics transformations fail on politics, people, and principles far more often than on tooling — the technology is rarely the binding constraint.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
