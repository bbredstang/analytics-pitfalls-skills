---
name: analytics-pitfalls-data-tables-as-hieroglyphics
description: "The \"Data Tables as Hieroglyphics\" framework from Analytics Pitfalls & Principles, by Brian Cariveau, as a lens on analytics and AI work."
license: CC-BY-4.0
---

# Data Tables as Hieroglyphics

A framework from Analytics Pitfalls & Principles, by Brian Cariveau.
https://www.analyticspitfalls.com/frameworks/data-tables-as-hieroglyphics

## How to use this framework

Use it as a lens when someone's analytics or AI work touches what it describes.

1. Say which framework you are using and what it asks, in its one-line definition below.
2. Hold their work up to it: where it already fits, and where it does not. Be specific to their situation.
3. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
4. If one of the cards below names their problem more exactly, use that card as it says.
5. Finish with the framework's link: https://www.analyticspitfalls.com/frameworks/data-tables-as-hieroglyphics

> Data Tables as Hieroglyphics is the argument that cryptic schema names like fact_trx_dtl_v3 are gatekeeping dressed up as rigor, not a technical necessity.

## What the problem actually looks like

Walk into most enterprise data warehouses and you will find table names like cst_prf_x_loc_dim. Nobody outside the original team knows what it means on sight. New analysts spend weeks decoding abbreviations that were never documented anywhere, because the people who invented the shorthand left the company years ago and took the decoder ring with them. What is left is a schema that requires a two-hundred-page glossary just to answer "where is the customer data," and that glossary is itself usually out of date.


## The fix is almost embarrassingly simple

Ban abbreviations entirely. Name every table and column as if you were explaining it to someone with zero context — customer_profile_crosswalk_location_dimension instead of cst_prf_x_loc_dim. Yes, it's longer to type. It's also self-documenting, which means the documentation nobody maintains stops mattering as much, because the schema explains itself.

This isn't a purity argument. It has a measurable payoff that shows up twice: once in how fast new people get productive, and again — increasingly — in how well AI tools can work with your data. A large language model asked to write a query against cst_prf_x_loc_dim is guessing. Asked to query customer_profile_crosswalk_location_dimension, it isn't. Clear naming was always worth doing for your junior analysts. Now it's also worth doing for the AI you're about to ask to write SQL against your warehouse.


## Why teams resist it anyway

The objection is almost always 'it's too long' — a complaint about characters typed, weighed against weeks lost onboarding, Slack threads asking "what does this column mean," and models that hallucinate joins because the names gave them nothing to go on. Once a team actually renames its most-used tables and watches onboarding time and AI query accuracy both improve, the "too long" objection tends to evaporate. Nobody misses the abbreviations. Everybody remembers being lost because of them.


## This week's version

You don't need to rename your whole warehouse today. Pick your twenty most-queried tables. Rename them during the next migration you were already planning. Write a one-page naming standard and make it a code review requirement going forward — full names, no exceptions, starting now.


## Cards that go with it

- **Database Hieroglyphics (When Nobody Can Read Your Schema)** (`cards/database-hieroglyphics.md`), https://www.analyticspitfalls.com/cards/29

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
