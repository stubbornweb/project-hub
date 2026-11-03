# KissMyApps Product Engine and Product Hub: research

Date of research: 2026-11-03.

How to read this file:

- "Their claim" means a fact that comes from kissmyapps.com. The company says it. We have not checked it.
- "Reported" means a fact from a press article, a profile or a search summary. The source is named.
- Their own pages are saved as plain text in `research/sources/kissmyapps-product-engine.md` and `research/sources/kissmyapps-product-hub.md`.

## 1. Summary

- Product Engine is KissMyApps' own AI system for launching and scaling consumer apps. The company says it has four parts: analytics, marketing, app development help and payments (their claim).
- Product Hub is a page on their site. It shows apps that succeeded on their platform. It also explains their 11-step launch framework and lists open jobs. It is a showcase and a hiring page. It is not a status board.
- Their claimed success rate is 80% on launches (their claim). Their claimed app count is 20+ (their claim). Their pages do not show prices or a client list.
- Their pages do not show budgets, deadlines or sales targets for each idea. Earlier press numbers for this (a $50,000 test budget, three months, a $100,000 target) are from dev.ua, not from their site (reported).
- The main lesson for this system: their 11-step path ends in a results review and a scale-or-close decision. Our pipeline ends at `publish`. We have no step after launch.

## 2. What they are, who they are for, and how they earn

### Product Engine

- What it is: "our own full-cycle AI product development platform that helps launch and scale B2C businesses" (their claim, Product Engine page). B2C means business to consumer: apps sold to ordinary people.
- Four modules (their claim, Product Engine page):
  - Kiss & Tell: analytics. Their pages say it uses AI agents that scan 1,000+ competitor apps every day and suggest niches.
  - Kiss My Ads: marketing automation for app store ads, search optimisation and paid campaigns.
  - Ready2Kiss: ready-made code libraries for payments, onboarding and analytics, plus AI testing and localisation for 15+ languages.
  - Pay2Kiss: a payment gateway that routes card and other payments, handles subscriptions and retries.
- Who it is for: their pages name two groups.
  - Consumer app businesses that need launch and scale help (Product Engine page).
  - Experts with traction who want to build a business with the company as co-founder (Co-founding page, see section 2.3).
- Price: none. Their menu and footer have no pricing page. Product Engine is not sold to outside companies on any page we read.

### Product Hub

- What it is: a page with three parts. It shows apps that succeeded on their platform (AI Remodel, Printer App, Chi and Botan). It explains the 11-step framework. It lists open roles.
- Who it is for: visitors and job candidates. The page does not offer a service to buy.
- Price: none.

### How the business makes money

Their pages do not say how each app earns money. They do not name ads, subscriptions or sales as the main source. Their pages say:

- They are a "platform company" that can "launch and scale businesses through in-house, co-founding, and M&A strategies" (their claim, About page). M&A means buying companies.
- They are "9-figure status, fully bootstrapped" (their claim, About page). Bootstrapped means no outside investment. "9-figure" means a number with at least nine digits, in a currency the page does not name. They do not give a number.
- Co-founded businesses: the founder runs the new business full time as CEO. The founder gets a monthly pay from the project budget. The company keeps the majority share (their claim, Co-founding page).

Reported: Forbes Ukraine, July 2025, quotes the CEO on the company's model (reported). The Recursive, July 2026, says products come from three sources: in-house builds, co-founded apps and bought apps (reported).

### 2.3 The co-founding offer

This is a second product for outside experts, not for software buyers.

- Who it is for: "experts with traction" (their claim). The page asks for a head or C-level person with team management experience and a plan for up to 3 years. It asks for a financial model and a pitch deck.
- What they give: infrastructure, a marketing ecosystem (24/7 campaign tools, market data, frameworks), back office (finance, legal, payments, hiring) and tech (AI testing, localisation, an SDK, and the Product Engine modules) (their claim, Co-founding page).
- Their steps (their claim, Co-founding page): application, pre-screening, CEO screening, meeting with the company CEO, culture check, business case, CFO screening, and a handshake.
- Their claim: 30+ products have succeeded on the platform (Co-founding page). This does not match the 20+ figure on other pages (see section 6).

## 3. Stages, steps and terms, compared with this system

Their 11-step framework (Product Hub page, their claim). Our parts are named as in `docs/sources/2026-11-03-vision.md`.

