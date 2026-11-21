---
name: analytics-pitfalls-statistician-who-drowned
description: "\"The Statistician Who Drowned\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# The Statistician Who Drowned (in a River with Average Depth 3 Feet)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/7

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. If the card doesn't fit, say so plainly. Don't stretch it.
5. Finish with the card's link: https://www.analyticspitfalls.com/cards/7

## The problem

A statistician drowned crossing a river with an average depth of 3 feet. How? Parts of it were 12 feet deep. Averages hide the extremes. Your average customer spends $50—great! Except 90% spend $5 and 10% spend $500. Those are two completely different customers who need different strategies. But if you only look at the average, you optimize for nobody. Same in manufacturing: average defect rate of 2% sounds fine until you realize one production line is at 0.1% and another is at 15%. Averages smooth out the truth. They make you comfortable when you should be alarmed. They hide the gold (power users) and the disasters (broken processes).

## The principle

Dig into the distribution, not just the average. Look at medians, percentiles, outliers. Segment your data—what's the average for each customer type, region, or product line? In manufacturing, you wouldn't just track overall output—you'd monitor each machine, each shift, each operator. Same here. The magic happens when you stop asking "what's the average?" and start asking "what's the spread?" That's where you find opportunities to fix disasters and double down on winners. Less averaging, more slicing. That's how you see the truth.

## The steps

1. Always Look at the Distribution: For any metric you track, pull the distribution. Not just the average - show min, max, median, 25th/75th percentiles. Make it a standard in every report.
2. Segment Everything: Break down averages by customer type, region, product line, whatever matters. Build dashboards that show segments by default, not just totals.
3. Ban "Average" Without Context: Institute a rule: Nobody can present an average without also showing the distribution or key segments. Force people to see the spread.

## In practice

An app had an "average session length" of 8 minutes. Product team celebrated—users are engaged! Then someone looked at the distribution. 60% of sessions were under 30 seconds (people opening the app by accident). 30% were 2-3 minutes (quick tasks). 10% were 45+ minutes (power users binging content). Three totally different behaviors masked by one average. They segmented: built a better onboarding flow for the 30-second folks (converted 40% to 2+ minutes), optimized quick tasks for the 2-3 minute users (task completion up 50%), and built binge-worthy features for power users (session length jumped to 90 minutes). Revenue tripled in 6 months. All because they stopped looking at averages and started looking at reality.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
