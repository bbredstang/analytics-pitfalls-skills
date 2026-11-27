# The Blender (When Systems Get Mixed Before Anyone Knows What Each One Says)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/87

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. If you don't know their situation yet (what they're working on, and where: their kind of company and team), ask one short question first, unless the conversation already says. Then fit everything below to it, not to a generic company.
2. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
3. Give the principle in the card's own words. Don't rewrite it.
4. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
5. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
6. If the card doesn't fit, say so plainly. Don't stretch it.
7. Finish with the card's link: https://www.analyticspitfalls.com/cards/87

## The problem

The team has three call systems, so they build one table for all of them. Straight from raw, all in one go. It looks great on the architecture slide.

Then the east call center's numbers look wrong. Is it the east system, the blending, or the definition? Nobody can tell, because the only place the east system exists is blended into everything else. There's nothing to check it against.

And when the west system gets replaced next year, the whole blended table has to be rebuilt.

## The principle

See each system alone before you put them together. Give every source system its own layer, one system at a time, in its domain: one call system, one website, one portal, one claims system. Call it system-specific. Most teams call it silver.

Here each system is told straight, in its own terms. Its business rules written down with an owner. Its codes turned into words. Its customers and products joined to the master data with standard keys. Its names in full words, so a person or an agent can open the table and read it.

Then build the system-agnostic layer from those. When a number looks wrong, you can go back one step and see which system said what. When a system is replaced, you replace one table, not the whole blend.

## The steps

1. **List every source system in one domain.** Pick the domain people argue about most. Write down every system that feeds it, and check whether each one can be seen on its own today.
2. **Build one system-specific table per system.** Its own rules, written down with an owner. Codes in words. A stated grain. Keys to the master data. Names in full words. Start with the system that breaks most.
3. **Rebuild the blend from them.** Build system-agnostic from the system-specific tables, never straight from raw, and keep the source system on every row so anyone can trace a number back.

## In practice

A company ran four websites and two customer portals, all blended into one traffic table. When portal logins dropped 30% in a week, the team spent nine days working out whether the drop was real. It turned out one portal had changed how it logged sessions, and the blend had hidden it.

They split the blend into one system-specific table per site and portal, each with its own definition of a session, written down. The next time a site changed its logging, the analyst saw it the same morning, in one table, and fixed the mapping before anyone outside the team noticed.

## Inspired by

The essay "People and Systems Over Solutions" in The Auction Block, and Brian Cariveau’s talks on data layers.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
