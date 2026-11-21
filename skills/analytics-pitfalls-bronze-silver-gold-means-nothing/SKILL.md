---
name: analytics-pitfalls-bronze-silver-gold-means-nothing
description: "\"Bronze, Silver, Gold Means Nothing\": a pitfall card from Analytics Pitfalls & Principles. Use when a plan, request, dashboard, metric or AI project might be falling into it."
license: CC-BY-4.0
---

# Bronze, Silver, Gold Means Nothing (When Layer Names Don't Help)

A pitfall card from Analytics Pitfalls & Principles, drawn from *The Auction Block* by Brian Cariveau (https://www.analyticspitfalls.com/book).
https://www.analyticspitfalls.com/cards/61

## How to use this card

Use it when what someone is working on, or something they heard at work, looks like the problem below: a plan, a roadmap, a request, a dashboard, a metric, an AI project.

1. Name the card by its title and say in a sentence why it fits. Say the work looks like this pitfall; never tell someone they have it.
2. Give the principle in the card's own words. Don't rewrite it.
3. Take the steps one at a time against their actual situation: what is already done, what isn't, and which to do first. If you need a fact to do that, ask one question, not five.
4. If the card doesn't fit, say so plainly. Don't stretch it.
5. Finish with the card's link: https://www.analyticspitfalls.com/cards/61

## The problem

Your data lake has three layers: Bronze (raw data), Silver (cleaned data), Gold (business-ready data). Sounds sophisticated. Then new analyst joins: "Where's customer data?" Answer: "Check Gold layer." They search. Find 14 tables with "customer" in the name. Which one is right? No idea. They ask 3 people, get 3 different answers. Turns out the "right" customer table is actually in Silver because Gold was never finished. Bronze/Silver/Gold tells you nothing about what's inside. It's like Home Depot organizing by "Bronze aisle," "Silver aisle," "Gold aisle" instead of "Paint," "Tools," "Lumber." Users need to understand what data IS, not what processing tier it's in. Metal names are architecture porn—they make engineers feel organized but leave users lost.

## The principle

Name layers by what they contain, not processing stage. Use names that self-document: Raw (exactly as source systems sent it), Curated_SystemName (cleaned, usable, still system-specific), Integrated_TopicName (cross-system, business-ready). Examples: Raw_Salesforce, Curated_Claims, Integrated_Customer. Every name tells you what's inside. The magic happens when a new analyst can guess where data lives without asking anyone. Think retail: you find paint in the Paint section, tools in Tools, lumber in Lumber. Not in Bronze/Silver/Gold sections. Same with data—name by content, not by processing tier.

## The steps

1. **Audit Your Current Naming**

List all your data layer/zone names:
- What are they called?
- Can a new user guess what's in each layer from the name?

Test: Ask 5 analysts: "Where would you look for customer data?"

If they can't answer without documentation, your names failed.

Common bad patterns:
- Bronze/Silver/Gold (processing stage, not content)
- Stage1/Stage2/Stage3 (meaningless)
- Raw/Cleaned/Final (still doesn't say what's inside)
2. **Rename Using Content-Based Pattern**

Adopt naming convention:
- **Raw_SystemName**: Data exactly as source sent it (Raw_Salesforce, Raw_SAP)
- **Curated_Domain**: Cleaned, usable, system-specific (Curated_Claims, Curated_Calls)
- **Integrated_Topic**: Cross-system, business-ready (Integrated_Customer, Integrated_Product)

Every name answers: "What's in here?"

Create migration plan: Start with most-used tables, rename gradually.

Update all docs, queries, dashboards to use new names.
3. **Self-Documenting Standards**

Create naming standards guide:
- Layer prefix: Raw/Curated/Integrated
- Domain or system name
- Optional: granularity (Daily, Summary, etc.)

Example: Integrated_Customer_Daily vs Integrated_Customer_Summary

Test with new hires: Can they find data without help?

Goal: 80%+ of "where's X data?" questions answered by naming alone.

Bonus: Every new table must follow naming standard or gets rejected in code review.

## In practice

A financial services firm had Bronze/Silver/Gold lake architecture. Beautiful in PowerPoint. Nightmare in practice. New data scientists spent first 2 weeks just learning "which layer has what." Onboarding took 6 weeks because nobody could find data. They renamed everything: Bronze → Raw_SourceSystemName (Raw_Salesforce, Raw_Mainframe, etc.), Silver → Curated_Domain (Curated_Loans, Curated_Customers), Gold → Integrated_BusinessArea (Integrated_Lending, Integrated_Risk). Every name self-documented. New analyst question: "Where's loan data?" Answer obvious: Integrated_Lending. Onboarding dropped from 6 weeks to 1 week. Support tickets about "where's X data" dropped 71%. Bonus: Documentation became less critical because names explained themselves. The architecture didn't change—just the names. But user experience transformed overnight.

---

© 2026 Brian Cariveau, Analytics Pitfalls & Principles. Free to share and adapt under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/): keep this credit, "Brian Cariveau, Analytics Pitfalls & Principles (https://www.analyticspitfalls.com)", and say if you changed it.
The names Analytics Pitfalls & Principles, The Auction Block and The Second Factory are not part of the license. Don't use them for your own version, or to suggest it comes from us.