| # | Their step (their claim) | Our part today | Gap or match |
| --- | --- | --- | --- |
| 1 | Idea and problem | `idea-grill` writes a verdict (PROCEED, REFINE, PARK, REJECT) | Match |
| 2 | Market and audience analysis | `idea-research` ranks open questions. Kill-questions come first | Match in method. Theirs runs on data (see step 3) |
| 3 | Competitor analysis. Kiss & Tell scans 1,000+ competitor apps daily | `opportunity-scan` is named in `WORKSPACE.md` but is not in the public skills repo (vision doc, next steps) | Gap: no scanner in the public repo |
| 4 | Product decision and unique value | `idea-grill` verdict | Match |
| 5 | Financial model and monetisation | None in `idea-grill` or `project-brief` (no budget or unit-economics step found in the skill text) | Gap |
| 6 | Strategic goals and alignment | `project-brief` (`PROJECT-DESCRIPTION.md`, scope and out-of-scope) | Partial match. No goal numbers |
| 7 | Product development | `prototype-engine new`, `scaffold`, `build`, `review` | Match |
| 8 | Marketing strategy and channels | None | Gap |
| 9 | Roadmap and milestones | The Hub status board is planned, not built | Gap until the Hub exists |
| 10 | MVP launch (their Ready2Kiss kit, MVP in 1 month for Chi, their claim) | `prototype-engine publish` | Match in form. No time target |
| 11 | Results analysis and scale or close | None. The Hub's analytics choice is open (vision doc, open questions) | Gap |

Terms and parts that have no direct match:

- Client work: their co-founding track is the nearest match to our client projects. Their model is a partner who runs the business, not a client who buys work. Our `client-intake` and client repos do not have that form.
- Hub: their Product Hub is a public showcase. Our Hub is planned as a private status board for one owner.

## 4. What is the same, what is different, and what this system does not have yet

### Same

- Both run a path from idea to launch, with checks at each stage. Their checks use a numbered list. Ours use verdict words.
- Both stop weak ideas early. Their claim is that most products fail because each launch starts from zero, and their framework is built to stop that (their claim, Engine page).
- Both reuse a launch kit. Their Ready2Kiss gives payments and onboarding code. Ours has `prototype-engine` patterns and `extract-pattern`.
- Both use gates. Their site says "clear gates, clear metrics" (their claim, Product Hub page). Our gates are verdict words, and a failed gate ends the idea. Their site does not name the metrics.

### Different

- They make consumer apps for their own business and for co-founded businesses. Our system serves client work and one developer's daily tasks (vision doc).
- Their site shows no client portal, no chat inbox, no credential vault and no MCP server. Our system has all four (vision doc, capabilities 4, 5, 6, 7). Their pages cover marketing and payments instead.
- They claim a large data base: 120m+ or 130m+ users, and 120m+ user sessions used for retention analysis (their claim, Engine and Hub pages). Our system has no user data yet.
- They run a team with marketing, legal and finance roles. The open roles on their Engine and career pages show this (their claim). Our system is for one developer.

### This system does not have yet

- A money step. Their step 5 covers the financial model. Our `idea-grill` and `project-brief` do not ask for one.
- A marketing step. Their step 8 covers channels. We have none.
- A results review after launch. Their step 11 ends in a scale or close decision. Our pipeline ends at `publish`.
- A recorded list of closed ideas and the reason for each close. Their closure story is press-only (reported, see section 5).
- Numeric limits per idea (a budget cap, a deadline and a target). Their site shows none. Press reports them (reported, dev.ua).
- Revenue and usage fields in the status file that the Hub reads (vision doc, open questions).
- A `promote` command from prototype to client repo (vision doc, "How the parts connect").

## 5. Evidence of success

All numbers below come from kissmyapps.com unless marked otherwise.

| Topic | Figure | Where it appears | Tag |
| --- | --- | --- | --- |
| Launch success rate | 80% (also "80%+" and "up to 80%") | Engine, Hub, About pages | Their claim |
| Apps that succeeded on the platform | 20+ | Engine, Hub, About pages | Their claim. Co-founding page says 30+ (conflict) |
| Apps in active scale backed by the company | 20+ | Hub page | Their claim |
| Users worldwide | 130m+ (Engine, About). 120m+ (Hub) | Three pages | Their claim. Two figures differ |
| Team size | 300+ "Kiss'ers" (employees) | About page | Their claim. Press says 151-500 (CASES) and 201-500 (LinkedIn) |
| Growth | "YoY Growth X3" (about 3 times per year) | About page | Their claim |
| Scale-up in the early utilities period | "x10 YoY scale-up" | About page | Their claim |
| Financial status | "9-figure status, fully bootstrapped" | About page | Their claim. No revenue number |
| Age and history | Idea in 2022. Became a platform company at the start of 2025. Began with a merger and acquisition of Tonti Laguna Mobile | About page | Their claim |
| AI Remodel | "#1 AI-tool for Interior Design". Launched twice. Became #1 in 3 months. 3.5m+ users. 5m room redesigns. App Store rating 4.55 | Product page and Hub | Their claim |
| Printer App | 10M+ downloads. 10,000+ supported printer models. App Store rating 4.6 | Product page and Hub | Their claim |
| Chi | From idea to MVP in 1 month. App Store rating 4.7 | Product page and Hub | Their claim |
| Botan | 1M+ installs | Hub page | Their claim |
| Product SDK | Libraries "tested across 30+ products" | Engine page | Their claim |
| Charity | 30M+ UAH direct donations. 150M+ UAH raised by their initiatives | About page | Their claim. Not business evidence |

