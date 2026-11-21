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

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/62

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

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
