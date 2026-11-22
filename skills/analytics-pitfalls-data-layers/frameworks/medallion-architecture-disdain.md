# Medallion Architecture Disdain

A framework from Analytics Pitfalls & Principles, by Brian Cariveau.
https://www.analyticspitfalls.com/frameworks/medallion-architecture-disdain

## How to use this framework

Use it as a lens when someone's analytics or AI work touches what it describes.

1. Say which framework you are using and what it asks, in its one-line definition below.
2. Hold their work up to it: where it already fits, and where it does not. Be specific to their situation.
3. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
4. If one of the cards below names their problem more exactly, use that card as it says.
5. Finish with the framework's link: https://www.analyticspitfalls.com/frameworks/medallion-architecture-disdain

> Medallion Architecture Disdain argues that Bronze/Silver/Gold layer naming describes processing stage, not content — call it the Paint Department instead: raw, cleaned raw, system-specific and system-agnostic, names that tell you what is there.

## The problem hiding behind a tidy diagram

Bronze, Silver, and Gold sounds sophisticated on an architecture slide. It falls apart the moment a new analyst asks where customer data lives and gets sent to the Gold layer, where fourteen different tables have "customer" somewhere in the name and three different colleagues give three different answers about which one is actually correct. It turns out the real customer table lives in Silver, because Gold was never finished — a detail nobody wrote down anywhere, because the naming convention never asked anyone to.

Ask five teams what "silver" means and you'll get five answers. Metal-tier names describe processing stage: how refined the data is. They say nothing about content: what the data actually is. That distinction sounds academic until you watch a new hire lose their first two weeks just learning which layer holds what, purely because the labels were optimized to look organized in a diagram rather than to help a human find something.


## Name it like a hardware store, not a metallurgy chart

Replace processing-tier names with content-based ones. Four layers cover almost every business. Raw: exactly what the source system sent. Cleaned raw, where most teams put bronze: the same rows, with dates, time zones, money and codes in one standard format. System-specific, where silver usually sits: one system at a time, in its domain, so one call system, one website, one claims system. System-agnostic, the real gold: every system in a domain as one, with one definition, tied to the master data. Name tables layer first, then domain, system, thing and grain, in full words: system_specific_support_east_call_system_calls_daily, system_agnostic_support_calls_daily. Every name now answers "what's in here" on its own, without a meeting.

Little to no abbreviations, in every layer. Someone who opens the database should be able to read it without a lookup. Stupidly simple for humans is stupidly simple for agents: an AI reads the same names you do.

The test for whether this is working: ask five analysts where they'd look for a specific kind of data, with no documentation open. If they can guess correctly from the name alone, the naming succeeded. If they need to ask someone, it failed — no matter how elegant the underlying architecture is.


## It's a rename, not a rebuild

This is the quietly appealing part: the underlying architecture usually does not need to change at all. Same pipelines, same processing logic, same infrastructure — just names that tell a person what they will find instead of how far along the pipeline it traveled to get there. Teams that make this switch report onboarding time and "where's this data" support tickets both dropping substantially, without touching a single ETL job.


## Where to start

Audit whatever your current layer or zone names are, and be honest about whether a new hire could guess what's inside each one. If the answer is no, pick a content-based convention, apply it to your most-used tables first, and treat any newly built table that doesn't follow it as a code review rejection.


## Cards that go with it

- **Bronze, Silver, Gold Means Nothing (When Layer Names Don't Help)** (`../cards/bronze-silver-gold-means-nothing.md`), https://www.analyticspitfalls.com/cards/61
- **Cleaning the Same Dates Every Morning (When Every Query Fixes Raw Data Again)** (`../cards/cleaning-the-same-dates-every-morning.md`), https://www.analyticspitfalls.com/cards/86
- **The Blender (When Systems Get Mixed Before Anyone Knows What Each One Says)** (`../cards/blender.md`), https://www.analyticspitfalls.com/cards/87
- **One System in a Gold Costume (When "All of It" Is Really the Biggest System)** (`../cards/one-system-in-a-gold-costume.md`), https://www.analyticspitfalls.com/cards/88

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
