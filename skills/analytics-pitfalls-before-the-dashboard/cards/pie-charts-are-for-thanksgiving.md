# Pie Charts Are for Thanksgiving (When Circles Make Everything Harder)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/56

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/56

## The problem

Dashboard review. Someone shows market share by product. It's a pie chart. You stare at it. Which slice is bigger—the 23% green slice or the 21% blue slice? Can't tell. You have to read the labels. Now try comparing to last quarter's pie chart. Which slices grew? Shrank? Impossible to tell without doing mental math. Pie charts force humans to compare angles and areas—our brains are terrible at both. It's like asking someone to build a car by eyeballing measurements instead of using a ruler. A bar chart would've shown the comparison instantly. But pie charts "look nice" so we keep using them. And making every analysis harder.

## The principle

Bar charts are almost always better than pie charts. Period. Our brains compare lengths easily but struggle with angles and areas. When you need to show parts of a whole, use a stacked bar chart or just a table of numbers. The ONLY time pie charts work: showing exactly 2-3 categories where precision doesn't matter ("roughly half are X, half are Y"). Otherwise? Skip them. Think manufacturing: you wouldn't use a broken measurement tool just because it looks pretty. Same with visualization—use the tool that makes comparison easy, not pretty.

## The steps

1. **Audit Your Pie Chart Usage**

Find every pie chart in your reporting:
- Count the slices (if >3, it's automatically bad)
- Ask: Are users comparing values? (if yes, bar chart is better)
- Ask: Does precision matter? (if yes, table or bar chart)

Rule: If the pie has labels with numbers, you've admitted the pie itself doesn't communicate—just show the numbers.

Test: Cover the labels. Can you still rank the slices? If no, the chart failed.
2. **Replace with Better Alternatives**

For parts-of-a-whole:
- Stacked horizontal bar (easier to compare than pie)
- Simple table (if <6 categories)
- Regular bar chart (if comparing sizes)

For time series: Line chart or bar chart (never pie)
For ranking: Horizontal bar chart, sorted

Only keep pies for: True binary (50/50, yes/no) where rough proportion is the only message.
3. **Before/After Test**

For any pie chart replacement:
- Time 5 users answering a key question with the pie
- Time same 5 users with new chart
- Track: time + accuracy

Typically: Bar charts are 3-5x faster and more accurate.

Bonus: Train your team. Show the research. Make "pie charts are for Thanksgiving" a cultural meme. When someone proposes a pie, the team says "is it Thanksgiving?"

## In practice

A retail analytics team loved pie charts. Market share dashboard: 7-slice pie chart by region. Leadership meeting: "Which region grew most?" Team scrambles to calculate. Takes 3 minutes. Meeting derailed. They rebuilt it: horizontal bar chart, regions sorted by size, previous quarter shown as light gray bars behind. Leadership glanced at it: "West region jumped 4 points, South dropped 2." Took 5 seconds. No math required. The team ran an experiment: showed 20 analysts the same data in pie vs bar chart. Asked: "Which product has highest share?" Bar chart: average 2 seconds, 100% accuracy. Pie chart: average 12 seconds, 73% accuracy. Pie charts made analysis 6x slower and error-prone. They banned pie charts org-wide except for true binary splits (yes/no, pass/fail). Clarity improved immediately.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
