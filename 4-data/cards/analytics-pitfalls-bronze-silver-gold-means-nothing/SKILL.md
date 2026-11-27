---
name: analytics-pitfalls-bronze-silver-gold-means-nothing
description: "\"Bronze, Silver, Gold Means Nothing\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# Bronze, Silver, Gold Means Nothing (When Layer Names Don't Help)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/61

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/61

## The problem

Your data lake has three layers: Bronze, Silver, Gold. Sounds sophisticated. Ask five teams what silver means and you'll get five answers. One team's bronze is raw, another's is cleaned, and one team's silver is the next team's gold. Then new analyst joins: "Where's customer data?" Answer: "Check Gold layer." They search. Find 14 tables with "customer" in the name. Which one is right? No idea. They ask 3 people, get 3 different answers. Turns out the "right" customer table is actually in Silver because Gold was never finished. Bronze/Silver/Gold tells you nothing about what's inside. It's like Home Depot organizing by "Bronze aisle," "Silver aisle," "Gold aisle" instead of "Paint," "Tools," "Lumber." Users need to understand what data IS, not what processing tier it's in. Metal names are architecture porn—they make engineers feel organized but leave users lost.

## The principle

Name layers by what they contain, not how refined they are. Four layers cover almost every business: raw (exactly what the system sent), cleaned raw (the same data, formats fixed; most teams call it bronze), system-specific (one system at a time, in its domain; silver) and system-agnostic (every system in a domain, one definition; gold). Examples: raw_support_east_call_system_calls, system_specific_support_east_call_system_calls_daily, system_agnostic_support_calls_daily. Every name tells you what's inside, in full words, with little to no abbreviations. The magic happens when a new analyst, or an agent, can open the database and guess where data lives without asking anyone. Think retail: you find paint in the Paint department, not the Silver aisle.

## The steps

1. **Audit Your Current Naming**

List all your data layer/zone names:
- What are they called?
- Can a new user guess what's in each layer from the name?

Test: Ask 5 analysts: "Where would you look for customer data?"

If they can't answer without documentation, your names failed.

Common bad patterns:
- Bronze/Silver/Gold (processing stage, not content)
- Stage1/Stage2/Stage3 (meaningless)
- Raw/Cleaned/Final (still doesn't say what's inside)
2. **Rename Using Content-Based Pattern**

Adopt four layers, named for what they hold:
- **raw_**: Data exactly as the source sent it
- **cleaned_raw_**: Same rows, formats fixed (dates, time zones, money, codes)
- **system_specific_**: One system at a time, in its domain (system_specific_support_east_call_system_calls_daily)
- **system_agnostic_**: Every system in a domain, one definition (system_agnostic_support_calls_daily)

Every name answers: "What's in here?"

Create migration plan: Start with most-used tables, rename gradually.

Update all docs, queries, dashboards to use new names.
3. **Self-Documenting Standards**

Create naming standards guide:
- Layer first: raw, cleaned_raw, system_specific, system_agnostic
- Then domain, system, thing and grain, in full words
- Little to no abbreviations, in table and column names

Example: system_agnostic_support_calls_daily vs system_agnostic_support_calls_monthly

Test with new hires: Can they find data without help?

Goal: 80%+ of "where's X data?" questions answered by naming alone.

Bonus: Every new table must follow naming standard or gets rejected in code review.

## In practice

A financial services firm had Bronze/Silver/Gold lake architecture. Beautiful in PowerPoint. Nightmare in practice. New data scientists spent first 2 weeks just learning "which layer has what." Onboarding took 6 weeks because nobody could find data. They renamed every layer for what it held: raw, cleaned raw, system-specific (one loan system at a time) and system-agnostic (every loan system as one), with every table named in full words. Every name self-documented. New analyst question: "Where's loan data?" Answer obvious: system_agnostic_lending_loans_daily. Onboarding dropped from 6 weeks to 1 week. Support tickets about "where's X data" dropped 71%. Bonus: Documentation became less critical because names explained themselves. The architecture didn't change—just the names. But user experience transformed overnight.

## Inspired by

Home Depot/library organization analogy from Data Strategy 2023. The problem with abstract layer names that don't communicate content.

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
