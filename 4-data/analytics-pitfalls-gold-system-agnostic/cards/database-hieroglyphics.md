# Database Hieroglyphics (When Nobody Can Read Your Schema)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/29

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/29

## What it sounds like at work

"What does fact_trx_dtl_v3 even mean?"

## The problem

Walking into a data warehouse and seeing table names like "cst_prf_x_loc_dim" is like reading ancient hieroglyphics without a Rosetta Stone. Nobody knows what it means. New analysts spend weeks deciphering the cryptic abbreviations. "sls_txn_f47"? Is that sales transactions fact table 47? Or sales tax new framework 47? Who knows? The team that built it left years ago. Now you're stuck with a metadata mess that requires a 200-page glossary just to understand what data you have. It's expensive, slow, and dumb.

## The principle

BAN ABBREVIATIONS ENTIRELY: Name everything like you're explaining it to your grandmother—clear, complete, obvious. "customer_profile_crosswalk_location_dimension" beats "cst_prf_x_loc_dim" every single time. Yes, it's longer. Yes, it takes more characters. But you know what? Developers onboard faster. AI tools actually work. Analysts build models without asking "what does this column mean?" seventeen times.

The best documentation is code that doesn't need documentation. When your schema is self-explanatory, you stop wasting time on glossaries, metadata tools, and tribal knowledge. You start shipping value.

Make it stupidly simple. If a new hire can't guess what a table contains from its name, you failed. Think manufacturing: you wouldn't label raw materials with cryptic codes and expect workers to be productive. Same here. Clarity is speed.

## The steps

1. Ban Abbreviations Starting Today: New tables/columns get full names. "customer_profile" not "cst_prf." Make it a code review requirement. No exceptions.
2. Rename Top 20 Tables: Pick your 20 most-used tables with cryptic names. Rename them during next migration. Document before/after. Train team on new names.
3. Build a Naming Convention Guide: Document the standard: table_name format, column_name format, examples. Make it a 1-pager. Post it where everyone can see it.

## In practice

A Dutch architect joined a Fortune 100 retail company and was horrified by the schema. "cst_prf_x_loc_dim"? "sls_txn_f47"? "inv_adj_tmp_stg"? He couldn't make sense of it. Forced one rule on the team: zero abbreviations going forward. Everything gets renamed during the next migration.

Six months later: "cst_prf_x_loc_dim" became "customer_profile_crosswalk_location_dimension". "sls_txn_f47" became "sales_transactions_fact". "inv_adj_tmp_stg" became "inventory_adjustments_temporary_staging". 

New developers onboarded in 2 weeks instead of 6 months. But here's the shock: AI velocity tripled. GPT-4 could read the schema and write accurate queries on the first try. Analysts built models without Slack messages asking "what does this mean?" 

The team that resisted ("it's too long!") eventually admitted defeat. Simple names compounded value across everything. One rule changed everything.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
