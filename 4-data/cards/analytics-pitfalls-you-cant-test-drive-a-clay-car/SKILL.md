---
name: analytics-pitfalls-you-cant-test-drive-a-clay-car
description: "\"You Can't Test Drive a Clay Car\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# You Can't Test Drive a Clay Car: Why Fake Data Kills Innovation

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/42

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/42

## The problem

Your team wants to innovate. Build new models. Test AI capabilities. Leadership says: "Great! Set up a sandbox with fake data."

Six months later, you've built pipelines that work beautifully on made-up scenarios. Models that perform perfectly on fake problems. Dashboards that look impressive in demos.

Then you point it at production data and everything breaks.

Why? Because the innovation isn't in the pipeline you built. It's in the **outcome** that pipeline produces. And you can never see real outcomes with fake data.

It's like sculpting a sports car out of clay and thinking you get to drive it when you're done.

## The principle

Real innovation requires real data, secured properly.

You don't need fake data. You need production data with proper access controls, data masking where necessary, and security that actually works.

The risk isn't using production data. The risk is building solutions on fake problems and discovering they don't solve real ones.

## The steps

1. **Build Your Innovation Pipeline on Production Data**

Use actual customer behavior, real transaction patterns, genuine edge cases. Implement data masking for PII/sensitive fields where required. Set up proper access controls and audit logging. Test on the data you'll actually use.
2. **Stop the Fake Data Theater**

Before investing in fake data generation, ask teams: "How will you use this?" If the answer is "sounds cool, but we're good with test subsets," skip it. Fake data takes 6+ months to build and nobody ends up using it. Use anonymized production samples instead.
3. **Secure Production, Don't Avoid It**

Invest in proper data governance and access controls. Implement column-level encryption and row-level security. Use data masking policies for sensitive fields. If you really need to obfuscate, de-identify the data—it's still real information, still behaves like production, just without the PII. Build secure innovation environments, not fake ones.

## In practice

A Fortune 500 company spent six months building a "sandbox" with fake data for their AI innovation team. They generated synthetic transactions, made-up customer behaviors, perfectly balanced datasets.

The models worked beautifully. Accuracy scores above 95%. Leadership was thrilled.

Then they pointed the models at production data. Everything collapsed. The fake data had no edge cases, no data quality issues, no real-world chaos. The models had learned to solve problems that didn't exist.

They scrapped the entire effort and started over—this time with properly secured production data, masked PII, and real problems. The new models weren't as "accurate" on paper, but they actually worked in the real world.

The lesson: You can't test drive a clay car. Innovation needs real data, secured properly.

## Inspired by

Dean Furness, who's been expanding the halo effect for 15 years—sharing insights, challenging assumptions, and helping teams cut through the fake data theater to build real innovation on real problems. This is what analytics teams need: people helping people.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
