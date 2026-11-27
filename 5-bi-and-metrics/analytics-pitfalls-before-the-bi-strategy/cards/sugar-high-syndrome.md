# The Sugar High Syndrome

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/30

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/30

## The problem

Building sexy ML models and fancy dashboards that nobody actually uses to run their business. You get punch drunk on the "sugar high" of data - shiny tools, impressive demos, cool technology - but it's easy to crash when you realize you've created expensive shelf-ware. Organizations love the idea of being "data-driven" but hate the discipline of actually using data. So you build 50 dashboards. Maybe 5 get used. The rest? Digital dust collectors costing $200K/year in maintenance.

## The principle

VALUE OVER VANITY: If nobody uses it, it's worth nothing. Think of your data assets like retail inventory. Data sources are raw materials sitting on warehouse shelves. BI solutions are products on retail shelves that need to be "purchased" (used). ML models are fancy items gathering dust in the back room.

The counteracting principle: Implement usage metrics as your north star. Track who uses what, how often, and for what actual decisions. Create a "dashboard about your dashboards" and watch the behavior. Apply the retailer lens: Would anyone "buy" this if it was on a shelf?

Kill or promote: If nobody touched it in 90 days, either retire it or heavily advertise it. Measure adoption, not just deployment. "We built 50 dashboards" means nothing without "42 are used weekly by 200+ people."

Do "BI on yourself" - use your own analytics to shape and guide your strategy. This prevents the sugar high crash. Track usage religiously. Retire ruthlessly. That's how you stop wasting money on stuff nobody wants.

## The steps

1. Turn On Usage Tracking Today: Every dashboard, every model needs analytics. Who uses it? When? For how long? If your tool has this built-in, enable it. If not, add it.
2. Run the 90-Day Purge: Pull usage data. Anything with <5 weekly active users gets flagged. Meet with stakeholders: "Still need this?" If no, retire it.
3. Make Usage a Team Metric: Track "% of solutions with 10+ weekly active users." Review monthly. Celebrate when it goes up. This forces the team to build valuable stuff.

## In practice

A Fortune 500 company spent two years building dashboards. The VP of Analytics proudly presented to the board: "We now have 52 dashboards covering every business function!" The board clapped. Executives nodded.

Then someone asked the uncomfortable question: "How many people actually use them?"

Silence.

They ran a usage audit. Reality hit hard: 12 dashboards had monthly active users. 40 dashboards? Zero opens in six months. Zero. They were maintaining 40 dashboards that literally nobody used. Annual cost: $200K in infrastructure, maintenance, and support tickets for dashboards gathering digital dust.

They made the hard call: retired all 40 in one brutal purge. Consolidated the remaining 12 into 5 core products. Watched engagement triple because people could actually find what they needed.

That $200K? Redirected to building solutions people actually wanted. Usage became the only metric that mattered. No more sugar highs. Just value.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
