# KissMyApps Product Engine and Product Hub: research

Date of research: 2026-11-03.

Important limit: the company's own Product Engine and Product Hub pages did not load. The site returned HTTP 429 (too many requests) on every try. The facts below come from press articles, the company's LinkedIn and CB Insights profiles, and search summaries. Each fact has its source.

## 1. Summary

The owner's system is partly similar to KissMyApps. Both run a path from idea to launch, with checks at each stage. KissMyApps builds and runs consumer mobile apps for its own income. The owner's system helps one developer run client work, websites and credentials. The main lesson: KissMyApps sets hard numbers for each idea. Its CEO says it uses a test budget of about $50,000, a three-month deadline and a $100,000 sales target (their claim, reported by dev.ua). The owner's gates use pass or fail filters and a verdict word, with no numbers.

## 2. What they are

### Product Engine (KissMyApps)

- What it is: an internal system that the company calls its "product engine". It runs analytics, payments and marketing tools for new apps. Source: https://forbes.ua/innovations/vid-startapu-do-kompanii-platformi-urokami-zrostannya-kiss-my-apps-cherez-zaluchennya-talantiv-ta-avtomatizatsiyu-protsesiv-dilitsya-ii-ceo-dmitro-lola-03072025-31019 (their claim, from a CEO interview, July 3, 2025).
- Parts named in that article (their claim): an app store marketing system (ASO and Apple Search Ads), an "MVP launch library" that adds payments and analytics in hours, an analytics platform that predicts lifetime value with "accuracy above 95%", and AI tools for coding, testing and ad copy. Source: same URL.
- Who it is for: the company's own products. The company builds apps for its own revenue. Source: https://www.therecursive.com/building-a-startup-during-war-without-vc-and-without-replacing-people-with-ai/ (interview, July 29, 2026).
- Price: none found. It is not sold as a service in any source I could read.

### Product Hub (KissMyApps)

- What it is: a section of the company website. A search summary says it shows apps that grow on the platform. Source: https://www.kissmyapps.com/ua/product-hub (did not load; search summary only).
- Who it is for: not confirmed. The page did not load.
- Price: none found.

### Company facts

- Company type: a "platform company" that builds and launches consumer apps. Source: https://www.linkedin.com/company/kiss-my-apps (LinkedIn profile, loaded).
- Model: products come from three sources. The company builds them in house, co-founds them with outside founders, or buys apps. Source: https://www.therecursive.com/building-a-startup-during-war-without-vc-and-without-replacing-people-with-ai/
- Business model for the owner's comparison: none of the loaded pages mention selling software to other companies.

## 3. Stages, steps and terms

