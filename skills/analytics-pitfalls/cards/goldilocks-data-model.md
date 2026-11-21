# The Goldilocks Data Model (Too Hot, Too Cold, Never Just Right)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/21

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. If the card doesn't fit, say so plainly. Don't stretch it.
5. Finish with the card's link: https://www.analyticspitfalls.com/cards/21

## The problem

Two extremes plague analytics teams: (1) Data left unmodeled or haphazardly modeled, hindering scalability and usability, or (2) Data over-engineered, slowing progress and confounding even seasoned analysts. Fresh talent joins eager to build, only to hear "our data's a hot mess—expect to spend 70% of your time wrestling with it." Both extremes leave data harder to use, not easier. You can't achieve Analytics Powerhouse status without adhering to basic data modeling principles.

## The principle

A data model has ONE job: make data easier to use for those crafting solutions with it—the BI analysts and data scientists. Ask ruthlessly: "Does this model make the data easier to use—yes or no?" If yes, everything else (integration, quality monitoring, predictability, security) becomes way easier to pull off. Strive for "stupidly simple" data—so intuitive it's like picking a book off a shelf and instantly grasping its contents. Slow down just enough to speed up.

## The steps

1. Ask the Brutally Simple Question: For every table/column, ask: "Does this make data easier to use?" If no, simplify it. If yes, document why.
2. Onboard Test: Have a new analyst try to find data without help. Time them. If it takes >15 minutes to find common data, your model is too complex. Simplify.
3. Build a Data Catalog: Document your tables, columns, relationships in plain English. Make it searchable. New people should find what they need in seconds, not hours.

## In practice

A Fortune 100 retailer had 847 tables in their data warehouse with no naming conventions, no documentation, and cryptic abbreviations. New analysts spent 6 months learning the maze before being productive. They rebuilt using simple principles: clear naming (sales_transactions, not sls_txn_f47), logical grouping by domain, one source of truth per metric. Onboarding time dropped from 6 months to 3 weeks. Data science team velocity tripled. The "stupidly simple" redesign took 4 months but paid back in saved time within 90 days.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
