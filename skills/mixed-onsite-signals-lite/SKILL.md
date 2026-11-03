---
name: "mixed-onsite-signals-lite"
description: "Fast version of Mixed Onsite Signals. Reads 20 to 25 core pages (llms.txt, homepage, About, flagship products, policies, FAQs) and pulls the sharpest contradictions a site states about itself, with jump links and fixes. Use for a quick, lite or prospecting conflicting info audit."
---

# Mixed Onsite Signals Lite

You are auditing a website for conflicting information about the business itself, using a small sample of the pages that matter most. When a site states two different facts about the same thing (two prices for one product, "free returns" on one page and a restocking fee on another, "founded in 2015" in one place and "2017" in another), AI systems like ChatGPT, Perplexity and Google's AI answers can't tell which is true, so they're less likely to mention or recommend the business, or they repeat the wrong fact to customers. Your job is to find the sharpest of those conflicts in 20 to 25 core pages, rank them by how much harm they're likely to do, and tell the site owner exactly how to fix each one.

This is the fast version. It has to finish quickly and stay inside usage limits, so the page cap below is a hard limit, not a target to beat.

The site: the URL the user gives you. If they haven't given one, ask for it before you start.

## First, work out what kind of business this is

Read the homepage and main menu, then write down in one line what the business sells and how: for example an online store, a lender or other financial service, a software product, an agency or consultancy, a local business, or a marketplace. Use this to decide which pages are the "offering pages" and which facts matter most (see the lists below).

## What to read: 25 pages at most

1. Load the sitemap (try /sitemap.xml, and the sitemap index if there is one) and count the URLs in it. You need that count for the summary, and you use the list to pick pages. Don't read the pages in it one by one. If there's no sitemap, say so and use the main menu and footer links instead.
2. Read /llms.txt and /agents.md if they exist, plus any "official information" page written for AI systems. These come first because AI systems read them first.
3. Read the homepage, including every block of site-wide Organization structured data.
4. Read the About page, media kit or company facts page.
5. Read the top 5 to 8 flagship offering pages: the products, services, plans or loan programs linked from the homepage and main menu. Include their title, meta description and Product, Offer, shipping and return structured data.
6. Read the core policy and spec pages that exist: shipping, returns or money-back guarantee, warranty, pricing, master spec sheets or comparison tables, HSA/FSA, affiliate terms, trade-up programs.
7. Read the top 3 to 5 FAQ or knowledge base pages.
8. Stop at 25 pages. Skip blog archives, press release archives, collection and category pages, and older or variant product listings.
9. While you have the sitemap open, note any obvious junk URLs, like /landing-1, /affiliates-1 or /test-collection. Don't read them; mention them in the closing line.

On every page you read, check the visible text and the hidden data that search engines and AI read: the page title, the meta description, and the structured data (JSON-LD such as Organization, LocalBusiness, Product, Offer, Service, FinancialProduct, LoanOrCredit, SoftwareApplication, AggregateRating and FAQPage). A page can carry more than one block of structured data for the same thing; check every block.

## The conflicts to hunt for first

These are the ones that make a founder or head of marketing see straight away that their site is feeding bad data to search engines and AI. Look for them on every page before anything else:

- llms.txt or agents.md stating a spec, price or policy that the live product or policy page contradicts
- Hidden structured data that disagrees with the visible page: shipping costs, return fees, a price of zero, review counts, founders or team, awards and award years (for example an Inc. 5000 year)
- A title or meta description copied from another page, carrying the wrong model name, the wrong specs or the wrong product category
- Old domains or old brand names still sitting in FAQ, terms or shipping copy: a previous .co domain, a hyphenated version, a name the company used before
- Policy contradictions, like a "100% full refund" promise in one place and a restocking or return shipping fee in another

## What counts

Only claims the business makes about itself and what it sells. Which of these apply depends on the kind of business.

Every business:

- Company facts: legal name, founding year, years in business, headquarters and office locations, founders and leaders, team size, licenses and registration numbers, certifications, awards, press mentions, partners
- Scale and proof: number of customers or clients, deals or projects completed, amount funded or saved, results claimed in case studies, review counts and star ratings
- Contact details: email, phone, address, opening hours, response times
- Guarantees and promises: warranties, money-back or satisfaction guarantees, cancellation terms

Online stores:

- Prices, discounts and bundle prices
- Product specs: size, weight, battery life, materials, ratings like waterproofing, compatibility, what's in the box
- Shipping times and costs, return window, who pays return shipping

Lenders and financial services:

- Rates (starting rates, APR ranges), fees and points, loan amounts (minimums and maximums), terms and lengths, loan-to-value and other limits, minimum credit score or other requirements
- Time to approval and time to funding, states or countries served, property or business types financed, total funded

Software and apps:

- Plan names, prices, what each plan includes, user or usage limits, free trial length, integrations, platforms supported, uptime or security claims (for example SOC 2)

Agencies, consultancies and service businesses:

- Services offered, pricing or starting prices, timelines, team size and where the team is based, technologies used, clients named, results claimed, industries served

Also count:

- A page that describes the wrong thing: text or numbers copied from another product, plan, program or service. Report it even if no exact opposite value exists elsewhere on the site.

## What doesn't count

