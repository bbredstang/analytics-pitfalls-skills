---
name: analytics-pitfalls-wild-west-of-data
description: "\"The Wild West of Data\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# The Wild West of Data (When Everyone Does Whatever They Want)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/10

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/10

## What it sounds like at work

"Finance has a different number."

## The problem

Sales has their own definition of "customer." Marketing has a different one. Finance has a third. Three teams, three different numbers for "total customers." Executives get confused. Trust erodes. Every meeting turns into a definitional debate instead of a decision-making session. Or worse: anyone can access any data, PII is flying around in Slack, compliance is a nightmare, and you're one audit away from a massive fine. It's the Wild West—no rules, no standards, no control. It's like a manufacturing plant where every shift uses different specs for the same product. Some batches are perfect, some are disasters, and nobody knows which is which until customers complain.

## The principle

Set clear rules and enforce them. Define metrics once, centrally, and make that the source of truth. Control data access—not everyone needs to see everything. Audit who's accessing what. Document everything. Make governance boring and systematic, like quality control in manufacturing. The magic happens when everyone uses the same definitions, trusts the same numbers, and can actually make decisions instead of arguing about whose spreadsheet is right. Less chaos, more consistency. That's how you build trust in data.

## The steps

1. Define Metrics in One Place: Pick your top 10 metrics. Lock everyone in a room. Agree on ONE definition per metric. Document it. Build it into the data warehouse as the source of truth.
2. Implement Role-Based Access: Audit who has access to what data. Implement least privilege - people only see what they need. PII should be locked down tight.
3. Monthly Governance Review: Review data access logs monthly. Who accessed what? Any anomalies? Any policy violations? Make governance boring and systematic, like quality control.

## In practice

A SaaS company had 7 different definitions of "active user" across teams. Product said "logged in this month." Sales said "paid subscription." Customer Success said "used a core feature." Exec dashboard pulled from all three sources and showed conflicting numbers every week. CEO lost faith in analytics. New Chief Data Officer came in, locked everyone in a room, forced one definition: "Active user = logged in AND used a core feature in the past 30 days." Built one source of truth in the data warehouse. Killed all competing reports. Initially, teams complained. Six months later, decision-making speed doubled because nobody wasted time reconciling numbers. Investor board meetings became data-driven instead of data-debated. Trust in analytics went from 20% to 85%. One definition changed everything.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
