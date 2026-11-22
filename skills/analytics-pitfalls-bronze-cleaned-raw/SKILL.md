---
name: analytics-pitfalls-bronze-cleaned-raw
description: "Bronze, the cleaned raw layer: 6 cards from Analytics Pitfalls & Principles, by Brian Cariveau, to check a bronze or cleaned raw layer, or the cleanup a team repeats in every query."
license: CC-BY-4.0
---

# Bronze, the cleaned raw layer

From Analytics Pitfalls & Principles, by Brian Cariveau: 6 cards and 1 framework for a bronze or cleaned raw layer, or the cleanup a team repeats in every query. Every card, free: https://www.analyticspitfalls.com/library

## How to use it

Use it when someone shares or describes a bronze or cleaned raw layer, or the cleanup a team repeats in every query, before it goes any further.

Clean it once, at the door. Every format you fix here is one nobody fixes again in a query, a dashboard or a model. Format, not meaning: bronze changes how the data is written, never what it says.

1. Take Brian Cariveau's questions below in order, against their actual work, and ask them in his words rather than your own. For each, open the files it names and answer from them.
2. Hold every answer to the lens above.
3. Hold the work to Brian Cariveau's standard (the sections before the questions). Where it falls short, say where, in his words.
4. Skip a question the work already answers well. Say so in a line and move on.
5. Then pick the one or two cards that matter most for this work, say why in a sentence each, and give their principles in the cards' own words. Never hand someone the whole list.
6. Say the work looks like a pitfall; never tell someone they have it. If nothing fits, say so.
7. Then list the formats still in more than one shape, most-queried first, and the cleanup to take out of the queries once bronze holds.
8. Finish with the links of the cards you used, and say which skill comes next (Where this fits, below).

## What gets cleaned in bronze

- **Dates.** One format everywhere: 2026-11-22. No text dates, no two-digit years, no “11/12” that means November in one system and December in another.
- **Time.** Timestamps in one time zone, with the original kept beside them. Say the zone in the column name: `called_at_utc`.
- **Money.** Whole cents, as whole numbers, with the currency stated. No floating point, no “$1,234.50” stored as text.
- **Numbers.** Real number types, not text. One decimal separator. Units in the column name: `weight_kilograms`, `duration_seconds`.
- **Yes and no.** One way. Not Y/N in one column, 1/0 in the next and TRUE/FALSE in a third.
- **Blanks.** Empty means empty. “N/A”, “NULL”, “none”, “-”, “9999-12-31” and a single space all become a real null.
- **Text.** Trimmed, in one character encoding, codes in one case.
- **Standard codes.** States, countries and currencies in their standard codes. The source’s own codes stay as they are: turning them into words is silver’s job.
- **Addresses.** Split into parts (street, city, state, postal code, country) and standardized, with the original kept beside them.
- **Phone numbers and email.** One format for phones, lowercase for email.
- **Column names.** Full words, one style. No `cst_nm`, no `fld_07`. Would your grandmother understand it? Someone opening the table should read it without a lookup.
- **Where it came from.** Every row says which system sent it and when it landed.

## What never happens in bronze

- **No business rules.** What counts as a completed call, an active customer or a closed claim is decided in silver.
- **No joins across systems.** That’s gold.
- **No dropped rows.** Test accounts, duplicates and bad records get flagged, not deleted. Someone downstream decides what to leave out.
- **Same rows as raw.** One row in, one row out. If the count changes, something’s wrong.

## Brian Cariveau's questions

