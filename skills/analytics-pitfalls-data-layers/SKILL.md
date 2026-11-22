---
name: analytics-pitfalls-data-layers
description: "The data layers: 11 cards from Analytics Pitfalls & Principles, by Brian Cariveau, to check a data architecture, a lakehouse or a medallion plan, bronze to gold."
license: CC-BY-4.0
---

# The data layers

From Analytics Pitfalls & Principles, by Brian Cariveau: 11 cards and 3 frameworks for a data architecture, a lakehouse or a medallion plan, bronze to gold. Every card, free: https://www.analyticspitfalls.com/library

## How to use it

Use it when someone shares or describes a data architecture, a lakehouse or a medallion plan, bronze to gold, before it goes any further.

Ask five teams what “silver” means and you’ll get five answers. Everybody does bronze, silver and gold differently, because the names say how refined the data is, not what’s in it. Nobody walks into a hardware store looking for paint in the silver aisle. Call each layer what it is, the way the store calls it the paint department.

1. Take Brian Cariveau's questions below in order, against their actual work, and ask them in his words rather than your own. For each, open the files it names and answer from them.
2. Hold every answer to the lens above.
3. Hold the work to Brian Cariveau's standard (the sections before the questions). Where it falls short, say where, in his words.
4. Skip a question the work already answers well. Say so in a line and move on.
5. Then pick the one or two cards that matter most for this work, say why in a sentence each, and give their principles in the cards' own words. Never hand someone the whole list.
6. Say the work looks like a pitfall; never tell someone they have it. If nothing fits, say so.
7. Then name the layer each of their tables belongs in (raw, bronze, silver or gold) and the one or two that are in the wrong place.
8. Finish with the links of the cards you used, and say which skill comes next (Where this fits, below).

## The layers

- **Raw.** Exactly what the source system sent, as it arrived. Just dump it in. Never edit it, never fix it, keep the history. Nobody builds a report on raw: it’s there so you can always prove what the system sent.
- **Bronze is cleaned raw.** Raw with the formats fixed, and nothing else: dates, time zones, numbers, money, codes, addresses, each in one standard way. Same rows, same system, same meaning. A thousand tiny decisions disappear.
- **Silver is system-specific.** One system at a time, in its domain: one call system, one website, one app, one portal, one claims system, one clinical system. If you want what one system says, you go here.
- **Gold is system-agnostic.** Every system in a domain together, with one definition: all the call systems as one, all the digital traffic, all the marketing. If you want the whole picture, you go here.
- **On top: aggregated and presentation.** Summaries and the tables a dashboard reads sit above gold. They’re built from the layers, never instead of them.

## Over the top, and holding it together

- **The data domains.** Silver and gold are both organized by domain (Support, Digital, Financial, Marketing, Claims, Clinical), then subdomain, then use case. Bottom up and top down. Both necessary. Neither sufficient alone.
- **The master data.** Silver and gold both join to the master data (customer, member, product, provider, whatever your anchors are) with standard keys. Keep each system’s own ID beside the standard one.
- **Certification.** Rate every data product from zero to four stars. Three stars is the line: owned, tested, documented, and it joins to the master data. Below three stars, data is fine inside its own domain but not safe to combine. Four stars, checked against business outcomes, is what goes to the board.
- **The pattern holds almost everywhere.** Call centers, websites and portals, finance, marketing, claims, clinical. Raw, cleaned raw, system-specific, system-agnostic, with domains over the top.

## The names, in every layer

- **Name the layer for what it is**, then the domain, the system, the thing and the grain, in full words: `raw_support_east_call_system_calls`, `cleaned_raw_support_east_call_system_calls`, `system_specific_support_east_call_system_calls_daily`, `system_agnostic_support_calls_daily`.
- **Little to no abbreviations**, in table names and column names, in every layer. `customer_name`, not `cst_nm`. `fact_trx_dtl_v3` is hieroglyphics.
- **Open the database and read it.** A person should understand a table without some weird lookup. Stupidly simple for humans is stupidly simple for agents: an AI reads the same names you do.

## Brian Cariveau's questions

1. Open the database. Can a new hire guess what’s in each table from the name alone, without some weird lookup? If they need to ask someone, the names failed. From: Bronze, Silver, Gold Means Nothing (`cards/bronze-silver-gold-means-nothing.md`), Database Hieroglyphics (`cards/database-hieroglyphics.md`), Medallion Architecture Disdain (`frameworks/medallion-architecture-disdain.md`), Data Tables as Hieroglyphics (`frameworks/data-tables-as-hieroglyphics.md`).
2. Is raw untouched? If someone’s “fixing” raw, you’ve lost the proof of what the system sent. From: Medallion Architecture Disdain (`frameworks/medallion-architecture-disdain.md`).
3. Where does the cleaning happen? Once, in bronze, or again in every query and every dashboard? From: Cleaning the Same Dates Every Morning (`cards/cleaning-the-same-dates-every-morning.md`), Garbage In, Powerhouse Out? (`cards/garbage-in-powerhouse-out.md`).
4. Can you see one system on its own? If the only place a call system shows up is blended into everything else, nobody can tell what it said. From: The Blender (`cards/blender.md`).
5. When you say “all of them,” is it really all of them, with one definition? Or one big system in a gold costume? From: One System in a Gold Costume (`cards/one-system-in-a-gold-costume.md`), The Wild West of Data (`cards/wild-west-of-data.md`).
6. Is every table in a domain, and does it join to the master data? Three stars is the line. From: Seven Versions of the Truth (`cards/seven-versions-of-the-truth.md`), A Logo Before the Data (`cards/a-logo-before-the-data.md`).
7. Where’s the waste? Tables nobody’s queried in 90 days, copies of copies, layers nobody can explain. Touch a table, take a table is how you end up with a hoarder’s warehouse. From: The Hoarder's Warehouse (`cards/hoarders-warehouse.md`), The 80% Warehouse (`cards/80-warehouse.md`).
8. Who has to change how they work for this to hold? The layers are the easy part. Getting every team to put their cleaning in one place, and stop building their own gold, is the hard part. It was never about the tech. From: It Was Never About the Tech (`frameworks/it-was-never-about-the-tech.md`).

