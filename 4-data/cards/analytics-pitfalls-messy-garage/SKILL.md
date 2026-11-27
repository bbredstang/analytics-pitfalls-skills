---
name: analytics-pitfalls-messy-garage
description: "\"The Messy Garage\" (When Clutter Holds You Back): a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# The Messy Garage (When Clutter Holds You Back)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/62

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/62

## The problem

Your data platform looks like a messy garage. Expired ETL jobs from 2019 still running—like tools you haven't touched in years. Datasets nobody remembers building, piled like boxes labeled "misc stuff." Duplicate tables with names like "customer_v2," "customer_final," "customer_FINAL2"—like having three sets of wrenches because you can't find the first two. Dashboard folders 12 levels deep. Every time you need something, you have to search through the clutter. New projects take forever because you can't find existing work—easier to just rebuild it. Team morale tanks because navigating the mess is exhausting. It's like trying to fix a car in a garage where half the tools are broken, everything's buried under junk, and you spend more time searching than working. The clutter isn't just messy—it's slowing down everything you do.

## The principle

Clean the garage. Manufacturing plants run "5S" programs (Sort, Set in order, Shine, Standardize, Sustain)—regular cleanup cycles to eliminate waste. Apply same to your data platform. Monthly cleanup ritual: archive unused jobs, delete duplicate tables, consolidate redundant dashboards, organize folders logically. Create "days since last use" metric for everything: data, jobs, dashboards, code. If it's been >90 days without use, archive it. If someone needs it later, unarchive it. The magic happens when your platform is so clean that finding what you need takes seconds, not hours. Every team member can find existing work before building new. Think classic car restoration: you can't work on the Mustang if you can't even get into the garage. Clutter elimination = velocity increase.

## The steps

1. **Inventory the Mess**

Create "clutter report":
- ETL jobs: how many? Days since last run?
- Tables/datasets: how many? Days since last query?
- Dashboards/reports: how many? Days since last view?
- Code repos: how many? Days since last commit?
- Folders: how deep is nesting? How many empty?

Calculate "clutter score": Sum of (items × days unused)

Higher score = more clutter = more drag on team velocity.
2. **Monthly Garage Cleaning Ritual**

Last Friday of every month: 2-hour team cleanup session.

Agenda:
1. Review "unused in 90+ days" list (15 min)
2. Archive or delete unused items (45 min)
3. Rename confusing things (30 min)
4. Reorganize folders (30 min)

Rules:
- If nobody remembers what it does, archive it
- If it's a duplicate, delete the worse version
- If name is confusing, rename it
- If folder is >3 levels deep, flatten it

Celebrate: Track items archived/deleted each session. Aim for 10%+ reduction monthly until steady state.
3. **Prevent Future Clutter**

Create "clean as you go" standards:
- New items must have clear names and descriptions
- Duplicate work requires justification
- Items unused for 90 days auto-flagged for review
- Folder depth limit: 3 levels max
- Code repos require README with purpose

Quarterly "deep clean": Bigger cleanup session, 4 hours.

Goal: Platform stays so clean that new hires can navigate it independently within 1 week.

Bonus: Tie promotions to "left platform cleaner than you found it."

## In practice

A major bank's analytics team had 2,300+ ETL jobs. Nobody knew what half of them did. Dashboards in folders so nested that finding anything took 20 minutes. New projects always started from scratch because finding existing work was harder than rebuilding. They implemented monthly "garage cleaning": Last Friday of every month, 2-hour team session. Review "unused in 90+ days" list. Archive anything nobody needed. Delete duplicates. Rename confusing things. Reorganize folders. First session: archived 420 ETL jobs (18%), deleted 180 duplicate dashboards, flattened folder structure from 12 levels to 3. Developer experience transformed: "I can finally find things!" Time to find reusable work dropped from 45 minutes to 5 minutes. New project velocity up 30% because teams reused existing work instead of rebuilding. The garage cleaning became cultural ritual: "Clean platform = fast team."

## Inspired by

Manufacturing 5S principles (Sort, Set in order, Shine, Standardize, Sustain). Classic car garage metaphor aligns with fable's automotive theme (Sarah's 1981 Porsche 911, Ben's Mustang).

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