| Stage or step | KissMyApps term (source URL) | This system's part | This system's term |
| --- | --- | --- | --- |
| Idea stage | "Niche-selection framework" for choosing products (https://forbes.ua/innovations/vid-startapu-do-kompanii-platformi-urokami-zrostannya-kiss-my-apps-cherez-zaluchennya-talantiv-ta-avtomatizatsiyu-protsesiv-dilitsya-ii-ceo-dmitro-lola-03072025-31019) | `idea-grill`, step 1: write the idea in the owner's own words | `IDEA-DECISION.md`, `opportunities` folder |
| Validation or decision stage | About $50,000 test budget per idea, and a three-month test with a $100,000 sales target. Products that miss it are closed (https://dev.ua/en/news/kiss-my-apps-1788762387, their claim) | `idea-grill` filters and verdict (PROCEED, REFINE, PARK, REJECT). `idea-research` ranks "kill-questions" first | `IDEA-DECISION.md`, `RESEARCH-QUESTIONS.md` |
| Brief or spec | none found | `project-brief` | `PROJECT-DESCRIPTION.md` |
| Prototype | "MVP launch library" that builds an app in hours. Launch "in 24 hours" is possible (https://dev.ua/en/news/kiss-my-apps-1788762387, their claim) | `prototype-engine` commands: `new`, `scaffold`, `build`, `review` | Prototype folder `prototypes/<slug>/` |
| Client or production build | In-house, co-founded or bought apps (https://www.therecursive.com/building-a-startup-during-war-without-vc-and-without-replacing-people-with-ai/) | `client-intake` (`INTAKE.md`, `PROPOSAL.md`). One repo per client project | Client repo. No `promote` command yet (vision doc, "How the parts connect") |
| Delivery or launch | App store marketing system (ASO and Apple Search Ads) (https://forbes.ua/innovations/vid-startapu-do-kompanii-platformi-urokami-zrostannya-kiss-my-apps-cherez-zaluchennya-talantiv-ta-avtomatizatsiyu-protsesiv-dilitsya-ii-ceo-dmitro-lola-03072025-31019) | `prototype-engine publish` | `publish` command. Client handover: none |
| Status or hub view | "Product Hub" (https://www.kissmyapps.com/ua/product-hub, did not load) | Project Hub: status board | "Project Hub" status board |

Notes on the owner's terms (from the owner's own files):
- `idea-grill` writes the verdict into `IDEA-DECISION.md`.
- `prototype-engine` has the commands `new`, `scaffold`, `build`, `review`, `publish` and `extract-pattern` (source: `/home/yevhenii/www/prototype-engine/README.md`).
- The vision doc says the Hub is not built yet. It names the handoffs still missing: brief to prototype, prototype to production, and status files for the Hub (`/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md`).

## 4. Same, different, and missing

### Same

- Both use a stage path from idea to launch.
- Both stop weak ideas early. KissMyApps closes products that miss its target. The owner's verdict can end at REJECT or PARK.
- Both reuse a launch kit. KissMyApps has an "MVP launch library". The owner has `prototype-engine` patterns and `extract-pattern`.
- Both measure results before going on. KissMyApps predicts lifetime value (their claim). The owner's Hub plans analytics on the status board (vision doc, open questions).

### Different

- KissMyApps builds consumer mobile apps for its own revenue. The owner's system serves client work and one developer's daily tasks.
- The loaded KissMyApps pages mention no clients, client portals, credential vaults or chat inboxes. The owner's system has all four (vision doc). The company home page did not load, so this is limited.
- KissMyApps uses numbers for each decision (budget, deadline, sales target). The owner's gates use pass or fail filters and a verdict word.
- KissMyApps has a team of 151 to 500 people (CASES profile, https://cases.media/en/kiss-my-apps/) or 201 to 500 (LinkedIn). The owner's system is for one developer (vision doc).

### This system lacks

- Numeric limits per idea: budget cap, deadline and sales target.
- A dated check after launch. The owner's pipeline ends at `publish`.
- A record of closed ideas and the reason for each close.
- Revenue or usage data in the status file the Hub reads. The vision doc lists this as an open question.
- A `promote` command from prototype to client repo (vision doc, "How the parts connect").

## 5. Evidence of success

Facts that come from kissmyapps.com are marked "their claim". Facts from other sources name the source.

- Founded in 2022. Source: https://www.linkedin.com/company/kiss-my-apps (LinkedIn, loaded). Also https://cases.media/en/kiss-my-apps/ (CASES, loaded).
- Company age on 2026-11-03: about 4 years (from the 2022 founding year).
- Team size: 201 to 500 employees (LinkedIn, loaded: https://www.linkedin.com/company/kiss-my-apps). CASES lists 151 to 500 (https://cases.media/en/kiss-my-apps/). A search summary lists 59 on LinkedIn. The sources disagree. Use the range, not one number.
- Users: 100 million users (https://forbes.ua/innovations/vid-startapu-do-kompanii-platformi-urokami-zrostannya-kiss-my-apps-cherez-zaluchennya-talantiv-ta-avtomatizatsiyu-protsesiv-dilitsya-ii-ceo-dmitro-lola-03072025-31019, CEO interview, their claim). A search summary gives 130 million users (https://www.crunchbase.com/organization/kiss-my-apps, did not load). Sources disagree.
- Downloads: more than 130 million downloads (https://www.therecursive.com/building-a-startup-during-war-without-vc-and-without-replacing-people-with-ai/, reported in an interview).
- Apps or products: about 20 consumer products plus four internal products (The Recursive, same URL). 22 new products in two years, and more than 30 AI-powered apps across seven product verticals (Forbes article, their claim). 27 apps with about 6 million combined monthly users (https://dev.ua/en/news/kiss-my-apps-1788762387, reported). Sources disagree.
- Closed products: five products closed in four and a half years, after missing the target (https://dev.ua/en/news/kiss-my-apps-1788762387, reported by dev.ua from the CEO).
- Growth claim: "at least 3x" year over year (https://cases.media/en/kiss-my-apps/, quoting the company's About page, their claim). The About page did not load.
- Revenue: described as a "9-figure" business. No revenue number is given (https://forbes.ua/innovations/vid-startapu-do-kompanii-platformi-urokami-zrostannya-kiss-my-apps-cherez-zaluchennya-talantiv-ta-avtomatizatsiyu-protsesiv-dilitsya-ii-ceo-dmitro-lola-03072025-31019, their claim).
- Bootstrapped: "Bootstrapped from day one" (https://www.therecursive.com/building-a-startup-during-war-without-vc-and-without-replacing-people-with-ai/, interview).
- Launch success rate: "80+%" and concept-to-profit in "2-4 weeks" (search summary of https://www.crunchbase.com/organization/kiss-my-apps, did not load; their claim).
- Award: named among winners of the Fast Company 2026 Best Workplaces for Innovators list, AI and automation category. Source: https://www.cbinsights.com/company/kiss-my-apps (CB Insights summary, loaded). The date shown is Sep 8, 2026. The Fast Company page itself was not checked.
- Press coverage: Forbes Ukraine (July 2025), The Recursive (July 2026), TechUkraine (2025, did not load), and Liga.net (June 2026, from CB Insights). Sources: URLs in section 8.
- Client counts: none found.
- Client reviews: none found.
- Employee reviews: only two on Glassdoor, per a search summary (https://www.glassdoor.com/Reviews/Kiss-My-Apps-Reviews-E10640335.htm, did not load).
- Clutch profile: none found in search.

## 6. Name risk

Names compared:

- "Prototype Engine" (owner) and "Product Engine" (KissMyApps). Both end in "Engine". Both start with "Prot" or "Product". The sound is close. Both describe a fast build stage.
- "Project Hub" (owner) and "Product Hub" (KissMyApps). The words differ by a few letters. Spoken, they sound close. The owner's vision doc says the final name is not decided (`/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md`, open questions).

Search results:

- No software product named "Project Hub" in the results. Results are roundups of client-portal tools (for example https://productive.io/blog/project-management-software-with-a-client-portal/). The term is generic.
- No product named exactly "Prototype Engine" in the results. Similar tools: `proto-cli` on npm (https://www.npmjs.com/package/proto-cli), `create-proto` (https://github.com/sherizan/proto) and the GOV.UK Prototype Kit (https://github.com/alphagov/govuk-prototype-kit).
- No trademark record was found for either name in search. I could not search the USPTO trademark database. A search there is still needed.

Plain statement: the names are close to KissMyApps' product names. I found no direct conflict in search. A trademark check is still needed before any public launch. This is not legal advice.

## 7. Ideas worth considering

- Consider adding numeric limits to `IDEA-DECISION.md`: a spend cap, a deadline and a target. KissMyApps uses these (their claim).
- Consider a dated check after launch, such as a three-month review, in the Hub status file.
- Consider a log of closed ideas with the reason for each close. KissMyApps reports five closed products (reported).
- Consider revenue and usage fields in the status file the Hub reads. The vision doc lists this as open.
- Consider a trademark search for "Prototype Engine" and "Project Hub" before any public use or naming decision.
- Consider keeping the owner's product purpose separate from KissMyApps. The owner's system serves client work. KissMyApps builds consumer apps.
- Consider reading the Product Engine and Product Hub pages again later. The site was rate limited for the whole session.

## 8. Sources checked

Company pages (kissmyapps.com):
- https://www.kissmyapps.com/product-engine: did not load (HTTP 429, tried 5 times)
- https://www.kissmyapps.com/product-hub: did not load (HTTP 429, tried 3 times)
- https://www.kissmyapps.com/: did not load (HTTP 429, tried 2 times)
- https://www.kissmyapps.com/ua: did not load (HTTP 429)
- https://www.kissmyapps.com/ua/product-hub: did not load (HTTP 429)
- https://www.kissmyapps.com/ua/about: did not load (HTTP 429)
- https://www.kissmyapps.com/co-founding: did not load (HTTP 429, tried 2 times)
- https://www.kissmyapps.tech/: did not load (HTTP 301 redirect to kissmyapps.com, not followed)
- Pricing, FAQ, terms, blog and case study pages on kissmyapps.com: not found and not fetched, because the site returned 429 on all pages.

Independent sources:
- https://www.linkedin.com/company/kiss-my-apps: loaded
- https://www.cbinsights.com/company/kiss-my-apps: loaded
- https://cases.media/en/kiss-my-apps/: loaded
- https://forbes.ua/innovations/vid-startapu-do-kompanii-platformi-urokami-zrostannya-kiss-my-apps-cherez-zaluchennya-talantiv-ta-avtomatizatsiyu-protsesiv-dilitsya-ii-ceo-dmitro-lola-03072025-31019: loaded
- https://dev.ua/en/news/kiss-my-apps-1788762387: loaded
- https://www.therecursive.com/building-a-startup-during-war-without-vc-and-without-replacing-people-with-ai/: loaded (paywalled after intro)
- https://www.crunchbase.com/organization/kiss-my-apps: did not load (HTTP 403). Search summary only.
- https://www.cbinsights.com/company/kiss-my-apps: loaded (listed above)
- https://techukraine.org/2025/07/07/crisis-proof-tech-the-9-figure-playbook-of-ukraines-kiss-my-apps/: did not load (HTTP 403). Search summary only.
- https://www.glassdoor.com/Overview/Working-at-Kiss-My-Apps-EI_IE10640335.11,23.htm: did not load (HTTP 403)
- https://www.glassdoor.com/Reviews/Kiss-My-Apps-Reviews-E10640335.htm: search summary only
- Clutch: searched. No Kiss My Apps profile found. Not fetched.
- Search for trademark and name conflicts: searches only. Results listed in section 6.
- https://www.npmjs.com/package/proto-cli, https://github.com/sherizan/proto, https://github.com/alphagov/govuk-prototype-kit: search results only, not fetched.
- https://productive.io/blog/project-management-software-with-a-client-portal/: search result only, not fetched.

Local files read:
- `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md`: read
- `/home/yevhenii/www/prototype-engine/README.md`: read
- `/home/yevhenii/www/skills/skills/product/idea-grill/SKILL.md`: read
- `/home/yevhenii/www/skills/skills/product/idea-research/SKILL.md`: read
- `/home/yevhenii/www/skills/skills/product/project-brief/SKILL.md`: read
- `/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md`: read
- `/home/yevhenii/opportunities/`: listed only (one folder, `validated-problem-marketplace`). Not read, not changed.
