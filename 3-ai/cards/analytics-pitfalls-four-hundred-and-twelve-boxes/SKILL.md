---
name: analytics-pitfalls-four-hundred-and-twelve-boxes
description: "\"Four Hundred and Twelve Boxes\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# Four Hundred and Twelve Boxes (Building the AI Ontology From the Top Down)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Second Factory*, Brian Cariveau's next novel (https://www.analyticspitfalls.com/second-factory).
https://www.analyticspitfalls.com/cards/79

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/79

## The problem

Someone stands up with a deck. Every AI-native company has an ontology, a model of the business that agents can understand. The next slide is a diagram with four hundred boxes and so many lines it looks like a plate of spaghetti. Eighteen months, enterprise-wide, top down, with a consulting partner.

You've seen this dream before. Ten years ago it was a single source of truth. Then a semantic layer. Now an ontology. Same dream, new word, same ending: out of date before it's finished, drawn by people who've never answered a customer's call, and nobody uses it.

Meanwhile your agents are guessing. If a new hire would be confused by your data, the agent will be too. It'll just be confused confidently, at scale.

## The principle

Simple for humans is simple for agents. Build the map one trusted domain at a time, in words a new hire would understand.

An ontology is a map of the things your business cares about, what each one means and how they connect. A seller lists a vehicle. A part fits certain vehicles. You may already have most of it. If your data products are rated, owned and joined on the same keys, that's the backbone. All that's missing are the words.

Start with one question a real leader asks every week. Write a plain-English definition for every term it depends on, each pointing at the data it comes from. Let AI stand only on data you trust: three stars and up, on a scale of zero to four. Then test it like code, sit beside the leader while they ask, and pick the next domain.

## The steps

1. **Pick one question and one sponsor.** Not an enterprise model. One question a real leader asks every week, written down word for word.
2. **Rate the data it needs.** Zero to four stars, honestly. Three stars means it has an owner and joins reliably on your core keys, and that's the line for anything AI touches. If someone argues their data is three stars, test the join in front of them.
3. **Write the words.** A plain-English definition for every term, each pointing at its data. Read each one aloud and ask whether someone in their first week would understand it.
4. **Test it like code.** Twenty real questions with known answers. Fix the definitions, not the answers. Don't show anyone until it gets eighteen right and cites its sources.

## In practice

At ClassicMotors' weekly leadership meeting, the head of Enterprise Architecture put one word on his first slide: ONTOLOGY. His second was a diagram with four hundred and twelve boxes. Eighteen months, enterprise-wide, scoped with a consulting partner.

Jin Park, who ran the data factory floor, looked at the ceiling. "Ten years ago, everybody needed a single source of truth. A few years later, everybody needed a semantic layer. Now it's an ontology. New word. Same dream. Same plate of spaghetti."

That evening, Nora Berg asked the AI to explain an ontology three ways, the last as if she'd never heard the word and was suspicious of it. A map of the things a business cares about, what each one means and how they connect. She stopped walking in front of a neighbor's garage.

The next morning, she stood at the end of the catwalk in front of a wall she'd walked past a hundred times: the domain map Sarah Chen and Jin had built years earlier. Twelve domains, the data products under each, and a star rating, zero to four, next to every one. Eleven of the twelve domains were at three stars or better.

"Oh," Jin said, when he saw what she saw. "Oh, that's annoying. We did the hard part."

## Inspired by

Chapter 8 of The Second Factory, "The Map We Didn't Know We Needed," and the domain map from The Auction Block. And a line first written in a comment on a post by Joe Reis: stupidly simple for humans is stupidly simple for AI.

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