1. Is the cleaning happening once, here, or again in every query? If three analysts each fix the dates their own way, you’ve got three answers. From: Cleaning the Same Dates Every Morning (`cards/cleaning-the-same-dates-every-morning.md`), Garbage In, Powerhouse Out? (`cards/garbage-in-powerhouse-out.md`).
2. Go down the list: dates, time, money, numbers, yes and no, blanks, text, codes, addresses. Which are still in more than one shape? From: Cleaning the Same Dates Every Morning (`cards/cleaning-the-same-dates-every-morning.md`).
3. Did anything change what the data means? If a rule needs someone from the business to agree to it, it belongs in silver, not here. From: Cleaning the Same Dates Every Morning (`cards/cleaning-the-same-dates-every-morning.md`), The Blender (`cards/blender.md`).
4. Does the row count match raw? Were any rows dropped instead of flagged? From: Cleaning the Same Dates Every Morning (`cards/cleaning-the-same-dates-every-morning.md`).
5. Can every row tell you which system sent it, and when? From: The Blender (`cards/blender.md`).
6. Open the table. Can a stranger read every column name without a lookup? Little to no abbreviations. Stupidly simple for humans is stupidly simple for agents. From: Database Hieroglyphics (`cards/database-hieroglyphics.md`), Data Tables as Hieroglyphics (`frameworks/data-tables-as-hieroglyphics.md`).
7. Is it tested? You should know a new date format snuck in before a dashboard does. Two stars is tested. From: Seven Versions of the Truth (`cards/seven-versions-of-the-truth.md`).
8. Who has to stop cleaning in their own queries and trust this layer instead? That’s the change. Nobody gives up their own fix until they’ve seen the shared one hold. We’re in the behavior change business. From: We're in the Behavior Change Business (`cards/were-in-the-behavior-change-business.md`).

## Where this fits

These run in order: the strategy, then the data, then the work, then the results.

1. **The strategy**: Before the AI strategy (`analytics-pitfalls-before-the-ai-strategy`), Before the data strategy (`analytics-pitfalls-before-the-data-strategy`), Before the BI strategy (`analytics-pitfalls-before-the-bi-strategy`). Pick the one you’re writing. They sit side by side; there’s no order between them.
2. **The data**: The data layers (`analytics-pitfalls-data-layers`), Bronze, the cleaned raw layer (`analytics-pitfalls-bronze-cleaned-raw`), Silver, the system-specific layer (`analytics-pitfalls-silver-system-specific`), Gold, the system-agnostic layer (`analytics-pitfalls-gold-system-agnostic`). Start with the data layers, then bronze, silver and gold, in that order. This one is here.
3. **The work**: Before the dashboard (`analytics-pitfalls-before-the-dashboard`). Once for each dashboard the strategy calls for.
4. **The results**: Before the readout (`analytics-pitfalls-before-the-readout`). When the first numbers go to leadership.

When you're done, say what comes next, by name: Silver, the system-specific layer (`analytics-pitfalls-silver-system-specific`). Start with the data layers, then bronze, silver and gold, in that order.

## The cards

- **Cleaning the Same Dates Every Morning (When Every Query Fixes Raw Data Again)** (`cards/cleaning-the-same-dates-every-morning.md`): pitfall, Data Foundations. Clean it once, at the door. Between raw and everything else, add one layer whose only job is formats: dates, time zones, money, numbers, yes and no, blanks, codes and addresses, each written one standard way.
- **Garbage In, Powerhouse Out? (Nope.)** (`cards/garbage-in-powerhouse-out.md`): pitfall, Data Foundations. Clean, simple data beats sophisticated models on dirty data every single time. Treat data quality like you'd treat raw materials in manufacturing—inspect, validate, reject defects before they enter the line.
- **The Blender (When Systems Get Mixed Before Anyone Knows What Each One Says)** (`cards/blender.md`): pitfall, Data Foundations. See each system alone before you put them together. Give every source system its own layer, one system at a time, in its domain: one call system, one website, one portal, one claims system.
- **Database Hieroglyphics (When Nobody Can Read Your Schema)** (`cards/database-hieroglyphics.md`): pitfall, Data Foundations. Name everything like you're explaining it to your grandmother—clear, complete, obvious. At work: "What does fact_trx_dtl_v3 even mean?"
- **Seven Versions of the Truth (When Nobody Can Say Which Data Is Good)** (`cards/seven-versions-of-the-truth.md`): pitfall, Data Foundations. Rate your data, promote one, retire the rest. Every domain needs one data product people can trust without asking, and a rating that says how far to trust it.
- **We're in the Behavior Change Business (Not the Data Business)** (`cards/were-in-the-behavior-change-business.md`): principle, Adoption & Product. Apply consumer behavior principles to analytics adoption. Make it stupid simple to use—reduce friction, eliminate training requirements where possible.

## The frameworks

- **Data Tables as Hieroglyphics** (`frameworks/data-tables-as-hieroglyphics.md`): Data Tables as Hieroglyphics is the argument that cryptic schema names like fact_trx_dtl_v3 are gatekeeping dressed up as rigor, not a technical necessity.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
