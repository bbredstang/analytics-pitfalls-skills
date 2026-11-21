---
name: analytics-pitfalls-walk-the-catwalk
description: "\"Walk the Catwalk\" (Go See the Work, Don't Just Read Reports): a principle card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project needs it."
license: CC-BY-4.0
---

# Walk the Catwalk (Go See the Work, Don't Just Read Reports)

A principle card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/65

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work could use this principle.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/65

## The problem

You're a data leader. You get status reports: "Pipeline is running fine," "Dashboards deployed successfully," "Users are happy." Everything looks good on paper. Then you randomly check a dashboard in production—it takes 45 seconds to load. You ask a business user how they use your platform—they pull out an Excel spreadsheet. "Your portal is too slow, so I just export and work in Excel." You had no idea. The reports said everything was fine because people reported what you wanted to hear, not reality. It's like a manufacturing exec who never walks the factory floor—they never see the jammed machine, the pile of defects, the unsafe workaround. Leaders who don't inspect the work in production are managing fantasy, not reality.

## The principle

Walk the catwalk. Manufacturing term: executives regularly walk the production floor (catwalk), watching work happen, talking to operators, spotting problems. Apply to data: randomly open your dashboards as if you're a user. Try searching for data in your catalog. Sit with an analyst and watch them work. Ask business users to show you how they use your solutions. The magic happens when you see reality, not filtered reports. You'll discover: Dashboards are slow. Naming is confusing. Workarounds everywhere. Users frustrated. None of this shows up in status reports. Weekly catwalk walks reveal more truth than monthly status meetings. Go see, go do—don't just read about it.

## The steps

1. **Schedule Weekly Catwalk Walks**

Block 2 hours weekly: "Catwalk Friday" (or whatever day).

Plan:
- Week 1: Use a random dashboard as if you're an end user
- Week 2: Try searching data catalog for common terms
- Week 3: Sit with an analyst, watch them work for 30 min
- Week 4: Ask a business user to show how they use your platform

Rotate through different areas monthly.

Key rule: Do NOT tell people you're coming. You want to see reality, not a demo.
2. **Document What You Find**

During catwalk walk, take notes:
- What's broken?
- What's slow?
- What's confusing?
- What workarounds do people use?
- What frustrates users?

Don't judge. Don't blame. Just observe and document.

After each walk: Pick top 2-3 issues. Bring to team meeting: "Here's what I found. How do we fix it?"

Goal: Surface problems that status reports miss.
3. **Make Catwalk Culture, Not Just Leadership**

Expand beyond leadership:
- Data engineers: Use the dashboards you built
- Analysts: Try data catalog like a new hire would
- BI developers: Watch business users use your reports

Monthly team catwalk: Everyone spends 1 hour using the platform as a customer.

Share findings in team meeting. Fix top issues.

Goal: Everyone sees reality regularly, not just hears filtered reports.

Bonus: Customer-facing teams appreciate when you ask "show me how you really use this." Builds trust and uncovers truth.

## In practice

A major bank's VP inherited a large data org. Status reports: green across the board. "Everything is running smoothly." He didn't believe it. Instituted "Catwalk Fridays": Every Friday, 2 hours, he randomly picked a dashboard and used it as if he were an end user. Week 1: Tried sales dashboard. Took 3 minutes to load. Filters didn't work. He couldn't find the metric he needed. Week 2: Tried data catalog. Searched for "customer data." Got 47 results, no idea which was right. Week 3: Sat with an analyst. Watched them spend 40 minutes joining 5 tables manually because "the integrated table is wrong." Every week: new problems discovered. He brought them to team meetings: "I walked the catwalk Friday, found this issue, let's fix it." Team realized: status reports were fantasy. Actual user experience was broken. Six months of catwalk walks: dashboard load times dropped 75%, catalog search improved dramatically, analysts working 30% faster. The work got better because leadership SAW the work, not just heard about it.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
