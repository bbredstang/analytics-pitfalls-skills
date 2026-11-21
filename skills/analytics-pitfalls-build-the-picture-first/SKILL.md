---
name: analytics-pitfalls-build-the-picture-first
description: "\"Build the Picture First\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# Build the Picture First: Why Mockups Beat Requirements Documents

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/43

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/43

## What it sounds like at work

"Send me the requirements doc first."

## The problem

Your team wants to build an AI solution. Or a new dashboard. Or a data product.

So they do what teams always do: Jump straight to the data.

"What tables do we need?"
"Where does this data live?"
"How do we join these sources?"

If requirements get written at all, they look like this:

"The user shall be able to filter by date range, product category, and region. The system shall display aggregated metrics with drill-down capability. Performance shall be sub-2-second response time."

Verbose. IT-centric. Not particularly useful.

Six months later, you build exactly what the requirements specified. You demo it.

The response? "Yeah... this isn't really what we needed."

Because nobody could see it. They couldn't picture it. They approved words on a page, not a solution to their problem.

You built what was asked for, not what was needed.

## The principle

Pictures are more powerful than words. Mockups are better specs than requirements documents.

Build the picture first. Make it real—even if it's fake. Get someone excited about the mockup before you write a single line of code or touch a single table.

When someone looks at your mockup and says "THAT—that is it. If you build that, it will be so helpful"—THEN you start identifying what data you need.

Not before.

The mockup is the requirement. The mockup is the spec. The mockup is what you build to.

In the age of GenAI tools, there's no excuse. You can iterate on UI mockups in minutes, not months.

## The steps

1. **Make Mockups Non-Negotiable**

New rule for your team: No building until someone gets excited about a mockup.

Use whatever tool works:
- Figma (professional UX)
- Balsamiq (quick wireframes)
- PowerPoint (yes, really—it works)
- GenAI mockup tools (fastest option now)
- Even paper sketches (better than nothing)

The mockup should show:
- What the user sees (the actual interface)
- What questions it answers (the value)
- Who uses it (the personas)

Show it to the actual user. If they say "that would be so helpful," you have a green light. If they say "maybe," iterate. If they're lukewarm, start over.

Don't write requirements. Don't jump to data sourcing. Build the picture first.
2. **Develop Mockup Skills in Your Team**

This isn't just for designers. Your analysts, data engineers, and product folks should be able to quickly mock up solutions.

Invest in:
- Design thinking training (helps people think about user needs)
- Basic UX principles (clarity, simplicity, user flow)
- Mockup tools (train the team on whatever tool you choose)
- GenAI prompt engineering (for AI-powered mockup tools)

Create a UI template library:
- Standard dashboard layouts
- Common component patterns
- Reusable design elements
- Brand guidelines

The goal: Anyone on the team can build a mockup in 30-60 minutes, not 30-60 days.

Bonus: These skills make your team more valuable. An analyst who can build AND design? That's a unicorn.
3. **Use the Mockup as the Spec**

Once someone gets excited about the mockup, THAT becomes your requirements document.

Not a 20-page Word doc. The picture.

Development process:
1. Pin the mockup in your project channel
2. Reference it in every standup ("Are we building what's in the picture?")
3. Compare your work-in-progress to the mockup daily
4. When questions arise, go back to the mockup
5. If the mockup doesn't answer the question, update the mockup first, then update the code

The mockup is the source of truth. Build exactly what's in the picture. No more. No less.

If someone wants something different, they update the mockup and get it re-approved. No verbal change requests. No email additions.

Picture first. Build second. Ship what was promised.

## In practice

One of my BI teams made this a non-negotiable rule:

No building until we had a mockup that someone got excited about.

The process:
1. Build a mockup in our UI template (not code, just visuals)
2. Identify the personas who would use it
3. Identify what questions it would answer
4. Show it to the actual person who would use it

If they looked at it and said "That would be so helpful"—we built it.

If they said "Maybe" or "I guess so"—we iterated on the mockup.

If they said "I don't think that answers my question"—we started over.

We didn't write a single query until someone was excited about the picture.

The result? Our team started shipping solutions people actually used. Not solutions that matched requirements documents.

We stopped building dashboard graveyards. We stopped building AI pilots that never made it to production.

Because we built what people could see, not what they could read.

---

Fast forward to today. GenAI mockup tools changed the game again.

One of our product team members was working on a new data governance tool. In the past, this would have been weeks of requirements gathering, documentation, review cycles.

Instead, two product folks used a GenAI mockup tool. Within hours, they had a UI. They iterated with a few team members. Got feedback. Adjusted in real-time.

They showed it to the broader team.

The response? "Oh my gosh—that would be awesome. Build that."

Not "I think that could work" or "Let me review the requirements."

But genuine excitement. Because they could SEE it.

The picture became the spec. The team knew exactly what to build. No ambiguity. No interpretation. No rework.

Many people on that old BI team became unicorns at this skill—analysts who could build solutions AND quickly mock them up. They studied design thinking principles. They learned UX basics.

And they shipped solutions that people loved, not solutions that checked boxes.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
