# The Data Export Trap (When Your Dashboards Are Just CSV Machines)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/52

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/52

## What it sounds like at work

"Can I get that as an export to Excel?"

## The problem

You built a beautiful dashboard. Charts, filters, drill-downs. Proud of it. Then you check usage analytics: 80% of users just click "Export to Excel" and leave. They're using your $500K BI platform as a glorified CSV generator. They do the actual analysis in Excel, not your dashboard. Why? Because your viz doesn't answer their question—it just dumps data. They rebuild everything in pivot tables anyway. It's like building a fancy restaurant where everyone orders takeout. You're not delivering anything people act on—you're delivering raw ingredients.

## The principle

Measure data export rate. If >40% of dashboard views end in data export, you built a data dump, not an analytics solution. Ask: why are they exporting? Usually because the dashboard doesn't show what they need. Fix the dashboard to answer the question OR accept that this use case needs direct data access (not a dashboard). The magic happens when export rate drops below 20% because users get their answers IN the dashboard. Think manufacturing: finished products, not raw materials.

## The steps

1. **Measure Export Behavior**

Track for every dashboard:
- Views
- Data exports (to Excel, CSV, etc.)
- Export rate = exports ÷ views

Flag dashboards with >40% export rate. Interview 5 users: 'Why do you export?'

Common reasons:
- Dashboard missing key dimension/metric
- Need custom calculations not built in
- Need data in different format
- Sharing with others (no dashboard access)

Different problems = different solutions.
2. **Fix or Kill High-Export Dashboards**

For each high-export dashboard, pick one:

**Option A: Fix the Dashboard**
- Add missing dimensions/metrics users need
- Build in their custom calculations
- Add better export formats if needed
Goal: Make the dashboard answer their question so they don't need to export.

**Option B: Build Data Access Instead**
- If users need raw data for ad-hoc analysis, give them direct data access (SQL, API, etc.)
- Kill the dashboard—it's not the right solution

Don't force dashboards on use cases that need raw data.
3. **Monitor Export Rate as Product Health**

Track export rate monthly:
- <20% = healthy (people act right in the product)
- 20-40% = investigate (might need fixes)
- >40% = problem (redesign or deprecate)

Goal: Get your portfolio average export rate below 25%.

If a dashboard stays >40% export rate after redesign attempts, it's the wrong solution. Give users direct data access and kill the dashboard.

## In practice

A retail analytics team had 52 dashboards with 67% average export rate. Users opened dashboards just to download CSVs, then did analysis elsewhere. The team asked 10 heavy exporters: "Why export?" Answers: "Dashboard doesn't show my stores," "I need to add calculations," "Can't compare to last year the way I need." They redesigned 15 high-export dashboards based on feedback. Added missing dimensions, calculations, time comparisons. Export rate dropped to 18% for those 15. For dashboards where users legitimately needed raw data (ad-hoc analysis), they built direct data access tools instead of pretending dashboards would work. Export rate became a product health metric: >40% = redesign or deprecate.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
