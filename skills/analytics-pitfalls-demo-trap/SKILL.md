---
name: analytics-pitfalls-demo-trap
description: "\"The Demo Trap\": a pitfall card from Analytics Pitfalls & Principles, by Brian Cariveau. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# The Demo Trap

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/66

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/66

## What it sounds like at work

"The AI demo went great. Leadership loved it."

## The problem

Your GenAI project demos brilliantly. Executives love it. The technology is impressive. The interface is elegant. The conversations feel natural.

But when you check the usage data, you find 47 total sessions in production—and 43 of them were from your team testing it.

You spent six months of engineering time and $180,000 in inference costs building a solution that solved the wrong problem exceptionally well. The real friction wasn't where you thought it was. Users didn't want a conversation; they wanted to complete a task as quickly as possible.

Your chatbot added eight minutes to a process that used to take three. It converted at 38% when the old process converted at 87%. And it cost $60,000 per month to run.

But it demos great.

## The principle

Demo success ≠ production value. The most impressive technology often solves problems that don't exist, while boring solutions fix problems that cost real money every day.

Before building any AI solution, validate three things:
1. The problem exists and is painful enough to change behavior
2. The AI solution is actually faster/better than what exists today
3. You're measuring adoption, not just engagement

Boring problems beat sexy solutions. Every time.

## The steps

1. **Measure problem frequency before solution coolness.** Don't ask 'Could we use AI for this?' Ask 'How many times per day does this problem cost us money?' If the answer is less than 10x per day, it's probably not worth automating.
2. **Start with the ugliest, most manual process.** If AI helps with something people already enjoy, you've added unnecessary complexity. If it helps with something people actively avoid, you've created real value.
3. **Demo to actual users before building, not after.** Show sketches and wireframes to 10 real users. If they don't immediately say 'This would save me so much time,' you're building the wrong thing.
4. **Track adoption weekly, not quarterly.** If usage isn't growing 20%+ week-over-week in the first month, you have a problem. Don't wait for quarterly reviews to discover nobody's using it.
5. **Compare to the status quo, not to nothing.** Don't ask 'Is this AI solution good?' Ask 'Is this AI solution better than what people do today?' Faster? Easier? Cheaper? If not, you're creating friction, not solving it.
6. **Set a kill date before you launch.** Decide in advance: 'If we don't have X active users by Y date, we shut it down.' Prevents the sunk cost fallacy from keeping bad projects alive.

## In practice

ClassicMotors built an AI listing assistant that helped sellers list their cars through natural conversation. It was impressive in demos—executives loved watching it adapt to different car types and ask intelligent follow-up questions.

The data told a different story:
- Completion rate: 38% (vs. 87% for traditional form)
- Average time: 8 minutes (vs. 3 minutes for form)
- Returning seller adoption: 6%
- Cost: $180,000 over three months

The problem? The form was never the friction point. Sellers already knew what information ClassicMotors needed. They wanted to paste their VIN, upload photos, and move on with their day.

The chatbot made them wait for the AI to ask questions they already had answers to. It turned parallel input (fill out multiple fields at once) into sequential conversation (answer one question, wait for next question).

Sarah Chen, VP of Analytics, killed the project after five weeks. The four engineers were reassigned to fix the Excel spreadsheet that actually ran the auction business.

The chatbot won an internal innovation award. The spreadsheet fix saved $2.4 million per year.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