Other figures from outside sources:

- Early history: "merger and acquisition" and the "utilities" period are on their About page (their claim). Press and profile sources agree the company was founded in 2022 (reported, LinkedIn and CASES).
- Founded in 2022 (reported, LinkedIn: https://www.linkedin.com/company/kiss-my-apps and CASES: https://cases.media/en/kiss-my-apps/).
- Users: 100 million (reported, Forbes, CEO interview). A search summary gives 130 million (reported, Crunchbase summary, not loaded).
- Downloads: more than 130 million (reported, The Recursive, July 2026).
- Products closed: five products closed after missing a target (reported, dev.ua, citing the CEO).
- Budget rule: about $50,000 test budget per idea, three months, and a $100,000 sales target (reported, dev.ua). Not on their site.
- Launch in 24 hours (reported, dev.ua). Their site says 1 month for Chi (their claim). See section 6.
- Award: named among winners of the Fast Company 2026 Best Workplaces for Innovators list, AI and automation category (reported, CB Insights profile, Sep 8, 2026). The Fast Company page was not checked.
- Press: Forbes Ukraine (July 2025), The Recursive (July 2026), dev.ua (2026), Liga.net (June 2026, via CB Insights). TechUkraine (2025) did not load.
- Client counts: none found on their site or in press.
- Client reviews: none found.
- Employee reviews: two on Glassdoor, per a search summary (Glassdoor page did not load).
- Prices: none on any page read.

## 6. Corrections to the first version of this file

The first version used press and search results. Their own pages now change these points:

- The earlier claim that "KissMyApps sets hard numbers for each idea" is not supported by their site. The $50,000, three-month and $100,000 figures come from dev.ua (reported). Their site says "clear gates, clear metrics" but gives no numbers.
- The earlier claim that "Launch in 24 hours is possible" (dev.ua) conflicts with their site. Their site says "From idea to MVP in 1 month" for Chi (their claim).
- Product Hub: the earlier note said a search summary described it as showing apps that grow on the platform. The page shows apps that succeeded on the platform, the 11-step framework and open jobs (their claim).
- Users: the earlier note gave 100m (Forbes) and 130m (search summary). Their own pages say 130m+ (Engine and About) and 120m+ (Hub). Use the company figure as "their claim".
- Team: the earlier note gave 151-500 and 201-500. Their About page says 300+. Use the range from press and "300+" as their claim.
- Success rate: the earlier note gave "80+%" from a search summary. Their pages say 80%, 80%+ and "up to 80%" (their claim).
- Concept-to-profit in "2-4 weeks" (search summary): not found on their pages. Remove unless a later source confirms it.
- Who it is for: the earlier note said "not confirmed". Their pages now name consumer app businesses and experts with traction (co-founding).
- Business model: the earlier note said "builds apps for its own revenue". Their pages also describe co-founded businesses, where the company keeps the majority share (their claim).
- The earlier note said the company's pages mention no clients, client portals or chat inboxes. This is still true for the pages read. The earlier company home page did not load and is now read.

## 7. Name risk

Names compared:

- "Prototype Engine" (owner) and "Product Engine" (KissMyApps). Both end in "Engine" and both describe a build or launch stage. The first words, "Prototype" and "Product", sound alike at the start.
- "Project Hub" (owner) and "Product Hub" (KissMyApps). The words differ by one letter. They sound almost the same when spoken. KissMyApps uses "Product Hub" as the name of a public page on its site (their claim, page title).
- The owner's vision doc says the final name is not decided (`docs/sources/2026-11-03-vision.md`, open questions).

Search results (from the first version):

- No software product named "Project Hub" in the results. Results are roundups of client-portal tools, so the term is generic.
- No product named exactly "Prototype Engine" in the results. Similar tools include `proto-cli` on npm (https://www.npmjs.com/package/proto-cli), `create-proto` (https://github.com/sherizan/proto) and the GOV.UK Prototype Kit (https://github.com/alphagov/govuk-prototype-kit).
- No trademark record was found for either name in search. The USPTO trademark database was not searched.

Plain statement: KissMyApps uses "Engine" and "Hub" in the names of its own pages and modules. Their names are close to the owner's names. A trademark search is needed before any public launch. This is not legal advice.

## 8. Ideas worth considering

These are options for the owner to weigh. None is decided.

- Add a money step to the pipeline, as their step 5 does. It could go in `idea-grill` or `project-brief`.
- Add a marketing step, as their step 8 does.
- Add a results review after launch, as their step 11 does. A dated check, such as a three-month review, could feed the Hub status file.
- Add numeric limits to `IDEA-DECISION.md`: a spend cap, a deadline and a target. Their site gives none, but press reports them (reported, dev.ua). Consider the owner's own numbers, not theirs.
- Keep a list of closed ideas and the reason for each close. Their press story says they close products that miss a target (reported).
- Look at their test habit: they run AI smoke tests and testing for localisation (their Ready2Kiss module). This could be a later idea for the prototype stage, not a first step.
- Consider the co-founding terms as one reference if the owner ever offers a partner role. Their terms are: full-time CEO, monthly pay from the project budget, and the company keeps the majority share (their claim).
- Run a trademark search for "Prototype Engine" and "Project Hub" before any public use or naming decision.
- Keep the owner's client work and the consumer-app model apart in the docs. They solve different problems.

## 9. Sources checked

Their own site (read 2026-11-03 with a browser, page text saved in `research/sources/`):

- https://www.kissmyapps.com/product-engine: read. Saved as `research/sources/kissmyapps-product-engine.md`.
- https://www.kissmyapps.com/product-hub: read. Saved as `research/sources/kissmyapps-product-hub.md`.
- https://www.kissmyapps.com/about: read (about, timeline, team, growth, culture, charity). Not saved as a source file.
- https://www.kissmyapps.com/co-founding: read (co-founding offer, terms, hiring steps). Not saved as a source file.
- https://www.kissmyapps.com/product/ai-remodel: read (product page, stats). Not saved.
- https://www.kissmyapps.com/product/chi: read (product page, stats). Not saved.
- https://www.kissmyapps.com/product/printer-app: read (product page, stats). Not saved.
- https://www.kissmyapps.com/career: read (hiring steps, open-roles page). Not saved.
- Not opened: /culture (its content is on the About page), /blog, /newsroom, and the individual job pages. Pricing: no pricing page is linked from the site menu or footer.

Press and profile sources (from the first version, not re-checked in this run):

- https://forbes.ua/innovations/vid-startapu-do-kompanii-platformi-urokami-zrostannya-kiss-my-apps-cherez-zaluchennya-talantiv-ta-avtomatizatsiyu-protsesiv-dilitsya-ii-ceo-dmitro-lola-03072025-31019: loaded (CEO interview, July 3, 2025).
- https://www.therecursive.com/building-a-startup-during-war-without-vc-and-without-replacing-people-with-ai/: loaded (interview, paywalled after intro).
- https://dev.ua/en/news/kiss-my-apps-1788762387: loaded.
- https://www.linkedin.com/company/kiss-my-apps: loaded.
- https://www.cbinsights.com/company/kiss-my-apps: loaded.
- https://cases.media/en/kiss-my-apps/: loaded.
- Liga.net (June 2026): listed in the first version via CB Insights. Not checked in this run.

Could not read (in the first version and in this run):

- https://www.crunchbase.com/organization/kiss-my-apps: HTTP 403. Search summary only.
- https://techukraine.org/2025/07/07/crisis-proof-tech-the-9-figure-playbook-of-ukraines-kiss-my-apps/: HTTP 403. Search summary only.
- https://www.glassdoor.com/Overview/Working-at-Kiss-My-Apps-EI_IE10640335.11,23.htm: HTTP 403. Search summary only.
- Clutch: searched, no profile found, not fetched.

Local owner files read (first version):

- `docs/sources/2026-11-03-vision.md` and `docs/sources/2026-11-03-handoff.md` (this repo).
- `/home/yevhenii/www/prototype-engine/README.md`.
- `/home/yevhenii/www/skills/skills/product/` skills: `idea-grill`, `idea-research`, `project-brief`, `client-intake`. The grill skill has no numeric limits and uses PROCEED, REFINE, PARK and REJECT.
- `/home/yevhenii/opportunities/`: one folder listed (`validated-problem-marketplace`), not read.
