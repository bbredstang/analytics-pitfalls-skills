---
name: analytics-pitfalls-is-it-right
description: "\"Is It Right?\" (The Wrong Question to Ask of AI): a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# Is It Right? (The Wrong Question to Ask of AI)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Second Factory*, Brian Cariveau's next novel (https://www.analyticspitfalls.com/second-factory).
https://www.analyticspitfalls.com/cards/82

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. If the card doesn't fit, say so plainly. Don't stretch it.
5. Finish with the card's link: https://www.analyticspitfalls.com/cards/82

## The problem

Software is supposed to do the same thing every time. Same input, same output. So when AI answers the same question two different ways, it feels broken.

People respond in one of two ways. Some check everything, by hand, forever. Others decide it's been fine for a while and stop checking at all. Both are managing AI like software, when it now behaves much more like a factory: the output varies.

And when something does go wrong, the instinct is to tinker. Change the instructions after a bad week, then change them again. Half the time you're fixing things that weren't broken, and the answers get worse.

## The principle

Ask whether it's within tolerance, and how you know. Nothing is right every time, in a factory or in AI.

Engineers who make real things never expected two bolts to come out the same. They decide how much variation they can live with, measure a sample instead of everything, and chart it over time. Walter Shewhart and W. Edwards Deming taught us to tell two kinds of wobble apart. Common cause is the process being a process. Special cause is one specific thing breaking. Treat everyday wobble as a break and you start fiddling. Treat a real break as wobble and you miss it.

Seen this way, an eval is just quality inspection. Keep a set of questions with known right answers and run them every time a skill changes. Then sample what the agent does in production, score it against a short checklist, and put the scores on a chart.

## The steps

1. **Pick one agent.** One that talks to customers, runs at real volume and isn't the riskiest. Name an owner.
2. **Write a short checklist.** Five to seven yes-or-no checks a good answer has to pass, short enough to score one in under a minute. Write it with someone from the front line, not just Legal.
3. **Collect a baseline before you set limits.** Sample twenty to fifty answers a day for three or four weeks. An AI judge can help score them, and a person makes the call. Only then draw the center line and the limits.
4. **Decide what a break sets off.** Three dots in a row below the line, or one far outside it, means someone looks within the hour.
5. **Fix the skill, not just the answer.** When the chart catches something, add it to the test questions, so the next time it fails in testing instead of in front of a customer.

## In practice

Teresa Vang spent twenty-two years making bolts for airplanes, then took a job as the quality engineer at the small factory that makes ClassicMotors' parts. For two years almost nobody listened to her. Every bad week, the machinists adjusted something, then something else, and the parts got worse.

She set a bolt on the break-room table. "No two of these are the same. Not one. Ever." Then she drew a chart on a napkin: a line down the middle, limits above and below, dots wobbling between them. "If a dot jumps outside these lines, or seven in a row creep up on one side, something specific has gone wrong. And now you know where to look."

Driving home with the napkin on the passenger seat, Nora Berg remembered the head of IT months earlier, frustrated, when the AI first started making things up. "Software's supposed to do the same thing every time. You put the same thing in, you get the same thing out. That's the whole point of software."

Teresa had never once expected two bolts to come out the same. The real question was hers. Is it within tolerance? And how do we know?

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
