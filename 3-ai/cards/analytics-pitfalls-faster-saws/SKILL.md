---
name: analytics-pitfalls-faster-saws
description: "\"Faster Saws\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# Faster Saws (Every Step Got Faster, and the Customer Still Waits)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Second Factory*, Brian Cariveau's next novel (https://www.analyticspitfalls.com/second-factory).
https://www.analyticspitfalls.com/cards/80

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/80

## The problem

Every team in the process has an AI story it's proud of. Verification went from half a day to twenty minutes. Pricing went from an afternoon to a few minutes. Reconciliation runs overnight now, in seconds.

And the customer waits exactly as long as they did last year.

The time was in the waiting between the steps, and nobody's AI story touched that. The Tuesday meeting. The twice-a-week payment run. The sign-off somebody added after a mistake years ago. The file sitting in a queue until the next person gets to it. Sensible answers to problems that no longer exist. That's organizational debt, and AI doesn't pay it down by itself. You can pay off every bit of your technical debt and still owe all of it.

## The principle

Faster stations aren't a faster factory. Walk one real order through the business, color the work blue and the waiting red, and the red wins by a mile almost every time.

So stop speeding up the stations and redesign how the work moves between them. Start from zero. If you built this process today, with agents in it from the first minute, what has to be true? Which of those things genuinely needs a person to decide? Let the work move itself everywhere else, and bring people together only at those few decision points. Engineers call it orchestration. In plain words, it's deciding who waits for whom, on purpose.

It rarely needs a new tool. The hard part is getting seven teams to agree to work differently.

## The steps

1. **Follow one order end to end.** Pick one real customer order from last month and pull every timestamp from every system it touched. Not a sample: one order, all the way through.
2. **Color it blue and red.** On a wall, blue for anyone, person or agent, actually doing work, and red for waiting. Add up each color. Show it to the team leads together, and let them read it before anyone talks.
3. **Ask what has to be true.** Wipe the board. If you started this business today, what has to be true for the order to be done? Then ask which of those needs a person to decide. Everything else is moving the file.
4. **Pilot one pod.** A small cross-team group, one agent following each order instead of each team, and one short daily meeting where the people who decide, decide. A few weeks, a few dozen orders, everything else unchanged.

## In practice

A seller sold his 1957 Ranchero through ClassicMotors and got paid twenty-three days after he first called. He was thrilled with the price. He called four times to ask where his money was. Everybody was very nice. Nobody could tell him.

The auction itself takes a week. So Nora Berg asked the data team to pull everything about that one car: every system, every person who opened the file, every timestamp. It lived in seven systems that didn't talk to each other, and two of the handoffs had happened by email.

She took blue and red sticky notes up to the catwalk. Blue for work, red for waiting. Verification: twenty minutes, then five days waiting for an inspector. Inspection: half a day, then four days waiting for the Tuesday pricing meeting. Pricing: a few minutes, then three days waiting for Monday's auction lists. The payout, matched overnight by an agent, then two days waiting for the twice-weekly payment run.

Outside the auction: sixteen days, about a day and a half of them blue.

Every team on that wall was faster than a year ago. Some were ten times faster. A year ago, the median wait had been twenty-four days.

"We all bought faster saws," said the man who ran transport. The payment run was twice a week because that was how the bank file used to work. It hadn't worked that way for three years.

## Inspired by

Chapter 11 of The Second Factory, "Twenty-Three Days." And Eliyahu Goldratt's The Goal: every system has one constraint, and speeding up anything else just piles up work in front of it.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
