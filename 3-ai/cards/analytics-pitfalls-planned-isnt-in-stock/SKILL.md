---
name: analytics-pitfalls-planned-isnt-in-stock
description: "\"Planned Isn't In Stock\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# Planned Isn't In Stock (When an Agent Reads Data Nobody Defined)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Second Factory*, Brian Cariveau's next novel (https://www.analyticspitfalls.com/second-factory).
https://www.analyticspitfalls.com/cards/68

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/68

## What it sounds like at work

"Just point the agent at the shared drive."

## The problem

A marketer builds an agent that finds owners of a particular car and emails them about parts. Everyone cheers. It's exactly the kind of builder you hoped for.

Nobody notices where it gets its information. It's pointed at a shared folder, and inside is the product roadmap: every part the team plans to make, with target dates. The agent reads "tail-light lens, Q2" and concludes, perfectly reasonably, that you sell tail-light lenses. So it tells hundreds of customers they're in stock.

Every person in the building knows the difference between planned and in stock. Nobody ever wrote it down, because nobody had to. An agent only knows what's been written down, and it acts on whatever it reads at full speed.

## The principle

Customer-facing agents read only from defined, trusted data. If a word matters to the business, write down what it means before an agent acts on it.

Planned, in production, on order and in stock are four different things. People learn the difference in their first month. Agents learn it from a definition or not at all. So define the words that carry promises (in stock, available, delivered, eligible, active), put each definition next to the data it comes from, and give it an owner.

Then draw a line. Anything that talks to a customer reads from certified data only, three stars or better. No roadmaps. No shared folders. Just the truth.

## The steps

1. **List the words that carry promises.** In stock, available, delivery date, refund window, eligible. Write a plain-English definition of each, pointing at the data it comes from, with an owner.
2. **Draw the three-star line.** Anything that talks to a customer reads from certified data only. No shared folders, no roadmaps, no exceptions on request.
3. **Ask what every agent reads.** For each customer-facing agent, list its sources. Anything you can't name is a promise waiting to go wrong.
4. **Correct it honestly.** When one does go wrong, tell customers the truth, short and in plain English, and offer them a place in line.

## In practice

Lena Brooks, a campaign manager at ClassicMotors, built her first agent in one of the company's AI sessions. It found owners of a particular model in the auction data, wrote each of them a personal email and sent it. She showed it off in the company's AI channel. It got forty reactions.

She'd pointed it at a shared folder called Parts Launch, where the parts team kept its roadmap. The agent read "1967 Shelby GT500 tail-light lens, Q2" and told nine hundred and fourteen Shelby owners the lenses were in stock. By nine that night, a hundred and forty-one had replied and twenty-three had tried to order. One wrote, in capital letters, I HAVE BEEN LOOKING FOR THESE FOR ELEVEN YEARS.

"Nobody told it the difference between planned and real," Lena kept saying.

"Nobody told it because nobody's told anyone," Nora said.

At the board meeting the next day, the lead independent director mentioned she'd had the email. She owned a 1967 Shelby.

## Inspired by

Chapters 8 and 9 of The Second Factory. And the discovery that nothing makes a team fix its data faster than an AI politely refusing to use it.

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
