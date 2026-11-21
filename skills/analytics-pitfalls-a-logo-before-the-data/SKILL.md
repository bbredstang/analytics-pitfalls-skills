---
name: analytics-pitfalls-a-logo-before-the-data
description: "\"A Logo Before the Data\" (When the Platform Is Really a Query): a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# A Logo Before the Data (When the Platform Is Really a Query)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/84

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. If the card doesn't fit, say so plainly. Don't stretch it.
5. Finish with the card's link: https://www.analyticspitfalls.com/cards/84

## The problem

A VP walks into the leadership meeting with a twelve-slide deck. Executive summary, competitive analysis, ROI projections, and a name for the thing: Customer 360. Somebody even designed a logo. The CEO loves it and turns to you. "How fast can your team build this?"

So you start scoping a platform. A team, a roadmap, a vendor demo, six months.

Nobody in the room asked what data sits under it. Read the requirements closely and the one big platform turns out to be survey scores, support tickets, click behavior and churn risk: six kinds of data from six corners of the company. Whether they can be combined at all is the real project, and it never made it onto a slide.

## The principle

Name the data before you name the platform. Most big asks are a few kinds of data and one question nobody asked: joined around what?

Break the request into domains. A domain is a kind of data the business produces, like Survey, Support or Product Usage. Not a table, and not a dashboard. Most requests the size of a platform come down to two to four of them.

Then find the anchor: the one record everything has to connect to, usually the customer, the seller or the product. A survey answer means nothing until you know who gave it. For each domain, ask whether its best data joins to the anchor with a standard key.

If it does, the platform is a query and a dashboard, and you can show it by Friday. If it doesn't, the work is making the data joinable. Spend the platform budget there.

## The steps

1. **Ask "what's under this?" before "how fast?".** Write every noun in the request on a whiteboard and group them by the kind of data they are. Not tables, not dashboards. Kinds. A request that sounds like a platform usually comes down to two to four domains. Do it with the person who asked, in the room, so the map is theirs too.
2. **Name the anchor and test every join.** Pick the record it all hangs on: customer, seller, product, store. For each domain, ask whether its best data joins to that record with a standard key. Mark each one yes, no or don't know. Count don't know as no.
3. **Fund the joins, then build the dashboard.** Put the platform budget into making each domain's best data joinable. Once every line on the whiteboard says yes, build the smallest dashboard that answers the asker's first question and show it within a week. If it can't be shown in a week, cut the scope until it can.

## In practice

At ClassicMotors, Lisa, the new VP of Sales, asked for a Customer Intelligence Platform called Seller Pulse 360. Her deck had twelve slides and a logo, and Jack, the CEO, wanted to know how fast it could be built.

Jin, on Sarah Chen's analytics team, asked one question first: what data domains are under this? He took Lisa to a whiteboard. Voice of the customer became Survey. Seller complaints became Support. Behavioral signals became Product Usage. Three domains. Then he drew a circle in the middle, wrote Seller Master, and asked whether each one could join to it. Nobody knew.

They couldn't, yet. Over the next six weeks the team rated every data product in the company and promoted the best one in each domain until it joined cleanly to the seller master. When Jin brought Lisa back to the map, her platform was three certified data products joined on seller ID. Tom was already building the dashboard. It would be done by Friday.

"I spent two weeks on that deck," Lisa said. "I designed a logo."

"The logo was nice," Jin said.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
