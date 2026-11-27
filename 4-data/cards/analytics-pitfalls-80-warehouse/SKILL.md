---
name: analytics-pitfalls-80-warehouse
description: "\"The 80% Warehouse\" (When Most of Your Data Just Sits There): a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# The 80% Warehouse (When Most of Your Data Just Sits There)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/60

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/60

## The problem

Your data warehouse has 847 tables. You're proud of it—years of work, terabytes of data, every system integrated. Then you check usage analytics: 680 tables haven't been queried in 90+ days. That's 80% of your warehouse sitting unused. Like a manufacturing plant with a giant warehouse where 80% of inventory just gathers dust—never moving to production, never creating value. Worse: you're paying to store it, maintain it, back it up, and document it. Every new table you add makes the problem worse. Users can't find what they need because they're drowning in unused tables. Your warehouse isn't an asset—it's a graveyard consuming resources.

## The principle

Track data usage like inventory turnover. Manufacturing plants obsess over "inventory turns"—how fast raw materials move through the system. If something sits >90 days, they investigate: Why isn't this moving? Should we stop ordering it? Same with data. Instrument your warehouse: track queries per table, last access date, who uses what. Set a rule: Tables unused for 90 days get flagged for review. At 180 days with zero usage, they get archived or deleted. The magic happens when you treat data like physical inventory—if it's not moving, it's waste. Build for 80% usage rate (only 20% unused at any time), not 20% usage rate (80% waste).

## The steps

1. **Instrument Your Data Warehouse**

Track for every table:
- Last query date
- Queries per day/week/month
- Distinct users querying it
- Rows actually read (not just table scanned)

Build a simple dashboard:
- Tables by days since last use
- Usage rate % (tables used in last 90 days)
- Storage cost by usage tier

Goal: Know exactly which 80% of your data is waste.
2. **Implement Usage-Based Lifecycle**

Create usage tiers:
- **Active**: Used in last 30 days (keep as-is)
- **Stale**: 30-90 days unused (yellow flag, notify owners)
- **Expired**: 90-180 days unused (red flag, archive candidate)
- **Dead**: 180+ days unused (archive immediately)

Monthly review: Archive or delete tables in Expired/Dead tiers.

Exception process: If owner makes case for keeping unused table, they must commit to using it within 30 days or it gets archived.
3. **Measure Inventory Turns**

Calculate warehouse health metrics:
- **Usage rate**: % of tables queried in last 90 days (target: 80%+)
- **Storage efficiency**: GB used ÷ GB total (target: 70%+)
- **Data debt**: # of tables ×  days since last use (target: declining)

Track monthly. Set goal: 80% usage rate within 6 months.

Celebrate wins: "We archived 200 unused tables this quarter and nobody noticed!"

Bonus: New tables require usage projections. If not used within 90 days of launch, they're candidates for immediate deletion.

## In practice

A Fortune 5 healthcare company's data team had 1,200+ tables in their enterprise warehouse. Data engineers were proud of the coverage. Then new VP asked: "What's our data usage rate?" They instrumented the warehouse: tracked every query, every table access. Results were brutal: 73% of tables had zero queries in the past 90 days. 897 tables completely unused. Storage cost: $180K/year just for unused data. Maintenance burden: engineers spent 40% of time supporting tables nobody used. They implemented a usage-based lifecycle: Yellow flag at 60 days unused, Red flag at 90 days, Archive at 120 days unused. First pass: archived 520 tables (43% of warehouse). Users didn't notice—because nobody was using them anyway. Six months later: warehouse down to 420 tables, usage rate at 82%, storage costs cut 60%, engineers focused on high-value work. The warehouse went from graveyard to efficient inventory system.

## Inspired by

Manufacturing inventory management principles. a Fortune 10 healthcare company's data warehouse usage analysis. The "80% unused" statistic from Walk the Catwalk presentation.

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
