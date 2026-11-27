---
name: analytics-pitfalls-medallion-architecture-disdain
description: "The \"Medallion Architecture Disdain\" framework from Analytics Pitfalls & Principles, by Brian Cariveau, as a lens on analytics and AI work."
license: CC-BY-4.0
---

# Medallion Architecture Disdain

A framework from Analytics Pitfalls & Principles, by Brian Cariveau.
https://www.analyticspitfalls.com/frameworks/medallion-architecture-disdain

## How to use this framework

Use it as a lens when someone's analytics or AI work touches what it describes.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Say which framework you are using and what it asks, in its one-line definition below.
3. Hold their work up to it: where it already fits, and where it does not. Be specific to their situation.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If one of the cards below names their problem more exactly, use that card as it says.
6. Finish with the framework's link: https://www.analyticspitfalls.com/frameworks/medallion-architecture-disdain

> Medallion Architecture Disdain argues that Bronze/Silver/Gold layer naming describes processing stage, not content — call it the Paint Department instead: raw, cleaned raw, system-specific and system-agnostic, names that tell you what is there.

## The problem hiding behind a tidy diagram

Bronze, Silver, and Gold sounds sophisticated on an architecture slide. It falls apart the moment a new analyst asks where customer data lives and gets sent to the Gold layer, where fourteen different tables have "customer" somewhere in the name and three different colleagues give three different answers about which one is actually correct. It turns out the real customer table lives in Silver, because Gold was never finished — a detail nobody wrote down anywhere, because the naming convention never asked anyone to.

Ask five teams what "silver" means and you'll get five answers. Metal-tier names describe processing stage: how refined the data is. They say nothing about content: what the data actually is. That distinction sounds academic until you watch a new hire lose their first two weeks just learning which layer holds what, purely because the labels were optimized to look organized in a diagram rather than to help a human find something.


## Name it like a hardware store, not a metallurgy chart

Replace processing-tier names with content-based ones. Four layers cover almost every business. Raw: exactly what the source system sent. Cleaned raw, where most teams put bronze: the same rows, with dates, time zones, money and codes in one standard format. System-specific, where silver usually sits: one system at a time, in its domain, so one call system, one website, one claims system. System-agnostic, the real gold: every system in a domain as one, with one definition, tied to the master data. Name tables layer first, then domain, system, thing and grain, in full words: system_specific_support_east_call_system_calls_daily, system_agnostic_support_calls_daily. Every name now answers "what's in here" on its own, without a meeting.

Little to no abbreviations, in every layer. Someone who opens the database should be able to read it without a lookup. Stupidly simple for humans is stupidly simple for agents: an AI reads the same names you do.

The test for whether this is working: ask five analysts where they'd look for a specific kind of data, with no documentation open. If they can guess correctly from the name alone, the naming succeeded. If they need to ask someone, it failed — no matter how elegant the underlying architecture is.


## It's a rename, not a rebuild

This is the quietly appealing part: the underlying architecture usually does not need to change at all. Same pipelines, same processing logic, same infrastructure — just names that tell a person what they will find instead of how far along the pipeline it traveled to get there. Teams that make this switch report onboarding time and "where's this data" support tickets both dropping substantially, without touching a single ETL job.


## Where to start

Audit whatever your current layer or zone names are, and be honest about whether a new hire could guess what's inside each one. If the answer is no, pick a content-based convention, apply it to your most-used tables first, and treat any newly built table that doesn't follow it as a code review rejection.


## Cards that go with it

- **Bronze, Silver, Gold Means Nothing (When Layer Names Don't Help)** (`cards/bronze-silver-gold-means-nothing.md`), https://www.analyticspitfalls.com/cards/61
- **Cleaning the Same Dates Every Morning (When Every Query Fixes Raw Data Again)** (`cards/cleaning-the-same-dates-every-morning.md`), https://www.analyticspitfalls.com/cards/86
- **The Blender (When Systems Get Mixed Before Anyone Knows What Each One Says)** (`cards/blender.md`), https://www.analyticspitfalls.com/cards/87
- **One System in a Gold Costume (When "All of It" Is Really the Biggest System)** (`cards/one-system-in-a-gold-costume.md`), https://www.analyticspitfalls.com/cards/88

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
