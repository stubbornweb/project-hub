# The studio

**Date:** 2026-11-04
**From:** [`ideas/solo-product-studio/IDEA-DECISION.md`](https://github.com/stubbornweb/opportunities/blob/main/ideas/solo-product-studio/IDEA-DECISION.md) in the idea workspace (private)

## What it is

The studio is the owner's set of engines, one for each stage, that take an own project or a client project from an idea to a live site under one slug. Each engine keeps the best current practices for its stage, and the Hub shows every project, its stage and what each engine made, in one place.

## Who it is for

The owner: a solo web developer who builds with Claude Code, one project per PhpStorm tab. The owner builds their own products and takes client projects, both new ones and existing ones. There is no client now, and the owner wants the tools ready before the next one.

Clients are the second user. They do not run the studio. They log in to see the progress of their own project.

## The problem it solves

In the owner's words (dictated in Ukrainian, translated):

"I want one general system that works in stages, so I understand where each project is, which stage it is in, what is happening with it, and how to improve and build it: both from zero and projects that are already built, which I take from clients. The system is built on engines, one for each stage, developed separately but with one shared system, so a project can travel from one engine to the next. Each engine holds the best practices I find: articles, videos, books, docs, existing projects, code, ideas and databases like Starter Story, both practices that already work and ones worth testing. Using the best current practices, in step with modern technology, is the most important part. On top of all the engines, the Hub joins them and shows the results each engine produced."

Today the work is scattered. Text is copied by hand from one stage to the next. Good practices stay in videos and bookmarks. Links are lost in the browser, client chats are in several apps, clients take progress on trust, and passwords have no protected home.

## What it does

In build order.

**The engines**

- The owner judges an idea and gets a verdict. At PROCEED, the idea becomes a project with its own project repo, and every part of the studio uses its slug.
- A project starts at the stage where it really is. An existing client site starts at the build stage and keeps one slug and one record.
- The Design Engine designs a project before its prototype.
- The Prototype Engine builds a prototype from the project's brief, with no text copied by hand.
- After launch, a results check records the real results and a decision: grow, change or stop. It also shows which "worth testing" practices helped.
- The owner gives a source (an article, a video, a book, a case or code) and gets practice proposals for one engine. Each approved proposal changes the engine through one pull request.

**The Hub**

The Hub gets these capabilities one at a time. Each one works before the next one starts. The Hub build map decides the order.

- One board shows every idea and project, its stage and its client, and what needs attention next.
- A link library saves links from anywhere and finds them again from a vague memory.
- One button opens a project in the local working folder, in PhpStorm and in Claude Code, without overwriting local work.
- A client logs in and sees the agreed phases, the features, the current work and what is done.
- One inbox holds all chats with a client, starting with Telegram, WhatsApp, email and Facebook. The owner replies from there.
- A protected area keeps project passwords and other secrets. It stays closed until the owner unlocks it, and no AI tool can open it.
- AI tools work with the Hub through an MCP server (a standard way for AI tools to call an app).
- WordCraft, PdfCraft and GridCraft make client proposals, contracts, client PDFs and status reports. They stay optional while they are alpha quality.

## Out of scope

**Later.** Each item comes back when its trigger happens. It is then added like a Hub capability: one at a time, with its own decision.

- **Selling the studio, or one of its parts, to other people.** The vision doc names other developers and product creators as the wider audience. Deferred: the studio is the owner's business tool first. A sale is a separate decision, and it brings a brand name and a trademark check (ADR 0001).
- **An SEO and analytics engine.** Deferred until a real project needs it. The number of engines stays small.
- **Slack and other channels in the inbox.** Deferred until a client needs one. A client's own Slack workspace probably needs a custom bridge.
- **Reading results through analytics and payment APIs.** For now, the owner types the numbers into each results check (ADR 0006). It comes back when typing them becomes a real cost, for example with 3 or more live projects.
- **Elapsed time in the client portal.** Not needed now. It comes back when a client asks for it.
- **Automatic collection from Starter Story.** Its terms say nothing about AI analysis or scraping, and they allow republishing only for non-commercial use. For now, the owner reads it by hand. It comes back when Starter Story gives written permission, or a lawyer reads the terms and allows it.

**Never.** These are limits of the design. Each one protects a rule of the studio.

- **Running an engine from the Hub.** The Hub shows the results of the engines and does not do their work again. Engines run in Claude Code, and each one works when the Hub is offline.
- **Changing a project's stage or files from the Hub.** The Hub only reads. The owner sets the `build`, `live` and `closed` stages by hand in the project file (ADR 0003).
- **AI that sends messages to clients.** AI can summarise client messages and draft replies. Only the owner sends.

## Constraints

| Constraint | Source |
|---|---|
| The interface and the logic of every workflow are simple. Notion was rejected because it takes too much learning before it is useful. | decision record; vision doc |
| One person maintains every part: one toolchain (strict TypeScript, Node 26, npm, `vite-plus`) and one small CI per repo. | ADR 0004 |
| Every engine works without the Hub. The Hub reads only files pushed to the default branch on GitHub, and never changes them. | ADR 0003 |
| One slug names an idea in every part: `a-z`, `0-9` and single dashes, 40 characters or fewer. It never changes. | ADR 0003 |
| The build order is: (1) check the concept, (2) engines work end to end, (3) the Hub, (4) client features and the GitHub integration. | decision record |
| Step 2 is done when one real idea goes from `idea-grill` to a running prototype with no text copied by hand. | decision record |
| AI makes errors when it reads a source: 1.8% to 3.3% for the best models on news-style articles. Human checks find more errors on long and complex text, such as books. So the owner approves each practice proposal before it changes an engine. | [`ai-proposals-accepted.md`](https://github.com/stubbornweb/opportunities/blob/main/ideas/solo-product-studio/research/ai-proposals-accepted.md); ADR 0005 |
| About one third of tested ideas improved their target metric at Microsoft, and no study covers solo builders. So a practice from a source is "worth testing" until the owner marks it proven. | [`outside-practices-improve-results.md`](https://github.com/stubbornweb/opportunities/blob/main/ideas/solo-product-studio/research/outside-practices-improve-results.md); ADR 0005 |
| Starter Story has no API or export. It is read by hand. | [`starter-story-access-terms.md`](https://github.com/stubbornweb/opportunities/blob/main/ideas/solo-product-studio/research/starter-story-access-terms.md) |
| The results check starts with no monthly cost: Google Analytics 4 for visits, Stripe for payments (fees per sale only). Reading visits through the Plausible API needs its $19 a month plan. | [`results-collection-cost.md`](https://github.com/stubbornweb/opportunities/blob/main/ideas/solo-product-studio/research/results-collection-cost.md) |
| In a one-day sample of Upwork and Useme, clients asked most for design and build work. Prototype and launch work was rarely named. | [`paid-demand-for-engine-work.md`](https://github.com/stubbornweb/opportunities/blob/main/ideas/solo-product-studio/research/paid-demand-for-engine-work.md) |
| One client never sees the data of another client. Nothing reaches the client portal until it is marked as visible to the client. | vision doc |
| Secret values never enter an AI process. Client messages are untrusted input for AI. | vision doc |
| Before the first client code or client credential goes into a repo, the full security checklist is in place. | ADR 0004 |

The vision doc is [`docs/sources/2026-11-03-vision.md`](docs/sources/2026-11-03-vision.md). The ADRs are in [`docs/adr/`](docs/adr/).

## Open questions

- How does a project take references (examples such as award sites) as input, and where does the project repo keep them?
- Is `opportunity-scan` rebuilt, or is its mention removed from the Idea Engine?
- Which numbers matter most on the Hub's board?
- Will the owner find paying clients again? The decision record keeps this assumption open.
