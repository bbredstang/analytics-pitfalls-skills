# The Netflix Principle (Recommend, Don't Force)

A principle card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/53

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work could use this principle.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/53

## The problem

Your data catalog has 2,154 reports. A new analyst joins: "Where do I start?" You have no answer. They're overwhelmed. Or worse: they keep asking YOU for recommendations 50 times. "What report should I use for sales?" You become a human concierge. Doesn't scale. Meanwhile, great reports sit unused because new users don't know they exist. It's like a library with no recommended reading list—just 10,000 books on random shelves. Users need help navigating, not a giant catalog.

## The principle

Build a recommendation engine. Netflix doesn't show you 10,000 movies—it shows you 20 you'll probably like based on what others watched. Same with analytics. Track who uses what. Recommend reports based on: user's department, role, what similar users view, trending/popular reports. Surface the right 5 reports for each user, not a catalog of 2,000. The magic happens when users find great reports without asking you. Think retail: "Customers who viewed this also viewed..." That's how you scale discovery.

## The steps

1. **Track Usage Patterns**

Instrument your analytics portal:
- Who views what reports
- When (time of day, day of week)
- Sequence (report A → report B)
- Duration (time on report)
- User attributes (department, role, location)

Build a usage database. This is your recommendation engine fuel.

Minimum data: user_id, report_id, timestamp, duration.
2. **Build Simple Recommendations**

Start with basic recommendations on portal homepage:

**Personalized:**
- 'Popular in [user's department]'
- 'Your team frequently uses'
- 'Based on your recent views'

**General:**
- 'Trending this week' (most views)
- 'Recently updated'
- 'Highest rated'

**Collaborative Filtering:**
- 'Users like you also viewed' (similar usage patterns)
- 'Frequently viewed together'

Don't need ML—simple rules work. Test with 5 recommendations per user.
3. **Measure Discovery Impact**

Track:
- % of users who click recommendations
- Reports discovered via recommendations vs search
- Time to first useful report (for new users)
- Hidden gem reports that get surfaced

Goal: 40%+ of report discoveries via recommendations (not search/asking).

Iterate based on click-through rates. Promote what works. Kill recommendations nobody clicks.

Bonus: Surface your best reports to more users without building 50 more reports.

## In practice

A financial services analytics team had 1,847 reports with terrible adoption. New hires spent 2 weeks just figuring out which reports to use. The team built "BI for BI"—usage analytics on their analytics. Tracked: who uses what, when, for how long. Built a recommendation engine: "Popular in Sales," "Your team uses these," "Trending this week," "Frequently viewed with this report." Added it to their portal homepage. Time-to-first-useful-report for new hires dropped from 2 weeks to 2 days. Report discovery jumped 310% (users finding reports via recommendations vs search). Bonus: recommendations surfaced hidden gems—great reports that were buried got traffic. Netflix-style discovery without hiring a concierge team.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
