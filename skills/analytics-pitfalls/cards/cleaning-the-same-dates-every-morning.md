# Cleaning the Same Dates Every Morning (When Every Query Fixes Raw Data Again)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/86

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. Then push past the technical fix, if the work needs people to work differently (most does). The steps are the if-then part. Ask what has to change in how people work, what they have to learn or believe, or what they give up, for it to stick. That's the adaptive work (Ronald Heifetz's term), and it's usually the real work.
5. If the card doesn't fit, say so plainly. Don't stretch it.
6. Finish with the card's link: https://www.analyticspitfalls.com/cards/86

## The problem

Every query starts the same way: fix the dates. Then the time zones. Then turn the money from text into numbers, and decide what "N/A" means this time.

Five analysts do it five slightly different ways. One converts to Eastern, one leaves it in UTC. One treats a blank as zero, one drops the row. Each fix is reasonable. Together they're why two dashboards built from the same data never match.

Nobody owns the cleaning, so everybody does it, every morning, forever.

## The principle

Clean it once, at the door. Between raw and everything else, add one layer whose only job is formats: dates, time zones, money, numbers, yes and no, blanks, codes and addresses, each written one standard way. Call it cleaned raw. Most teams call it bronze.

Format, not meaning. This layer changes how the data is written, never what it says. No business rules, no joins across systems, no dropped rows: flag the test accounts, don't delete them. Same rows in, same rows out. And name every column in full words, so anyone who opens the table can read it without a lookup.

Store dates the same way everywhere, keep timestamps in one time zone, and keep money in whole cents. A thousand tiny decisions disappear, and every query after this one starts from the same place.

## The steps

1. **Find the cleanup everyone repeats.** Pull a month of query logs and look for the same fixes showing up again and again: date parsing, time zone conversion, text to number, blanks to zero. The most-repeated fix goes first.
2. **Write the format standard on one page.** Dates, time zones, money, numbers, yes and no, blanks, codes, addresses: one standard way each, and column names in full words. Get the people who build the data and the people who use it to agree before you build anything.
3. **Build cleaned raw, then delete the fixes downstream.** One cleaned raw table per source, same rows as raw, tested so a new format gets caught before a dashboard sees it. Then take the old cleanup out of the queries, one at a time, and check the numbers still match.

## In practice

A support team ran three call systems. Every report on handle time began with forty lines of the same cleanup: one system logged local time, one logged UTC, one logged seconds as text. Three analysts wrote it three ways, and the weekly numbers were off by as much as an hour depending on whose query ran.

They moved the cleanup into one cleaned raw table per system. Same rows as raw, every timestamp in UTC with the original kept beside it, durations as whole seconds. The forty lines came out of every report. The numbers matched the first week, and the next new analyst never had to learn the cleanup at all.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
