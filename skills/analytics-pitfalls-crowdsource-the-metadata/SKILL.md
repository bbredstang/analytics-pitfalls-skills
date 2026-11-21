---
name: analytics-pitfalls-crowdsource-the-metadata
description: "\"Crowdsource the Metadata\" (Stop Being the Bottleneck): a principle card from Analytics Pitfalls & Principles, by Brian Cariveau. Use when a plan, request, dashboard, metric or AI project needs it."
license: CC-BY-4.0
---

# Crowdsource the Metadata (Stop Being the Bottleneck)

A principle card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/50

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work could use this principle.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. If the card doesn't fit, say so plainly. Don't stretch it.
5. Finish with the card's link: https://www.analyticspitfalls.com/cards/50

## The problem

Your team maintains a "data catalog." Except it's always wrong. The data engineer who built Table_X left 2 years ago and nobody knows what field_47b means. You have 500 tables and 3 people trying to document them. It's 18 months out of date. Users don't trust it. So they ask you directly, 50 times a week: "What's this field?" You're a human dictionary. Waste. And you can't scale—if documentation requires YOU, you'll never keep up with 500 tables growing to 5,000.

## The principle

Let users document what they know. Wikipedia works because millions contribute, not because one team writes everything. Same with your data. Crowdsource metadata: what tables mean, which fields matter, data quality issues, example queries. Users who USE the data write the docs. Your job? Curate, not create. Set up a system where anyone can add descriptions, tag tables, rate quality, leave examples. The magic happens when 100 users each document 5 tables instead of 3 people trying to document 500.

## The steps

1. **Enable User Contributions**

Add to your data catalog:
- 'Add description' button (any user can contribute)
- Star ratings for data quality
- Comment threads for clarification
- 'Example queries' section
- Tags/labels

Make it stupidly easy to contribute. Think Wikipedia, not a 47-field form.

Test with 5 power users: 'Document your favorite 3 tables.' If it takes >5 minutes per table, simplify.
2. **Gamify Contributions**

Create incentives:
- Leaderboard: most contributions this month
- Badges: 'Data Documentor', '10-Table Club'
- Recognition: shout-outs in team meetings
- Make it visible: 'Last edited by Sarah' stamps

Don't require perfection. Accept 'good enough' contributions. You can curate later.

Goal: 50% of users contribute at least one piece of metadata in 90 days.
3. **Curate, Don't Create**

Your team's new role:
- Review user contributions weekly
- Fix obviously wrong info
- Merge duplicate entries
- Promote great examples to 'featured'
- Fill gaps where no one contributes

Track: % of tables with user-contributed metadata. Target: 70%+ within 6 months.

If a table has zero contributions after 90 days, either nobody uses it (delete it) or you document it yourself.

## In practice

A financial services data team had 847 tables with 14% documented (120 tables). Metadata quality was so bad users bypassed the catalog entirely. They tried hiring more documenters—still couldn't keep up. Pivoted: built a Wiki-style data catalog where ANY user could add descriptions, tags, quality ratings, example SQL. Gamified it: leaderboard for most contributions. Within 6 months: 673 tables documented (79%). Users trusted it because it was written by users who actually used the data. Data team shifted from writing docs to moderating and curating. Governance through crowdsourcing. Questions dropped 68% because users found answers in the catalog.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