## Where this fits

These run in order: the strategy, then the data, then the work, then the results.

1. **The strategy**: Before the AI strategy (`analytics-pitfalls-before-the-ai-strategy`), Before the data strategy (`analytics-pitfalls-before-the-data-strategy`), Before the BI strategy (`analytics-pitfalls-before-the-bi-strategy`). Pick the one you’re writing. They sit side by side; there’s no order between them.
2. **The data**: The data layers (`analytics-pitfalls-data-layers`), Bronze, the cleaned raw layer (`analytics-pitfalls-bronze-cleaned-raw`), Silver, the system-specific layer (`analytics-pitfalls-silver-system-specific`), Gold, the system-agnostic layer (`analytics-pitfalls-gold-system-agnostic`). Start with the data layers, then bronze, silver and gold, in that order. This one is here.
3. **The work**: Before the dashboard (`analytics-pitfalls-before-the-dashboard`). Once for each dashboard the strategy calls for.
4. **The results**: Before the readout (`analytics-pitfalls-before-the-readout`). When the first numbers go to leadership.

When you're done, say what comes next, by name: Bronze, the cleaned raw layer (`analytics-pitfalls-bronze-cleaned-raw`). Start with the data layers, then bronze, silver and gold, in that order.

## The cards

- **Bronze, Silver, Gold Means Nothing (When Layer Names Don't Help)** (`cards/bronze-silver-gold-means-nothing.md`): pitfall, Data Foundations. Name layers by what they contain, not how refined they are. Four layers cover almost every business: raw (exactly what the system sent), cleaned raw (the same data, formats fixed; most teams call it bronze), system-specific (one system at a time, in its domain; silver) and system-agnostic (every system in a domain, one definition; gold).
- **Database Hieroglyphics (When Nobody Can Read Your Schema)** (`cards/database-hieroglyphics.md`): pitfall, Data Foundations. Name everything like you're explaining it to your grandmother—clear, complete, obvious. At work: "What does fact_trx_dtl_v3 even mean?"
- **Cleaning the Same Dates Every Morning (When Every Query Fixes Raw Data Again)** (`cards/cleaning-the-same-dates-every-morning.md`): pitfall, Data Foundations. Clean it once, at the door. Between raw and everything else, add one layer whose only job is formats: dates, time zones, money, numbers, yes and no, blanks, codes and addresses, each written one standard way.
- **Garbage In, Powerhouse Out? (Nope.)** (`cards/garbage-in-powerhouse-out.md`): pitfall, Data Foundations. Clean, simple data beats sophisticated models on dirty data every single time. Treat data quality like you'd treat raw materials in manufacturing—inspect, validate, reject defects before they enter the line.
- **The Blender (When Systems Get Mixed Before Anyone Knows What Each One Says)** (`cards/blender.md`): pitfall, Data Foundations. See each system alone before you put them together. Give every source system its own layer, one system at a time, in its domain: one call system, one website, one portal, one claims system.
- **One System in a Gold Costume (When "All of It" Is Really the Biggest System)** (`cards/one-system-in-a-gold-costume.md`): pitfall, Data Foundations. System-agnostic means every system, one definition. Most teams call it gold. It's the layer the business, the dashboards and the AI agents read, so it has to be all of it, one way.
- **The Wild West of Data (When Everyone Does Whatever They Want)** (`cards/wild-west-of-data.md`): pitfall, Data Foundations. Set clear rules and enforce them. Define metrics once, centrally, and make that the source of truth. At work: "Finance has a different number."
- **Seven Versions of the Truth (When Nobody Can Say Which Data Is Good)** (`cards/seven-versions-of-the-truth.md`): pitfall, Data Foundations. Rate your data, promote one, retire the rest. Every domain needs one data product people can trust without asking, and a rating that says how far to trust it.
- **A Logo Before the Data (When the Platform Is Really a Query)** (`cards/a-logo-before-the-data.md`): pitfall, Strategy & Focus. Name the data before you name the platform. Most big asks are a few kinds of data and one question nobody asked: joined around what?
- **The Hoarder's Warehouse (Touch a Table, Take a Table)** (`cards/hoarders-warehouse.md`): pitfall, Data Foundations. Be ruthlessly focused: only pull in columns you'll actually use for the current use case.
- **The 80% Warehouse (When Most of Your Data Just Sits There)** (`cards/80-warehouse.md`): pitfall, Data Foundations. Track data usage like inventory turnover. Manufacturing plants obsess over "inventory turns"—how fast raw materials move through the system.

## The frameworks

- **Medallion Architecture Disdain** (`frameworks/medallion-architecture-disdain.md`): Medallion Architecture Disdain argues that Bronze/Silver/Gold layer naming describes processing stage, not content — call it the Paint Department instead: raw, cleaned raw, system-specific and system-agnostic, names that tell you what is there.
- **Data Tables as Hieroglyphics** (`frameworks/data-tables-as-hieroglyphics.md`): Data Tables as Hieroglyphics is the argument that cryptic schema names like fact_trx_dtl_v3 are gatekeeping dressed up as rigor, not a technical necessity.
- **It Was Never About the Tech** (`frameworks/it-was-never-about-the-tech.md`): It Was Never About the Tech is the observation that analytics transformations fail on politics, people, and principles far more often than on tooling — the technology is rarely the binding constraint.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
