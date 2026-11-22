---
name: analytics-pitfalls-gold-system-agnostic
description: "Gold, the system-agnostic layer: 7 cards from Analytics Pitfalls & Principles, by Brian Cariveau, to check a gold or system-agnostic layer, every system in a domain as one."
license: CC-BY-4.0
---

# Gold, the system-agnostic layer

From Analytics Pitfalls & Principles, by Brian Cariveau: 7 cards and 1 framework for a gold or system-agnostic layer, every system in a domain as one. Every card, free: https://www.analyticspitfalls.com/library

## How to use it

Use it when someone shares or describes a gold or system-agnostic layer, every system in a domain as one, before it goes any further.

All of it, one way. All the call systems as one. All the digital traffic as one. All the marketing as one. Gold is what the business, the dashboards and the agents read, so it’s the layer that has to earn its stars. Stupidly simple for humans. Stupidly simple for robots.

1. Take Brian Cariveau's questions below in order, against their actual work, and ask them in his words rather than your own. For each, open the files it names and answer from them.
2. Hold every answer to the lens above.
3. Hold the work to Brian Cariveau's standard (the sections before the questions). Where it falls short, say where, in his words.
4. Skip a question the work already answers well. Say so in a line and move on.
5. Then pick the one or two cards that matter most for this work, say why in a sentence each, and give their principles in the cards' own words. Never hand someone the whole list.
6. Say the work looks like a pitfall; never tell someone they have it. If nothing fits, say so.
7. Then list each domain’s gold table with its stars, and for any below three, what’s in the way.
8. Finish with the links of the cards you used, and say which skill comes next (Where this fits, below).

## What belongs in gold

- **Every system in the domain, together.** Built from the silver tables, never straight from raw.
- **One definition per thing.** One definition of a completed call across all three call systems. One definition of a visit across every website and portal. Agreed once, written down, owned. Where a system’s own rule differs, the difference is mapped in the open, not buried in a CASE statement.
- **One list of codes.** Each system’s codes mapped to one shared list. “Transferred” means the same thing whichever system it came from.
- **The source on every row.** Every row still says which system it came from, so anyone can go back to silver and check.
- **The master data as the anchor.** Customers, members, products and providers matched across systems through the master data, so one customer who called on two systems is one customer.
- **Certified.** Three stars at least before anything is built on it. Four stars, checked against business outcomes by whoever owns the number, before it goes to the board or trains a model.
- **Names anyone can read.** `system_agnostic_support_calls_daily`, with columns in full words. Little to no abbreviations. This is the layer the agents read, and an agent can only use what it can understand without a lookup.
- **What’s built on top.** Aggregated and presentation tables, metrics, dashboards and AI agents read from here.

## What never happens in gold

- **No single system in a gold costume.** If it’s really the biggest system with the others bolted on, it’s silver with a fancier name.
- **No format fixing.** If you’re fixing dates here, bronze isn’t doing its job.
- **No shortcuts from raw.** Straight from raw means there’s nothing to check it against.

## Brian Cariveau's questions

1. Is it really every system, or the biggest one with the others bolted on? Count the systems in the domain, then count the ones in the table. From: One System in a Gold Costume (`cards/one-system-in-a-gold-costume.md`).
2. Is there one definition of each thing that matters, agreed and owned? If Finance has a different number, the line is already making defects. From: The Wild West of Data (`cards/wild-west-of-data.md`).
3. Where a system’s own rule disagreed, is that written down where people can see it? From: One System in a Gold Costume (`cards/one-system-in-a-gold-costume.md`).
4. Does every row say which system it came from, so anyone can go back to silver and check? From: One System in a Gold Costume (`cards/one-system-in-a-gold-costume.md`), The Blender (`cards/blender.md`).
5. Is it matched through the master data? Is one customer one customer, wherever they showed up? From: Seven Versions of the Truth (`cards/seven-versions-of-the-truth.md`).
6. How many stars? Three before anyone builds on it. Four before it goes to the board or trains a model. From: Seven Versions of the Truth (`cards/seven-versions-of-the-truth.md`).
7. Was it built from silver, or straight from raw? Straight from raw, there’s nothing to check it against. From: The Blender (`cards/blender.md`).
8. What reads from it? Dashboards, metrics, agents. Can an agent open the table and understand it without a lookup? Has anyone defined what it reads? Planned isn’t in stock. From: Planned Isn't In Stock (`cards/planned-isnt-in-stock.md`), Database Hieroglyphics (`cards/database-hieroglyphics.md`).
9. Is the “platform” really just a few domains and a join? Don’t design a logo before the data. From: A Logo Before the Data (`cards/a-logo-before-the-data.md`).
10. Who gives up their own definition for the shared one? Every team that built its own gold has to let it go. It was never about the tech. From: It Was Never About the Tech (`frameworks/it-was-never-about-the-tech.md`).

