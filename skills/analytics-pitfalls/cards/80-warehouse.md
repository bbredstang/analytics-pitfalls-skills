# The 80% Warehouse (When Most of Your Data Just Sits There)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/60

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. If the card doesn't fit, say so plainly. Don't stretch it.
5. Finish with the card's link: https://www.analyticspitfalls.com/cards/60

## The problem

Your data warehouse has 847 tables. You're proud of it—years of work, terabytes of data, every system integrated. Then you check usage analytics: 680 tables haven't been queried in 90+ days. That's 80% of your warehouse sitting unused. Like a manufacturing plant with a giant warehouse where 80% of inventory just gathers dust—never moving to production, never creating value. Worse: you're paying to store it, maintain it, back it up, and document it. Every new table you add makes the problem worse. Users can't find what they need because they're drowning in unused tables. Your warehouse isn't an asset—it's a graveyard consuming resources.

## The principle

Track data usage like inventory turnover. Manufacturing plants obsess over "inventory turns"—how fast raw materials move through the system. If something sits >90 days, they investigate: Why isn't this moving? Should we stop ordering it? Same with data. Instrument your warehouse: track queries per table, last access date, who uses what. Set a rule: Tables unused for 90 days get flagged for review. At 180 days with zero usage, they get archived or deleted. The magic happens when you treat data like physical inventory—if it's not moving, it's waste. Build for 80% usage rate (only 20% unused at any time), not 20% usage rate (80% waste).

## The steps

1. **Instrument Your Data Warehouse**

Track for every table:
- Last query date
- Queries per day/week/month
- Distinct users querying it
- Rows actually read (not just table scanned)

Build a simple dashboard:
- Tables by days since last use
- Usage rate % (tables used in last 90 days)
- Storage cost by usage tier

Goal: Know exactly which 80% of your data is waste.
2. **Implement Usage-Based Lifecycle**

Create usage tiers:
- **Active**: Used in last 30 days (keep as-is)
- **Stale**: 30-90 days unused (yellow flag, notify owners)
- **Expired**: 90-180 days unused (red flag, archive candidate)
- **Dead**: 180+ days unused (archive immediately)

Monthly review: Archive or delete tables in Expired/Dead tiers.

Exception process: If owner makes case for keeping unused table, they must commit to using it within 30 days or it gets archived.
3. **Measure Inventory Turns**

Calculate warehouse health metrics:
- **Usage rate**: % of tables queried in last 90 days (target: 80%+)
- **Storage efficiency**: GB used ÷ GB total (target: 70%+)
- **Data debt**: # of tables ×  days since last use (target: declining)

Track monthly. Set goal: 80% usage rate within 6 months.

Celebrate wins: "We archived 200 unused tables this quarter and nobody noticed!"

Bonus: New tables require usage projections. If not used within 90 days of launch, they're candidates for immediate deletion.

## In practice

A Fortune 5 healthcare company's data team had 1,200+ tables in their enterprise warehouse. Data engineers were proud of the coverage. Then new VP asked: "What's our data usage rate?" They instrumented the warehouse: tracked every query, every table access. Results were brutal: 73% of tables had zero queries in the past 90 days. 897 tables completely unused. Storage cost: $180K/year just for unused data. Maintenance burden: engineers spent 40% of time supporting tables nobody used. They implemented a usage-based lifecycle: Yellow flag at 60 days unused, Red flag at 90 days, Archive at 120 days unused. First pass: archived 520 tables (43% of warehouse). Users didn't notice—because nobody was using them anyway. Six months later: warehouse down to 420 tables, usage rate at 82%, storage costs cut 60%, engineers focused on high-value work. The warehouse went from graveyard to efficient inventory system.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