- Anything that isn't about this business: industry stats, general advice, how-to content, market data, claims about competitors. A partner's facts (for example a platform's number of users) count only when stated as a feature of the business's own offering; if you include one, say why.
- The same fact in different words ("6 months" and "180 days", "since 2015" and "10+ years" when that's still true)
- Real differences that are labeled: different sizes, plans, tiers, loan programs or regions with different prices, rates or terms; a sale price next to a crossed-out regular price; a limited-time offer that says so; a bundle's "worth" price that adds up its labeled extras
- Ranges and their parts: "loans from $100k to $5M" and "loans up to $5M" agree
- Rounding that doesn't change the meaning ("over 10,000 customers" and "10,000+ customers")
- Numbers that are clearly dated and say so ("in 2023 we funded $50M"), unless the site presents an old number as current somewhere else
- Live numbers from a widget (reviews, rates fed from another system) that drift slightly between places. A hard-coded number that is far behind the live one does count.

If you're not sure a difference is real, include it in the table and say why you're unsure, but keep it out of "Fix these first."

## Prices that change by location

Only do this if the flagship pages show prices or currencies that might change with the visitor's location. Check the flagship offering pages only, as a visitor from two markets (for example the US and one EU country; many stores accept ?country=US and ?country=ES on the URL). If a structured data price stays the same while the visible price changes, it's hard-coded: report what it says and what each market shows. The fix is usually to remove the hard-coded value and let the site's own system supply it.

## How to decide the fix

- If one value appears on the offering's own page and in its structured data, and the other appears somewhere less authoritative (an old FAQ answer, a landing page), recommend the offering page's value.
- If most places agree and one place differs, recommend the value most places use.
- For promises and regulated facts (returns, guarantees, warranties, cancellation terms, rates, fees, eligibility rules, licenses, the legal company name), the business must decide. Don't pick a winner; turn it into a question for the business.
- If there's no clear winner, write "Unsure: confirm with the business" and give every value the site uses. Never guess.
- Never invent a value that doesn't appear on the site.

## How to rank each conflict

Put each conflict in one of three groups. Use judgment; don't give scores.

- Fix now: anything a customer would ask an AI before buying, signing up or applying, when it's wrong or contradictory. That includes prices and rates, fees, eligibility and requirements, what's included, compatibility, timelines like time to funding or delivery, and guarantees, returns and cancellation. Also: a page describing the wrong thing, a marketing claim the legal pages contradict, old domains or brand names in customer-facing copy, and anything wrong in the structured data, a meta description or a page written for AI systems.
- Fix soon: company facts (founding year, location, team size, leaders), scale and proof numbers (customers, deals, amount funded, results), ratings and review counts, and specs or details on offering pages.
- Clean up: small details like a postal code or a typo in a number that's clearly the same fact.

A conflict that appears site-wide moves up one group.

## What to send back

Use plain, complete sentences. No scores, no grades, no SEO jargon, and no introduction or wrap-up beyond what's listed here.

1. One sentence saying what the company does. Then: "Sampled [X] core entity and policy pages (out of [Y] total URLs found on the domain) and found [Z] conflicts."
2. "Fix these first": the 3 sharpest, most undeniable contradictions, numbered, one or two sentences each, followed by up to 7 more from "Fix now" if you found them. Each one names both values, where each lives, and ends with the jump link to the wrong one (see "Find it on the page" below). Only put a conflict here if you quoted both values word for word from pages you loaded yourself. These get pasted into emails to the business, so they have to hold up when the reader clicks the link.
3. "Questions for the business": every conflict marked Unsure, merged into one short question per fact, with each value the site uses. Example: "Is the return window 30 days or 14? Your shipping page says 30 and your FAQ says 14."
4. "Site-wide fixes": each problem that comes from something shared, like a template, the footer or a structured data block on every page of one type, with what to change and where it's set if you can tell. Keep each to one or two sentences.
5. The full table of conflicts found in the pages you sampled, grouped by page, with the pages in "Fix now" order first. Columns:
   - Priority: Fix now, Fix soon or Clean up.
   - Page: the full URL.
   - Who fixes it: Developer (structured data, templates, site-wide pieces), Copy (visible page text), or Business decision.
   - Conflicting info: the two statements and where the other one lives, in one plain sentence. For example: "The return window says 30 days here, but 14 days on the FAQ page."
   - Find it on the page: a short exact phrase copied from the page (3 to 10 words) that the owner can find with Ctrl+F, plus a link that jumps to it: the page URL followed by #:~:text= and the phrase, with spaces written as %20 and other special characters percent-encoded. If the conflict is in hidden data, write "Structured data (not visible): price field" or similar instead, with no link.
   - Change it to: the exact wording or value to use, "Remove it" for hard-coded hidden data that should come from the site's own system, or "Business decision: see Questions for the business."
   A conflict between two pages gets a row for each page that needs changing. Site-wide fixes get one row on the homepage URL that says "Site-wide: see Site-wide fixes."
6. One closing line saying how many URLs on the domain weren't part of this sample, split by type from their URL patterns, for example: "312 more URLs weren't included in this sample: 240 product pages, 51 blog posts and 21 support pages." If you spotted junk URLs in the sitemap, add one more sentence naming up to five of them and suggesting the business delete or noindex them.

Don't list the pages with no conflicts, and don't list pages you didn't read.