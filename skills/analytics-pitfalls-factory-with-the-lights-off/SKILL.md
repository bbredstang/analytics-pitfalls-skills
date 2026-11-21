---
name: analytics-pitfalls-factory-with-the-lights-off
description: "\"The Factory With the Lights Off\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# The Factory With the Lights Off (When Nobody Can See the Agents)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Second Factory*, Brian Cariveau's next novel (https://www.analyticspitfalls.com/second-factory).
https://www.analyticspitfalls.com/cards/73

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/73

## What it sounds like at work

"I built my own agent for that."

## The problem

You told everyone to build, and they did. Hundreds of skills and agents in two months. That's what you wanted.

Then something goes wrong, and Legal asks the obvious question: how many agents do we have? Nobody knows how many are running, what they read, who owns them or whether anyone uses them. When you finally pull the logs, it's worse than you imagined. Dozens with no owner, because the people who built them changed jobs. Dozens of near-copies of the same weekly report helper. Several versions of the same policy, giving customers different answers.

And the number that matters most: plenty of people use what they built themselves, and hardly anyone uses what a colleague built. That's twenty one-person companies in every department, all with the lights off.

## The principle

Turn the lights on. Every agent and shared skill goes on a screen, with an owner, a backup and a usage count.

After a scare, the instinct is to freeze everything. Don't. The builders won't stop building. They'll just stop telling anyone. Make it visible instead, then ask the questions you'd ask about dashboards: who uses it, and what does it drive?

Build the registry from the platform's own logs, not from forms. Give every orphaned agent thirty days to be adopted or switched off. Merge the duplicates into one shared skill with an owner, and let whoever thinks theirs is better make the shared one better. Then watch two numbers: people using what they built, and people using what someone else built. The gap between them is your next bottleneck.

## The steps

1. **Count from the logs.** How many agents people think you have, against how many the logs say. Then the share with a named owner and a backup.
2. **Put them on a screen.** What each one does, its owner, what data it reads, what it can do and who uses it, where everyone can see.
3. **Adopt or switch off.** Thirty days for every orphan. Most won't be missed.
4. **Merge the duplicates.** One shared skill per job, with an owner who signs off on every line. Anyone who thinks theirs is better gets to make the shared one better.
5. **Watch the two numbers.** Using what they built against using what others built. A high first number and a low second one means one-person companies and no team.

## In practice

The morning after an agent emailed hundreds of customers about parts ClassicMotors didn't have yet, the general counsel and the head of IT were waiting outside the CEO's office. "We need to stop every agent in the company," the general counsel said. "Today."

"How many agents would you be freezing?" Nora asked. Nobody knew. She asked for until Friday to turn the lights on.

Jin Park put it plainly on the catwalk. "We spent two years putting lights on this floor, and then we built a second factory right next to it and left the lights off."

On Friday, the new screens went up. Agents running: 612. With no owner: 74. Talking to customers: 41, nineteen of them reading from data rated under three stars. Thirty-eight versions of a weekly report helper. And two lines Nora read over and over. People using a skill or agent they built themselves: 23%. People using one someone else built: 4%.

"I told everyone to become a one-person company," Nora said.

"You told everyone to climb the ladder," Jin said. "They did. They just all stopped at rung three."

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