## Where this fits

These run in order: the strategy, then the data, then the work, then the results.

1. **The strategy**: Before the AI strategy (`analytics-pitfalls-before-the-ai-strategy`), Before the data strategy (`analytics-pitfalls-before-the-data-strategy`), Before the BI strategy (`analytics-pitfalls-before-the-bi-strategy`). Pick the one you’re writing. They sit side by side; there’s no order between them.
2. **The data**: The data layers (`analytics-pitfalls-data-layers`), Bronze, the cleaned raw layer (`analytics-pitfalls-bronze-cleaned-raw`), Silver, the system-specific layer (`analytics-pitfalls-silver-system-specific`), Gold, the system-agnostic layer (`analytics-pitfalls-gold-system-agnostic`). Start with the data layers, then bronze, silver and gold, in that order. This one is here.
3. **The work**: Before the dashboard (`analytics-pitfalls-before-the-dashboard`). Once for each dashboard the strategy calls for.
4. **The results**: Before the readout (`analytics-pitfalls-before-the-readout`). When the first numbers go to leadership.

When you're done, say what comes next, by name: Before the dashboard (`analytics-pitfalls-before-the-dashboard`). Once for each dashboard the strategy calls for.

## The cards

- **One System in a Gold Costume (When "All of It" Is Really the Biggest System)** (`cards/one-system-in-a-gold-costume.md`): pitfall, Data Foundations. System-agnostic means every system, one definition. Most teams call it gold. It's the layer the business, the dashboards and the AI agents read, so it has to be all of it, one way.
- **The Wild West of Data (When Everyone Does Whatever They Want)** (`cards/wild-west-of-data.md`): pitfall, Data Foundations. Set clear rules and enforce them. Define metrics once, centrally, and make that the source of truth. At work: "Finance has a different number."
- **The Blender (When Systems Get Mixed Before Anyone Knows What Each One Says)** (`cards/blender.md`): pitfall, Data Foundations. See each system alone before you put them together. Give every source system its own layer, one system at a time, in its domain: one call system, one website, one portal, one claims system.
- **Seven Versions of the Truth (When Nobody Can Say Which Data Is Good)** (`cards/seven-versions-of-the-truth.md`): pitfall, Data Foundations. Rate your data, promote one, retire the rest. Every domain needs one data product people can trust without asking, and a rating that says how far to trust it.
- **Planned Isn't In Stock (When an Agent Reads Data Nobody Defined)** (`cards/planned-isnt-in-stock.md`): pitfall, Data Foundations. Customer-facing agents read only from defined, trusted data. If a word matters to the business, write down what it means before an agent acts on it. At work: "Just point the agent at the shared drive."
- **Database Hieroglyphics (When Nobody Can Read Your Schema)** (`cards/database-hieroglyphics.md`): pitfall, Data Foundations. Name everything like you're explaining it to your grandmother—clear, complete, obvious. At work: "What does fact_trx_dtl_v3 even mean?"
- **A Logo Before the Data (When the Platform Is Really a Query)** (`cards/a-logo-before-the-data.md`): pitfall, Strategy & Focus. Name the data before you name the platform. Most big asks are a few kinds of data and one question nobody asked: joined around what?

## The frameworks

- **It Was Never About the Tech** (`frameworks/it-was-never-about-the-tech.md`): It Was Never About the Tech is the observation that analytics transformations fail on politics, people, and principles far more often than on tooling — the technology is rarely the binding constraint.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
