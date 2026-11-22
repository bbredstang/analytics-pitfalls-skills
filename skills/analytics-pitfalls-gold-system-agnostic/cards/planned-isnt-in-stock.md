# Planned Isn't In Stock (When an Agent Reads Data Nobody Defined)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Second Factory*, Brian Cariveau's next novel (https://www.analyticspitfalls.com/second-factory).
https://www.analyticspitfalls.com/cards/68

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/68

## What it sounds like at work

"Just point the agent at the shared drive."

## The problem

A marketer builds an agent that finds owners of a particular car and emails them about parts. Everyone cheers. It's exactly the kind of builder you hoped for.

Nobody notices where it gets its information. It's pointed at a shared folder, and inside is the product roadmap: every part the team plans to make, with target dates. The agent reads "tail-light lens, Q2" and concludes, perfectly reasonably, that you sell tail-light lenses. So it tells hundreds of customers they're in stock.

Every person in the building knows the difference between planned and in stock. Nobody ever wrote it down, because nobody had to. An agent only knows what's been written down, and it acts on whatever it reads at full speed.

## The principle

Customer-facing agents read only from defined, trusted data. If a word matters to the business, write down what it means before an agent acts on it.

Planned, in production, on order and in stock are four different things. People learn the difference in their first month. Agents learn it from a definition or not at all. So define the words that carry promises (in stock, available, delivered, eligible, active), put each definition next to the data it comes from, and give it an owner.

Then draw a line. Anything that talks to a customer reads from certified data only, three stars or better. No roadmaps. No shared folders. Just the truth.

## The steps

1. **List the words that carry promises.** In stock, available, delivery date, refund window, eligible. Write a plain-English definition of each, pointing at the data it comes from, with an owner.
2. **Draw the three-star line.** Anything that talks to a customer reads from certified data only. No shared folders, no roadmaps, no exceptions on request.
3. **Ask what every agent reads.** For each customer-facing agent, list its sources. Anything you can't name is a promise waiting to go wrong.
4. **Correct it honestly.** When one does go wrong, tell customers the truth, short and in plain English, and offer them a place in line.

## In practice

Lena Brooks, a campaign manager at ClassicMotors, built her first agent in one of the company's AI sessions. It found owners of a particular model in the auction data, wrote each of them a personal email and sent it. She showed it off in the company's AI channel. It got forty reactions.

She'd pointed it at a shared folder called Parts Launch, where the parts team kept its roadmap. The agent read "1967 Shelby GT500 tail-light lens, Q2" and told nine hundred and fourteen Shelby owners the lenses were in stock. By nine that night, a hundred and forty-one had replied and twenty-three had tried to order. One wrote, in capital letters, I HAVE BEEN LOOKING FOR THESE FOR ELEVEN YEARS.

"Nobody told it the difference between planned and real," Lena kept saying.

"Nobody told it because nobody's told anyone," Nora said.

At the board meeting the next day, the lead independent director mentioned she'd had the email. She owned a 1967 Shelby.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
