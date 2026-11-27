---
name: analytics-pitfalls-one-system-in-a-gold-costume
description: "\"One System in a Gold Costume\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# One System in a Gold Costume (When "All of It" Is Really the Biggest System)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/88

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/88

## The problem

The integrated layer is supposed to be the whole picture: every call system, every website, every marketing source, as one. It says so on the slide.

Look closer and it's the biggest system, with the others bolted on. The big system's definitions, the big system's codes, the big system's customer IDs. The smaller systems are squeezed to fit, or left out because they didn't join.

So "total calls" is really "calls from the main system, plus whatever matched." Finance's number is different, and nobody can say why.

## The principle

System-agnostic means every system, one definition. Most teams call it gold. It's the layer the business, the dashboards and the AI agents read, so it has to be all of it, one way.

One definition of each thing that matters, agreed and owned, with each system's own rule mapped to it in the open. One shared list of codes. The source system kept on every row. The master data as the anchor, so one customer who showed up in two systems is one customer. And names in full words: an agent can only use what it can read without a lookup.

Certify it before anyone builds on it. Three stars is the line: owned, tested, documented, and joined to the master data. Four stars, checked against business outcomes, before it goes to the board or trains a model.

## The steps

1. **Count the systems.** For one domain, list every system that feeds it and every system that is actually in the integrated table. Any gap is the first thing to fix.
2. **Agree one definition, in the open.** Put the owners of each system in one room and agree what each thing means across all of them. Write down where each system’s own rule differs and how it maps.
3. **Anchor it and certify it.** Match through the master data, keep the source on every row, and rate it. Nothing gets built on it below three stars.

## In practice

A claims team's "enterprise" claims table came from the largest of three claims systems. The other two were joined on a policy number that matched only about 70% of the time, and the misses quietly disappeared. The table undercounted claims by 12%, and the gap showed up first in Finance's reconciliation.

They counted the systems in the domain against the systems in the table, matched every claim through the member master instead of the policy number, and wrote down one definition of an open claim across all three. The gap closed to under 1%, and the table got its third star.

## Inspired by

The essay "People and Systems Over Solutions" in The Auction Block, and Brian Cariveau’s talks on data layers.

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
