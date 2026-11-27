---
name: analytics-pitfalls-silver-system-specific
description: "Silver, the system-specific layer: 7 cards from Analytics Pitfalls & Principles, by Brian Cariveau, to check a silver or system-specific layer, one system at a time."
license: CC-BY-4.0
---

# Silver, the system-specific layer

From Analytics Pitfalls & Principles, by Brian Cariveau: 7 cards and 2 frameworks for a silver or system-specific layer, one system at a time. Every card, free: https://www.analyticspitfalls.com/library

## How to use it

Use it when someone shares or describes a silver or system-specific layer, one system at a time, before it goes any further.

One system, told straight. If you have three call systems, you have three silver tables, and each one says exactly what that system says, in plain words. This is where you go for one website, one app, one portal, one claims system. Before you put systems together, you have to be able to see each one alone.

1. First, get their situation (below), so everything after fits their company, not a generic one.
2. Take Brian Cariveau's questions below in order, against their actual work, and ask them in his words rather than your own. For each, open the files it names and answer from them.
3. Hold every answer to the lens above.
4. Hold the work to Brian Cariveau's standard (the sections before the questions). Where it falls short, say where, in his words.
5. Skip a question the work already answers well. Say so in a line and move on.
6. Then pick the one or two cards that matter most for this work, say why in a sentence each, and give their principles in the cards' own words. Never hand someone the whole list.
7. Say the work looks like a pitfall; never tell someone they have it. If nothing fits, say so.
8. Then list the systems in each domain still missing their own silver table, and the silver tables below three stars.
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

- Which system is this, and which data area is it in?
- Who runs the system, and who knows its rules?
- Who, or what, reads this layer: analysts, a migration team, the gold layer, an agent?
- What platform and tools: Snowflake, Databricks, Fabric, BigQuery; dbt or not?

## What belongs in silver

- **One system per table, in its domain.** Support for the call systems, Digital for the websites and portals, Financial for the ledgers, then Claims, Clinical, Marketing. Domain, then subdomain, then use case.
- **That system’s business rules, written down.** What counts as a completed call in this system. What counts as a session on this website. Each rule in one place, with an owner.
- **Codes turned into words.** Status 7 becomes “transferred.” Disposition “CB” becomes “callback requested.” Open the table and read it, no lookup needed.
- **The system’s own things, at a stated grain.** Calls, agents, queues. Sessions, pages, visitors. Claims, lines, payments. One row per what, per when, and the grain in the name: `_daily`, `_per_call`.
- **Keys to the master data.** Every customer, member, provider or product maps to the master record with standard keys. Keep the system’s own ID beside it.
- **Names in full words.** `system_specific_support_east_call_system_calls_daily`, with columns like `call_disposition` and `agent_name`. Little to no abbreviations: stupidly simple for humans is stupidly simple for agents.
- **Built for one system’s people.** Running that system, moving off it, checking back to the source. They live here.

## What never happens in silver

- **No mixing systems.** The second you put two call systems in one table, you’re in gold.
- **No company-wide definition forced onto one system.** Where the company’s definition differs from this system’s, that gets worked out in gold, in the open.
- **No format fixing.** If you’re still fixing dates here, bronze isn’t doing its job.

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

1. Can you see each system on its own? If the only place the east call system shows up is blended into everything else, nobody can tell what it said, or catch it when it breaks. From: The Blender (`cards/blender.md`).
2. Which domain is it in, and is that obvious from the name? From: Bronze, Silver, Gold Means Nothing (`cards/bronze-silver-gold-means-nothing.md`).
3. Are this system’s rules written down, in one place, with an owner? Or do they live in someone’s head and twelve dashboards? From: The Wild West of Data (`cards/wild-west-of-data.md`).
4. Open the table. Are the codes in words, and the names in full words? Would a new analyst, or an agent, know what status 7 means without a lookup? From: Database Hieroglyphics (`cards/database-hieroglyphics.md`), Data Tables as Hieroglyphics (`frameworks/data-tables-as-hieroglyphics.md`).
5. What’s the grain? One row per what, per when, declared first, the way Kimball says? Not too hot, not too cold: does the model make the data easier to use, yes or no? From: The Goldilocks Data Model (`cards/goldilocks-data-model.md`).
6. Does every customer, member or product join to the master data with standard keys? If it’s email in one place and a vendor ID in another, it’s not three stars. From: Seven Versions of the Truth (`cards/seven-versions-of-the-truth.md`).
7. How many stars? Documented, tested, owned and joined to the master data is three. Three stars is the line. From: Seven Versions of the Truth (`cards/seven-versions-of-the-truth.md`).
8. Is anyone actually using it? Data products from the logs, not a form. If nobody’s queried it in 90 days, it goes on the retire list. From: Seven Versions of the Truth (`cards/seven-versions-of-the-truth.md`), The 80% Warehouse (`cards/80-warehouse.md`).
9. Whose system is it? The people who run each system have to own its rules and admit where its data is messy. That’s a conversation, not a pipeline. It was never about the tech. From: It Was Never About the Tech (`frameworks/it-was-never-about-the-tech.md`).

