---
name: analytics-pitfalls-hoarders-warehouse
description: "\"The Hoarder's Warehouse\" (Touch a Table, Take a Table): a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# The Hoarder's Warehouse (Touch a Table, Take a Table)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/28

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/28

## The problem

You hear it all the time from data engineers: "Touch a table, take a table." Sounds efficient, right? Just ingest the whole thing, every column, every row. Easy. Except now your data warehouse is a hoarder's nightmare. You've got 847 columns across 50 tables and nobody knows what 80% of them are. "customer_legacy_flag_2" sits there taking up space, covered in metaphorical cobwebs, never used in a single dashboard or analysis. But you're paying to store it. You're paying to process it. And worse—it's cluttering your shelves, making it harder for analysts to find what they actually need. It's like a manufacturing plant storing every scrap of raw material that ever entered the building "just in case." Meanwhile, the useful materials are buried under junk and workers waste hours digging through garbage to find what they need.

## The principle

Be ruthlessly focused: only pull in columns you'll actually use for the current use case. Yes, this requires thinking upfront. Yes, it's harder than "take everything." But it's the manufacturing mindset—you don't stock raw materials you don't have orders for. Before ingesting a table, ask: "Which specific columns will we use in reports, dashboards, or models?" Pull those. Document why. Then design your layers (raw → cleaned raw → system-specific → system-agnostic) so adding columns later is trivial when they're truly needed. And "needed" means "will be used," not "might be useful someday." The 80/20 rule applies: 80% of columns never get used. Don't pay to store, process, and maintain them. The magic happens when your data warehouse is clean, focused, and every column has a purpose. Analysts find what they need in seconds instead of minutes. Costs drop. Speed increases. Less is more.

## The steps

1. Audit Column Usage: Query your data warehouse. Which columns get used in joins, reports, models? Flag anything unused in 12 months for deletion.
2. Implement Pull-Only-What-You-Need: Before ingesting a table, list specific columns you'll use. Pull those. Document why. Build a process to add columns when truly needed.
3. Track Storage Costs: Monitor what data costs to store and process. Set a target to reduce costs 20% this quarter by removing waste. Celebrate savings.

## In practice

A financial services company had a "customers" table with 247 columns ingested from their CRM. Data team followed "touch a table, take a table." Storage costs: $18K/month. Query time: 8-12 seconds average. Analyst onboarding: 4 months to understand what columns meant. New data leader audited usage: 198 columns (80%) had ZERO joins to any downstream table in 12 months. Never used. Ever. They rebuilt: only ingested 49 essential columns (name, ID, contact info, key account details, product ownership). Documented each one. Built a process: "Need a new column? Submit request with use case, we add it in 2 days." Storage costs dropped to $4K/month (78% reduction). Query time: 2 seconds average (75% faster). Analyst onboarding: 3 weeks instead of 4 months. And here's the kicker—in the next year, only 7 additional columns were requested and added. Turns out they didn't need 247 columns. They needed 56. The other 191 were waste—pure warehouse clutter that cost money and slowed everyone down.

Whenever the work is a table, a data model or a layer past cleaned raw, and whenever you're the one designing it, hold it to the modeling standard, and ask what it needs to know before you pick a shape.

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

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
