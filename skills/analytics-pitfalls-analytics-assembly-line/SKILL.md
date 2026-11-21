---
name: analytics-pitfalls-analytics-assembly-line
description: "\"The Analytics Assembly Line\" (Why Your Data is Just Raw Materials): a principle card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project needs it."
license: CC-BY-4.0
---

# The Analytics Assembly Line (Why Your Data is Just Raw Materials)

A principle card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/22

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work could use this principle.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/22

## The problem

Most analytics teams think they're in the data business. Wrong. You're in the manufacturing business. Every piece of data is raw material sitting on the left side of your warehouse. Every dashboard, AI model, and insight is a finished product that either flies off the shelves or gathers dust. But here's the problem: most teams run their "factory" like chaos—no quality control on raw materials (garbage data), machines that break constantly (brittle pipelines), and products nobody ordered (dashboards nobody uses). It's a manufacturing line with 80% waste. You wouldn't tolerate that in a real factory. Why tolerate it in analytics?

## The principle

Treat your data ecosystem like a clean manufacturing line with zero waste. Raw materials (data) enter on the left—inspect for quality, reject defects. Machines in the middle (pipelines, transformations, models) turn materials into products—monitor uptime, optimize efficiency. Finished products on the right (dashboards, insights, AI) ship to customers—track usage, kill what doesn't sell. Measure yield at every step: what percentage of raw data becomes valuable insights? What's your waste rate? The magic happens when you eliminate waste, optimize flow, and only make products people actually want. That's how you become a powerhouse.

## The steps

1. Map Your Factory: Draw it out. Raw materials (data sources) on left. Machines (pipelines/transforms) in middle. Products (dashboards/insights) on right. Calculate your yield.
2. Implement Quality Gates: Reject bad data at ingestion. Don't let garbage enter your warehouse. Monitor pipeline uptime like you monitor systems - target 99%+.
3. Track Product Usage: Every "product" (dashboard, model, insight) needs usage metrics. Kill anything with <10 weekly active users. Free up capacity for products people want.

## In practice

A retail analytics team was drowning: 200 data sources, 80 pipelines breaking weekly, 60 dashboards with 12% adoption. New leader walked in, drew the factory: "Raw materials on left, products on right, what's our yield?" Answer: 12%. Brutal. They rebuilt: (1) Quality gates—reject bad data at ingestion, 95% fewer downstream issues. (2) Streamlined middle—80 pipelines became 35, uptime from 60% to 99%. (3) Product discipline—killed 40 unused dashboards, focused on 20 high-adoption ones. Yield jumped to 68% in 6 months. Team freed up 50% capacity from firefighting. That's the manufacturing mindset in action.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
