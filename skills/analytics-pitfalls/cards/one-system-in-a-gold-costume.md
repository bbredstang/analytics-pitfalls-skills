# One System in a Gold Costume (When "All of It" Is Really the Biggest System)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/88

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/88

## The problem

The integrated layer is supposed to be the whole picture: every call system, every website, every marketing source, as one. It says so on the slide.

Look closer and it's the biggest system, with the others bolted on. The big system's definitions, the big system's codes, the big system's customer IDs. The smaller systems are squeezed to fit, or left out because they didn't join.

So "total calls" is really "calls from the main system, plus whatever matched." Finance's number is different, and nobody can say why.

## The principle

System-agnostic means every system, one definition. Most teams call it gold. It's the layer the business, the dashboards and the AI agents read, so it has to be all of it, one way.

One definition of each thing that matters, agreed and owned, with each system's own rule mapped to it in the open. One shared list of codes. The source system kept on every row. The master data as the anchor, so one customer who showed up in two systems is one customer. And names in full words: an agent can only use what it can read without a lookup.

Certify it before anyone builds on it. Three stars is the line: owned, tested, documented, and joined to the master data. Four stars, checked against business outcomes, before it goes to the board or trains a model.

## The steps

1. **Count the systems.** For one domain, list every system that feeds it and every system that is actually in the integrated table. Any gap is the first thing to fix.
2. **Agree one definition, in the open.** Put the owners of each system in one room and agree what each thing means across all of them. Write down where each system’s own rule differs and how it maps.
3. **Anchor it and certify it.** Match through the master data, keep the source on every row, and rate it. Nothing gets built on it below three stars.

## In practice

A claims team's "enterprise" claims table came from the largest of three claims systems. The other two were joined on a policy number that matched only about 70% of the time, and the misses quietly disappeared. The table undercounted claims by 12%, and the gap showed up first in Finance's reconciliation.

They counted the systems in the domain against the systems in the table, matched every claim through the member master instead of the policy number, and wrote down one definition of an open claim across all three. The gap closed to under 1%, and the table got its third star.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
