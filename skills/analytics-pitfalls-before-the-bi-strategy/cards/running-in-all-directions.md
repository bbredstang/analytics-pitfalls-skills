# Running in All Directions (The Tool Circus Nobody Asked For)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/32

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/32

## What it sounds like at work

"Let’s buy a tool for that."

## The problem

Letting everyone pick their own tools and approaches, creating 3, 5, or 10 different ways to do the same thing. Technology teams love new shiny tools. Getting technologists excited about the latest thing is easy. But with too many choices, everyone grabs something different and runs with it, convinced they're innovating. The result? Chaos. Fragmentation. Three teams implementing three different data catalog vendors. Some building custom, others buying commercial. Same vendor used five different ways. Everyone thinks they're maturing the organization. Nobody realizes they're killing it.

## The principle

SHARED DIRECTION OVER INDIVIDUAL FREEDOM: Progress requires everyone running down the SAME side of the road together. When everyone picks different paths, you see small pockets of value team by team, but as a whole it diminishes your organization's fitness.

Create a clear mountaintop: Make it crystal clear where you're going as ONE team. Paint the picture. Show the destination. Then audit for duplication—find where you're doing the same thing multiple ways.

Standardize strategically: Pick ONE way for ONE thing. Doesn't mean one tool for everything—it means one approach per problem. Stop new fragmentation—any new initiative must answer "how does this align with our shared direction?" Retire competing approaches gradually. 

Communicate the WHY before making people climb. If you asked "where is your organization doing the same thing 3 different ways?" and have multiple examples, you're fragmented, not fit. Fix that first.

## The steps

1. Draw the Mountaintop: One page. Where are we going as ONE team? What's the future state? Make it crystal clear. Get leadership buy-in.
2. Audit for Duplication: Find everywhere you're doing the same thing 3+ ways. Data catalogs? BI tools? Quality frameworks? List them all. Pick ONE per function.
3. Sunset Competing Approaches: Give teams 90 days to migrate to the chosen approach. Retire the rest. Stop new fragmentation - any new tool must align with mountaintop.

## In practice

A healthcare analytics org had five separate teams. Each team decided—independently—to "solve the data quality problem." Team A built a custom Python framework. Team B bought Collibra. Team C bought Informatica. Team D built their own too, but in Scala. Team E just hired more people to manually check data.

Annual cost of this fragmentation: $2M. Five solutions. Zero coordination. Constant confusion about which system owned quality for which data.

New VP walked in, drew the mountaintop on a whiteboard: "ONE shared data quality framework. Period."

Teams resisted. "But our approach is better!" "But we already spent $400K!" "But our team knows this tool!"

VP was ruthless: "I don't care. Pick one. Sunset the rest. You have 90 days."

They picked Team B's approach (Collibra), killed the other four. Reallocated the $1.6M saved to capabilities that actually moved the needle. Migrated gradually over six months.

Results? Work completed 3x faster because everyone pulled in the same direction. No more "which quality system do we use?" debates. Data quality actually improved because resources were focused, not fragmented.

Fragmentation costs real money and real momentum. One direction. Always.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