## Where this fits

These run in order: the strategy, then the data, then the work, then the results.

1. **The strategy**: Before the AI strategy (`analytics-pitfalls-before-the-ai-strategy`), Before the data strategy (`analytics-pitfalls-before-the-data-strategy`), Before the BI strategy (`analytics-pitfalls-before-the-bi-strategy`). Pick the one you’re writing. They sit side by side; there’s no order between them.
2. **The data**: The data layers (`analytics-pitfalls-data-layers`), Bronze, the cleaned raw layer (`analytics-pitfalls-bronze-cleaned-raw`), Silver, the system-specific layer (`analytics-pitfalls-silver-system-specific`), Gold, the system-agnostic layer (`analytics-pitfalls-gold-system-agnostic`). Start with the data layers, then bronze, silver and gold, in that order. This one is here.
3. **The work**: Before the dashboard (`analytics-pitfalls-before-the-dashboard`). Once for each dashboard the strategy calls for.
4. **The results**: Before the readout (`analytics-pitfalls-before-the-readout`). When the first numbers go to leadership.

When you're done, say what comes next, by name: Gold, the system-agnostic layer (`analytics-pitfalls-gold-system-agnostic`). Start with the data layers, then bronze, silver and gold, in that order.

## The cards

- **The Blender (When Systems Get Mixed Before Anyone Knows What Each One Says)** (`cards/blender.md`): pitfall, Data Foundations. See each system alone before you put them together. Give every source system its own layer, one system at a time, in its domain: one call system, one website, one portal, one claims system.
- **Bronze, Silver, Gold Means Nothing (When Layer Names Don't Help)** (`cards/bronze-silver-gold-means-nothing.md`): pitfall, Data Foundations. Name layers by what they contain, not how refined they are. Four layers cover almost every business: raw (exactly what the system sent), cleaned raw (the same data, formats fixed; most teams call it bronze), system-specific (one system at a time, in its domain; silver) and system-agnostic (every system in a domain, one definition; gold).
- **The Wild West of Data (When Everyone Does Whatever They Want)** (`cards/wild-west-of-data.md`): pitfall, Data Foundations. Set clear rules and enforce them. Define metrics once, centrally, and make that the source of truth. At work: "Finance has a different number."
- **Database Hieroglyphics (When Nobody Can Read Your Schema)** (`cards/database-hieroglyphics.md`): pitfall, Data Foundations. Name everything like you're explaining it to your grandmother—clear, complete, obvious. At work: "What does fact_trx_dtl_v3 even mean?"
- **The Goldilocks Data Model (Too Hot, Too Cold, Never Just Right)** (`cards/goldilocks-data-model.md`): pitfall, Data Foundations. A data model has ONE job: make data easier to use for those crafting solutions with it—the BI analysts and data scientists.
- **Seven Versions of the Truth (When Nobody Can Say Which Data Is Good)** (`cards/seven-versions-of-the-truth.md`): pitfall, Data Foundations. Rate your data, promote one, retire the rest. Every domain needs one data product people can trust without asking, and a rating that says how far to trust it.
- **The 80% Warehouse (When Most of Your Data Just Sits There)** (`cards/80-warehouse.md`): pitfall, Data Foundations. Track data usage like inventory turnover. Manufacturing plants obsess over "inventory turns"—how fast raw materials move through the system.

## The frameworks

- **Data Tables as Hieroglyphics** (`frameworks/data-tables-as-hieroglyphics.md`): Data Tables as Hieroglyphics is the argument that cryptic schema names like fact_trx_dtl_v3 are gatekeeping dressed up as rigor, not a technical necessity.
- **It Was Never About the Tech** (`frameworks/it-was-never-about-the-tech.md`): It Was Never About the Tech is the observation that analytics transformations fail on politics, people, and principles far more often than on tooling — the technology is rarely the binding constraint.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
