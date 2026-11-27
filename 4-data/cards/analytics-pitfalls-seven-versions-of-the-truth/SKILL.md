---
name: analytics-pitfalls-seven-versions-of-the-truth
description: "\"Seven Versions of the Truth\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# Seven Versions of the Truth (When Nobody Can Say Which Data Is Good)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/85

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/85

## The problem

Someone needs survey data, so you search the warehouse. Seven tables come back. A raw dump that still has test accounts in it. A monthly file somebody uploads by hand. A quarterly feed from a vendor on a different scale. A "cleaned" copy nobody has touched in four months. A v2 that duplicates the monthly with new column names. A legacy merge with broken joins. A daily feed that might be fine.

You ask the team which one is right. "Depends what you need." Nobody can say which is good, which is better or which is best, and none of them joins cleanly to the customer table.

So every analyst picks whichever one loads first, two reports disagree, and the meeting turns into an argument about whose number is right. Then you check another domain and find the same thing.

## The principle

Rate your data, promote one, retire the rest. Every domain needs one data product people can trust without asking, and a rating that says how far to trust it.

Score every data product from zero to four stars, like a restaurant guide. Zero: it exists. One: documented, so you can understand it without tribal knowledge. Two: tested, so you know when it breaks. Three: governed, with an owner, and it joins to the master record with standard keys. Four: reference grade, checked against business outcomes by whoever owns the number, the way Finance signs off on revenue.

Three stars is the line. Below it, data is fine inside its own domain but not safe to combine. At three and above, you can join survey to customer to orders and trust the answer. Four stars is what goes to the board and what you train models on.

Start from the query logs, not a form. Logs tell you what people use. They don't tell you what's good; that part you earn. Then count how many domains have a product at three stars or more, and watch that number every month. The same map that helps a new analyst find the right data in an afternoon tells an AI model where its context lives.

## The steps

1. **Pull the logs for one domain.** Take the domain people argue about most. Pull ninety days of query logs: which tables get read, how often, by how many teams, joined to what. The most-used product is your candidate. A table nobody has read in six months goes on the retire list.
2. **Rate every product in one meeting.** Put the person who builds the data and the person who uses it in the same room and score every product from zero to four stars. Agree on what three stars means before you start: an owner, tests, documentation, and a clean join to the master record with standard keys.
3. **Promote one, retire the rest, report coverage.** Invest in the best candidate until it reaches three stars, then give the others a retirement date. Report one number every month: how many domains have a product at three stars or more. Anything below three that goes into a board report carries its rating next to it.

## In practice

At ClassicMotors, a request for survey data turned up seven survey tables. Marcus, the analyst closest to them, could explain each one and still couldn't say which was right. None joined cleanly to the seller master: one used email addresses, another the vendor's own IDs.

Jin didn't send around a form asking teams what they trusted. He pulled ninety days of query logs. The daily seller-feedback table had been queried more than two thousand times by four teams, almost always joined to sellers. The monthly upload had one regular user: Marcus, the morning after each upload. The v2 hadn't been touched in six months. The legacy merge was read every night by a job that fed nothing.

Then they rated all seven. None scored above two stars. They promoted the seller-feedback table to three, standardized its seller key, gave it an owner and retired the other six.

Over six weeks they ran the same audit across all twelve domains. Only about 10% of the estate reached three stars, but those products covered nine of the twelve domains. When Jack, the CEO, saw the map with its stars, he asked, "How did I not know our data was this simple?" Two months later his board asked how AI-ready the data was. He answered with one slide: nine of twelve domains at three stars or above.

## Inspired by

Chapter 8 of The Auction Block, "The Map We Didn't Know We Needed."

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
