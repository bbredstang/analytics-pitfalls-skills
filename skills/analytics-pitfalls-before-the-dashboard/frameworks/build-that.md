# Build That!

A framework from Analytics Pitfalls & Principles, by Brian Cariveau.
https://www.analyticspitfalls.com/frameworks/build-that

## How to use this framework

Use it as a lens when someone's analytics or AI work touches what it describes.

1. Say which framework you are using and what it asks, in its one-line definition below.
2. Hold their work up to it: where it already fits, and where it does not. Be specific to their situation.
3. If one of the cards below names their problem more exactly, use that card as it says.
4. Finish with the framework's link: https://www.analyticspitfalls.com/frameworks/build-that

> Build That! means validating ideas with a mockup people can react to before writing requirements — the picture is the spec, not a document nobody can quite picture.

## The failure mode this replaces

A team wants to build a new data product. The instinct is to jump straight to the data — which tables, which joins, which pipeline. If requirements get written at all, they read like legal text: "the system shall display aggregated metrics with drill-down capability." Six months later, the team demos exactly what the document specified. The response is some version of "this isn't really what we needed" — because nobody could actually see it until it was built. They approved words on a page, not a solution to their problem.


## The picture is the requirement

Build a mockup before a single query gets written — even a fake one, even one that took twenty minutes in a GenAI mockup tool. Show it to the actual person who would use it. There are three possible reactions, and only one of them is a green light. "That would be so helpful" means build it. "Maybe" or "I guess so" means iterate on the picture, not the code. "I don't think that answers my question" means start over, because you just saved yourself from building the wrong thing at full cost.

This isn't a designer's ritual bolted onto engineering. It's a cheaper, faster way to find out you're wrong. In the era of GenAI mockup tools, a rough interface takes hours, not weeks — there's no excuse left for skipping straight to the data layer and hoping the requirements document was specific enough.


## Storyboard before you build, too

The same instinct applies one level up, before a single chart gets built for an executive presentation: what's the story, not just the data? A dashboard built by opening a BI tool and dragging fields answers no question in particular. A dashboard built from a storyboard — hook, tension, solution, proof, close, sketched on paper before touching a tool — answers exactly one question, on purpose, and the chart selection follows from the narrative instead of the other way around.


## What this looks like Monday morning

Make the mockup non-negotiable for the next request that lands on your desk. It doesn't need to be polished — Figma, a slide, even a paper sketch beats a requirements doc, because a doc asks people to imagine and a mockup asks them to react. Show it to one real user before a line of code gets written. If they don't light up, you just avoided building the wrong thing at full price.


## Cards that go with it

- **Build the Picture First: Why Mockups Beat Requirements Documents** (`../cards/build-the-picture-first.md`), https://www.analyticspitfalls.com/cards/43
- **Story First, Data Second (Storyboard Before You Build)** (`../cards/story-first-data-second.md`), https://www.analyticspitfalls.com/cards/58

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
