# The Telephone Game

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/39

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/39

## The problem

Adding layers of people between idea and execution. Business person → Business Analyst → Project Manager → Data Developer → UI Developer → back to business. Six people. Six handoffs. Each handoff loses fidelity. Each translation adds cost. Each person added increases project time exponentially. A simple "show me last quarter's sales" becomes a 6-week project through the assembly line. Or worse: you're still stuck in 2007 where Business → BA → Sourcing → ETL → Modeler → BI Developer means a 2-month cycle for a dashboard. The manufacturing analogy is perfect: imagine Toyota running a production line where each station speaks a different language and has to translate work orders. You'd never ship a car. That's your BI process.

## The principle

Flatten the org. Get the person with the idea as close to the tools as possible. Give business analysts the same BI toolkit as developers. Train them. Trust them. Stop the assembly line of handoffs. The magic happens when someone who understands the business can build their own answer in 2 hours instead of waiting 6 weeks for IT. This is the self-serve wave: everyone on the same platform, fewer handoffs, faster insights. Think manufacturing: cross-functional cells where one team owns the whole widget, not 6 teams passing pieces. Reduce handoffs from 6 to 1 (or zero). Time-to-answer drops 90%. Fidelity stays perfect because no translation happens.

## The steps

1. **Map Your Handoffs**

For your most common request types, draw the flow:
- Who touches it?
- How many handoffs?
- Time at each step?

Example: "New dashboard request" might be:
Business → BA (3 days) → IT intake (5 days) → Data eng (10 days) → BI dev (14 days) → QA (7 days) → Deploy (3 days) = 42 days, 6 handoffs

If >3 handoffs, you have a telephone game problem.
2. **Enable Self-Service**

Give business analysts/power users direct access to tools:
- Pre-built data models (so they don't need data eng)
- BI platform training (Tableau, Power BI, etc.)
- SQL basics (so they can query)
- Templates and best practices

Start with 5 power users. Train them. Let them build.

Goal: Business users build 50%+ of routine reports themselves.
3. **Shift IT to Enablers**

IT's new role:
- Build/maintain data models and pipelines
- Govern data quality
- Create templates and training
- Review complex work
- Build what requires engineering

NOT: Build every single report.

Measure:
- % of reports built by business users (target: 60%+)
- Average handoffs per request (target: <2)
- Cycle time (target: 80% reduction)

Bonus: IT stops being a bottleneck and starts being strategic.

## In practice

A major bank had the classic 2007 problem: Business request → BA documents → Sourcing pulls data → ETL team loads it → Data modeler builds semantic layer → BI dev builds report → back to business. Average cycle time: 47 days. They shifted to self-serve: gave BAs access to Tableau + pre-built data models. Trained them on SQL basics. First month: BAs panicked. "We're not developers!" By month 3: BAs building 70% of reports themselves. IT focused on data quality + models. Handoffs dropped from 5 to 1 (just "approve the data model"). Cycle time: 47 days → 7 days (85% reduction). Fidelity improved because BAs who knew the business built exactly what was needed. IT stopped being a bottleneck and became enablers. The telephone game ended when you gave everyone the same phone.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
