---
name: analytics-pitfalls-breach-we-didnt-see-coming
description: "\"The Breach We Didn't See Coming\" (Until It Was Too Late): a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# The Breach We Didn't See Coming (Until It Was Too Late)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/15

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. If the card doesn't fit, say so plainly. Don't stretch it.
5. Finish with the card's link: https://www.analyticspitfalls.com/cards/15

## The problem

Your data warehouse has customer PII—names, emails, addresses, SSNs. Access controls? "We trust our people." Encryption? "It slows things down." Monitoring? "We'll get to it later." Then one day: "Um, we found our customer data on a hacker forum. We've been breached." Scramble mode. Lawsuits. Fines. Headlines. Trust destroyed. Turns out an intern had full database access, their laptop got stolen, and the thieves had everything. Or a contractor exfiltrated data before leaving. Or someone misconfigured an S3 bucket and it was public for 6 months. Security isn't optional—it's foundational. One breach can kill a company. Yet teams constantly deprioritize it because "nothing has happened yet." Until it does.

## The principle

Implement defense in depth: encryption at rest and in transit, role-based access controls (principle of least privilege), monitoring and auditing, regular security reviews. Assume breach will happen—have a response plan. Think manufacturing: you don't skip safety protocols because "we haven't had an accident yet." You prevent accidents by being rigorous. The magic happens when security becomes automatic, not an afterthought. Less "we'll fix it later," more "we build it right the first time." That's how you protect your business and your customers.

## The steps

1. Audit Access This Week: Pull a report of who has access to what data. Anyone with access they don't need? Revoke it. Implement least privilege - people see only what their job requires.
2. Encrypt Everything: Data at rest, data in transit - encrypt it all. If you're storing PII unencrypted, fix that today. It's not optional.
3. Run Quarterly Security Drills: Simulate a breach. Test your response plan. Can you identify it? Contain it? Notify customers? Improve your plan based on what you learn.

## In practice

A healthcare analytics startup stored patient data in unsecured S3 buckets—no encryption, public read access. "We'll lock it down after launch," they said. Someone found it. Downloaded 2 million patient records. Posted on the dark web. Company faced $10M in HIPAA fines, 15 lawsuits, and 3 years rebuilding trust. Nearly went bankrupt. They rebuilt from scratch: encrypted everything, role-based access, quarterly security audits, incident response drills. Five years later, they're profitable and compliant. But that breach almost killed them. Another company learned from that disaster—implemented security from day one, zero breaches in 8 years, customers trust them completely. One team learned the hard way. The other learned from them. Don't be the cautionary tale.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
