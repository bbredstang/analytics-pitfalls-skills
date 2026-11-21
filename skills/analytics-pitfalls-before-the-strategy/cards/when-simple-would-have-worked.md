# When Simple Would Have Worked (But We Got Fancy Instead)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/12

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/12

## The problem

Analytics team builds a "Customer Health Score" with 23 variables, weighted by a machine learning model nobody understands. It spits out numbers from 0-100. Sales teams ignore it because they don't trust a black box. Meanwhile, the real signal was obvious: customers who don't log in for 30 days churn. That's it. One simple rule would've worked better than the fancy model. But we overcomplicated it because smart people like to build smart things. Complexity feels impressive. Simple feels too easy. But complexity kills adoption. If people don't understand it, they won't use it. It's like building a Swiss watch when all you needed was a sundial.

## The principle

Start simple. Solve the problem with the simplest solution first. If "customers who don't log in for 30 days churn," just track login recency. You don't need a PhD-level model. Add complexity only when simplicity fails. Think manufacturing: you don't need a robotic arm when a lever works. The magic happens when solutions are so intuitive that people adopt them immediately because they just make sense. Less wizardry, more clarity. Stupidly simple always wins over impressively complex.

## The steps

1. Start with the Simplest Solution: Before building anything complex, ask: "What's the dumbest simple version that could work?" Try that first. Add complexity only when simplicity fails.
2. Measure Adoption, Not Accuracy: A 75% accurate model people trust beats a 90% accurate black box nobody uses. Optimize for understanding and adoption first.
3. Kill Complexity Creep: Every time someone suggests adding a feature, ask: "Does this make it easier to use or harder?" If harder, say no. Protect simplicity ruthlessly.

## In practice

A bank built a credit risk model with 47 features and a neural network. Took 9 months, cost $800K, and predicted default risk with 82% accuracy. Compliance team couldn't explain it to regulators. Got shelved. Intern built a simple model: 3 variables (income, debt-to-income ratio, payment history), logistic regression. Took 2 weeks. Accuracy: 79%. Close enough. But here's the kicker—compliance could explain it in 30 seconds, it was approved immediately, and it went into production. Prevented $15M in bad loans in year one. The fancy model sat unused. The simple model shipped. Sometimes 79% accuracy that people trust beats 82% accuracy nobody understands.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
