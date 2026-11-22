# Garbage In, Powerhouse Out? (Nope.)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/6

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/6

## The problem

You spent $2M building a state-of-the-art ML platform. Hired a team of PhDs. Bought the fanciest tools. Launch day comes, predictions are wildly off. Turns out your customer data has 40% duplicates, purchase dates are wrong half the time, and nobody has cleaned the source systems in 5 years. Garbage in, garbage out. Except now it's expensive garbage with a PhD babysitting it. It's like building a Ferrari and filling it with contaminated fuel—doesn't matter how good the engine is if the inputs are trash. Data quality is the foundation. Skip it and everything built on top is a house of cards. Yet teams constantly underinvest here because it's not sexy. Cleaning data doesn't win awards. But it's what separates powerhouses from pretenders.

## The principle

Clean, simple data beats sophisticated models on dirty data every single time. Treat data quality like you'd treat raw materials in manufacturing—inspect, validate, reject defects before they enter the line. Automate quality checks at ingestion. Monitor data health like you monitor system uptime. Make data quality everyone's job, not just the data engineer's. The magic happens when you slow down just enough to build a foundation of trustworthy data, then speed up knowing every decision is built on solid ground. Less firefighting, more building. That's the path to powerhouse status.

## The steps

1. Implement Quality Gates at Ingestion: Before data enters your warehouse, validate it. Check for nulls, duplicates, out-of-range values. Reject bad data at the door.
2. Build Automated Monitors: Set up alerts for data quality issues - duplicate records, missing values, unexpected changes in volume. Monitor data health like you monitor system uptime.
3. Make Quality Everyone's Job: Add data quality metrics to your team dashboard. Track: % of clean records, # of quality issues caught. Review monthly. Celebrate improvements.

## In practice

A healthcare company built a $5M patient risk prediction model. Accuracy in testing: 94%. Accuracy in production: 61%. Why? Source data was a disaster—duplicate patient records (some patients had 7 IDs), wrong birthdates, medications listed for the wrong people. They stopped, rebuilt the foundation. Spent 4 months cleaning: deduped patients, validated dates, built quality monitors. Relaunched the model—same algorithm, clean data. Accuracy: 91% in production. Model actually worked. Saved $12M in unnecessary procedures in year one. The lesson? The model was never the problem. The foundation was. Clean your data first, build fancy stuff second. That's the only order that works.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
