# The 32% Click-Through Problem (When Email Becomes Spam)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/51

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/51

## The problem

You send out the weekly sales report to 500 people. You track opens: 68% don't even click the link. Of those who do, half spend <10 seconds looking at it. You're burning hours building and sending reports that 85% of recipients ignore. It's spam. Except you're the one sending it. Think manufacturing: imagine running a production line where 85% of finished products go straight into the trash. That's your email distribution strategy. Meanwhile, users who actually NEED the report can't find it because it's buried in their inbox with 47 other "analytics updates" nobody reads.

## The principle

Stop mass-emailing reports. Build a self-service portal and only notify people when THEIR data changes. Track click-through rates like eCommerce tracks cart abandonment. If <50% of recipients click a report, stop sending it. Let users subscribe to what they want, not what you think they need. The magic happens when you flip from push (email spam) to pull (portal with alerts). Think retail: Amazon doesn't email you every product—you search for what you need. Same with analytics.

## The steps

1. **Measure the Waste**

For every report email you send:
- Track open rate
- Track click-through rate (opened AND clicked the report)
- Track time-on-report (<10 seconds = ignored)

Calculate: % of recipients who actually USE the report.

If <50%, it's spam. Add up hours spent on these reports. That's wasted capacity.
2. **Build Self-Service + Alerts**

Create a portal where users:
- Browse/search for reports (self-service)
- Subscribe to specific reports (opt-in, not mass email)
- Get alerts ONLY when their data changes (not weekly blasts)

Example: "Sales in your region dropped 15% this week" = useful alert.
"Here's the weekly sales report" to 500 people = spam.

Test with one high-traffic report. Move it to portal-only. Track adoption.
3. **Kill Low-Performing Emails**

Review every email distribution:
- <50% click-through? Stop sending it. Move to portal.
- <30%? It's spam. Delete the distribution list.

Track:
- Email vs Portal usage
- Click-through % by report
- Time saved (hours not spent emailing)

Goal: 80%+ of analytics accessed via portal, <20% via email (only critical alerts).

## In practice

A major bank's BI team had 47 active email distribution lists sending reports to 2,300 people weekly. Click-through rate: 32%. That means 68% of emails were noise. They built an analytics portal and shifted to optional subscriptions. Users opted into alerts for THEIR data only. Email volume dropped 73%. Click-through rate jumped to 78% (only engaged users subscribed). Support tickets dropped because users went to the portal first. The 47 distribution lists? Down to 8 (for truly critical daily alerts). Email vs portal became a key metric: if email click-through <50%, move it to portal. Spam eliminated.

## Inspired by

A major bank's analytics portal usage data (2016). Email click-through rates revealed 68% of report emails were ignored—pure waste.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
