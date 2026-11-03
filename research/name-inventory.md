# Name inventory

Date: 2026-11-03

This file lists the names and concepts used in four sources. It only reports what the sources say. It does not pick a winner for any clash.

## How this was made

- Files were read with read-only commands. No git command was run.
- The opportunities folder is private. Only its folder layout, file names and file formats are described. No idea content is quoted. Idea folders are written as `<idea-slug>`.
- All paths are absolute. Line numbers count from line 1 of each file.
- The visibility of the public repos comes from the caller brief. It was not checked online.

Words used in this file:

- **Slug:** a short lowercase name with dashes, for example `my-idea-name`. It names a folder or a file.
- **Markdown:** plain text files with light formatting. Most documents here use it.
- **YAML:** a simple text format of `key: value` lines.
- **Frontmatter:** the header block at the top of a skill file, between `---` lines.
- **Scaffold:** create starter files and folders for a new site.
- **Shell (in the engine):** the base framework of a site. The engine uses Astro or React.
- **Gitignore:** a file that lists paths that git must skip.

---

## 1. Parts

| Part | Repo name and owner | Visibility | Local path |
|---|---|---|---|
| Skills (product skills) | `skills`. GitHub: `YevheniiVolosiuk/skills`. Owner: Yevhenii Volosiuk (`/home/yevhenii/www/skills/.claude-plugin/plugin.json:6`, repo URL at `:8`). | Public (caller brief) | `/home/yevhenii/www/skills/skills/product` (repo root: `/home/yevhenii/www/skills`) |
| Prototype engine | `prototype-engine`. GitHub: `stubbornweb/prototype-engine`. Owner: stubbornweb (`/home/yevhenii/www/prototype-engine/CLAUDE.md:67`). | Public (caller brief) | `/home/yevhenii/www/prototype-engine` |
| Opportunities | `opportunities`. Owner: Yevhenii Volosiuk (caller brief; the folder does not name the owner). | Private (`/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:7` says "private GitHub repo") | `/home/yevhenii/opportunities` (same as `~/opportunities`) |
| Vision doc and handoff | `project-hub-product` (folder name). Owner: not stated in the files. The vision author line says `@Stubborned` (`/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:3`). | Not stated | `/home/yevhenii/www/project-hub-product/docs/sources` |

### Other skill folders under `skills/`

There are no other skill folders. The folder `/home/yevhenii/www/skills/skills/` holds one folder, `product`. The four skill folders under `product` are:

| Skill folder | One-line purpose (from the SKILL.md description) |
|---|---|
| `client-intake` | Turns a pasted job post or client message into questions, an intake, a proposal and a logged pain. (`/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:3`) |
| `idea-grill` | Grills a raw idea down to one verdict: PROCEED, REFINE, PARK or REJECT. (`/home/yevhenii/www/skills/skills/product/idea-grill/SKILL.md:3`) |
| `idea-research` | Turns open assumptions into ranked research questions, then sends them out. (`/home/yevhenii/www/skills/skills/product/idea-research/SKILL.md:3`) |
| `project-brief` | Writes `PROJECT-DESCRIPTION.md`: what is built, for whom, and what is out of scope. (`/home/yevhenii/www/skills/skills/product/project-brief/SKILL.md:3`) |

---

## 2. Names per part

### 2.1 Skills (product)

| Concept | Name the part uses | Where (path:line) |
|---|---|---|
| idea | The word "idea". Skill `idea-grill`. Folder `ideas/<slug>/`. | `/home/yevhenii/www/skills/skills/product/idea-grill/SKILL.md:2`; `/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:20`; `/home/yevhenii/www/skills/skills/product/idea-grill/IDEA-DECISION-FORMAT.md:1` (title `# <Idea name>`) |
| slug | `<slug>`, `<question-slug>`, `<client-slug>`. Rule: lowercase kebab-case, named for the thing it does. | `/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:25`, `:40-45`; `/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:14` |
| client | Folder `clients/`, `<client-slug>`, and the word "client" for the person who posts work. | `/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:12`, `:14`; `/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:2`, `:8`, `:14` |
| project | Skill `project-brief`, file `PROJECT-DESCRIPTION.md`, "project repo", title `<Project name>`. | `/home/yevhenii/www/skills/skills/product/project-brief/SKILL.md:2`, `:8`, `:40`; `/home/yevhenii/www/skills/skills/product/project-brief/PROJECT-DESCRIPTION-FORMAT.md:1` |
| site | none | No match in the skills folder. |
| product | The category name `product`. Also "no `product-` prefix" rule. | `/home/yevhenii/www/skills/skills/product/README.md:1`; `/home/yevhenii/www/skills/README.md:25`, `:32`; `/home/yevhenii/www/skills/.claude-plugin/plugin.json:12` |
| prototype | none | No match in the skills folder. |
| brief | Skill name `project-brief`. Text: "A brief earns its keep through what it excludes." | `/home/yevhenii/www/skills/skills/product/project-brief/SKILL.md:2`, `:6`, `:10` |
| engine | none | No match in the skills folder. |
| phase | none | No match in the skills folder. |
| status | The `State:` line in the decision file. The `Status` column in the assumptions table. | `/home/yevhenii/www/skills/skills/product/idea-grill/IDEA-DECISION-FORMAT.md:3`, `:33`; `/home/yevhenii/www/skills/skills/product/idea-grill/DECISION-STATES.md:1` |

### 2.2 Prototype engine

| Concept | Name the part uses | Where (path:line) |
|---|---|---|
| idea | Used only in plain words in the README. No code name. | `/home/yevhenii/www/prototype-engine/README.md:5` |
| slug | Function `slugify()`. Usage text `<slug>`. Folder `prototypes/<slug>/`. | `/home/yevhenii/www/prototype-engine/src/cli.ts:53-59`, `:20`; `/home/yevhenii/www/prototype-engine/README.md:36` |
| client | "helps the client sell"; "client promotion"; the business that owns the site. | `/home/yevhenii/www/prototype-engine/CLAUDE.md:6`; `/home/yevhenii/www/prototype-engine/README.md:72`; `/home/yevhenii/www/prototype-engine/src/cli.ts:302` |
| project | Internal word for the prototype folder: `cwd: "project"` and parameter `projectDir`. Also "Project code" in the stack policy. | `/home/yevhenii/www/prototype-engine/src/cli.ts:89`, `:219`, `:224`; `/home/yevhenii/www/prototype-engine/docs/stack-policy.md:46` |
| site | Folder `site/` inside a prototype. Argument `"site"` for the scaffold tool. | `/home/yevhenii/www/prototype-engine/src/cli.ts:103`, `:274`, `:290`; `/home/yevhenii/www/prototype-engine/docs/stack-policy.md:50` |
| product | "product" for the business's own product, in customer copy. | `/home/yevhenii/www/prototype-engine/docs/customer-first.md:51`, `:52` |
| prototype | Folder `prototypes/<slug>/`. "Prototype mode". | `/home/yevhenii/www/prototype-engine/src/cli.ts:61-62`, `:298`; `/home/yevhenii/www/prototype-engine/CLAUDE.md:12` |
| brief | Option `--brief`. Section `## Brief`. Key `brief:` in `prototype.yaml`. | `/home/yevhenii/www/prototype-engine/src/cli.ts:29-31`, `:302`, `:307`; `/home/yevhenii/www/prototype-engine/README.md:41` |
| engine | "Prototype Engine" (name). `PROTOTYPE_ENGINE_ROOT`. Function `engineRoot()`. | `/home/yevhenii/www/prototype-engine/README.md:1`; `/home/yevhenii/www/prototype-engine/src/cli.ts:20`, `:25-27` |
| phase | none | No match in the engine folder. |
| status | Key `status: prototype` in `prototype.yaml`. Key `mode: prototype` in one prototype file. | `/home/yevhenii/www/prototype-engine/src/cli.ts:307`; `/home/yevhenii/www/prototype-engine/prototypes/demo-studio/prototype.yaml:3`; `/home/yevhenii/www/prototype-engine/prototypes/portfolio-studio/prototype.yaml:6`, `:14` |

Extra term (not in the list): the shell. The engine uses `astro` or `react` (`/home/yevhenii/www/prototype-engine/src/cli.ts:65`, `:37-44`).

### 2.3 Opportunities (structure only)

| Concept | Name the part uses | Where (path:line) |
|---|---|---|
| idea | Folder `ideas/`. One folder per idea: `ideas/<idea-slug>/`. | `/home/yevhenii/opportunities/ideas/` (folder) |
| slug | `<idea-slug>` (folder name). | `/home/yevhenii/opportunities/ideas/<idea-slug>/` (folder) |
| client | none. No `clients/` folder is present. | none |
| project | none | none |
| site | none | none |
| product | none | none |
| prototype | none | none |
| brief | none. No `PROJECT-DESCRIPTION.md` is present. | none |
| engine | none | none |
| phase | none | none |
| status | A `State` line, and a `Status` column in an assumptions table. | `/home/yevhenii/opportunities/ideas/<idea-slug>/IDEA-DECISION.md:3`, `:81` (State lines); `:46`, `:98` (Status column headers) |

### 2.4 Vision doc and handoff

| Concept | Name the part uses | Where (path:line) |
|---|---|---|
| idea | "idea", "new ideas", "the idea folder". | `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:111`, `:117`, `:128`, `:137` |
| slug | "shared slug", "one slug everywhere", "per slug", `<slug>`. | `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:117`, `:128`, `:129`, `:137` |
| client | "client", "clients", "Client role", "Unified client inbox". | `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:13`, `:33`, `:53`, `:81`; `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-handoff.md:7` |
| project | "project" for each client job. "Project Hub" (product working title). | `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:1`, `:13`, `:32`, `:54`; `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-handoff.md:7` |
| site | "sites", "websites". | `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:13`, `:21`, `:53`; `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-handoff.md:7`, `:62` |
| product | "product" for the Hub and for the ecosystem. "Product principles". | `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:7`, `:36`, `:111` |
| prototype | "Prototype Engine", "a prototype", `prototype-engine new`. | `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:113`, `:121`, `:127`; `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-handoff.md:21` |
| brief | "brief", "Brief → prototype", `--brief`. | `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:121`, `:126`, `:127` |
| engine | "Finding Engine" (the skills), "Prototype Engine" (the CLI), "engines". | `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:113`, `:117`, `:133`; `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-handoff.md:19`, `:21` |
| phase | "agreed phases", "phases". | `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:76`, `:180` |
| status | "status", "status board", "state" (what state each is in), "State line", "status file per slug", "up or down status". | `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:13`, `:54`, `:76`, `:126`, `:129`; `/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-handoff.md:62` |

Other names in the vision doc: "Cockpit" (`:178`) is used once for the first build step. "Hub" is a short name for Project Hub (`:117`).

---

## 3. Files per part

### 3.1 Skills (product)

The skills write only under `~/opportunities/`. The skills repo itself keeps no artifacts (`/home/yevhenii/www/skills/README.md:36`).

**Writes:**

| File | Written by | Format | Where (path:line) |
|---|---|---|---|
| `clients/<client-slug>/` folder | client-intake | Folder | `/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:14` |
| `clients/<client-slug>/NOTES.md` | client-intake (append-only) | Markdown | `/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:14`, `:18` |
| `clients/<client-slug>/INTAKE.md` | client-intake | Markdown, one-screen layout with a text diff block | `/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:42`; `/home/yevhenii/www/skills/skills/product/client-intake/ONE-SCREEN-FORMAT.md:5-30` |
| `clients/<client-slug>/PROPOSAL.md` | client-intake | Markdown with a table | `/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:50`; `/home/yevhenii/www/skills/skills/product/client-intake/PROPOSAL-FORMAT.md:7-18` |
| `clients/PAINS-INDEX.md` (one row per pain) | client-intake | Markdown table | `/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:56`; `/home/yevhenii/www/skills/skills/product/client-intake/PAINS-INDEX-FORMAT.md:5-12` |
| `ideas/<slug>/SIGNALS.md` | client-intake, when a pain reaches 3 clients | Markdown, one heading per source with bold fields | `/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:58`; `/home/yevhenii/www/skills/skills/product/client-intake/SIGNALS-FORMAT.md:5-16` |
| `ideas/<slug>/` folder | idea-grill, step 1 | Folder | `/home/yevhenii/www/skills/skills/product/idea-grill/SKILL.md:24`; `/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:20` |
| `ideas/<slug>/IDEA-DECISION.md` | idea-grill. idea-research adds a dated section at the end. | Markdown with tables | `/home/yevhenii/www/skills/skills/product/idea-grill/SKILL.md:52`; `/home/yevhenii/www/skills/skills/product/idea-grill/IDEA-DECISION-FORMAT.md:1-53`; `/home/yevhenii/www/skills/skills/product/idea-research/SKILL.md:45` |
| `ideas/<slug>/RESEARCH-QUESTIONS.md` | idea-research | Markdown with numbered questions | `/home/yevhenii/www/skills/skills/product/idea-research/SKILL.md:41`; `/home/yevhenii/www/skills/skills/product/idea-research/RESEARCH-QUESTIONS-FORMAT.md:1-39` |
| `ideas/<slug>/research/<question-slug>.md` | The research skill, sent by idea-research | Markdown (no format file in these sources) | `/home/yevhenii/www/skills/skills/product/idea-research/SKILL.md:43`; `/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:24-25` |
| `PROJECT-DESCRIPTION.md` (project root, or the idea folder if no project repo) | project-brief | Markdown | `/home/yevhenii/www/skills/skills/product/project-brief/SKILL.md:40`; `/home/yevhenii/www/skills/skills/product/project-brief/PROJECT-DESCRIPTION-FORMAT.md:1-42` |

**Reads:**

| File | Read by | Where (path:line) |
|---|---|---|
| `WORKSPACE.md` (location rules) | idea-grill, client-intake | `/home/yevhenii/www/skills/skills/product/idea-grill/SKILL.md:24`; `/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:14` |
| `SIGNALS.md` (if it exists) | idea-grill | `/home/yevhenii/www/skills/skills/product/idea-grill/SKILL.md:24`, `:32` |
| `FILTERS.md`, `DECISION-STATES.md`, `IDEA-DECISION-FORMAT.md` | idea-grill | `/home/yevhenii/www/skills/skills/product/idea-grill/SKILL.md:32`, `:50`, `:52` |
| `SIGNALS-FORMAT.md` (signal ladder) | idea-grill, through FILTERS | `/home/yevhenii/www/skills/skills/product/idea-grill/FILTERS.md:7` |
| `MOM-TEST.md`, `DEMAND-SIDE-SALES.md`, `WIN-WITHOUT-PITCHING.md`, `PAINS-INDEX-FORMAT.md`, `ONE-SCREEN-FORMAT.md`, `PROPOSAL-FORMAT.md` | client-intake | `/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:24`, `:34`, `:42`, `:48`, `:50`, `:56` |
| `NOTES.md`, `clients/PAINS-INDEX.md` | client-intake | `/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:14`, `:56` |
| `IDEA-DECISION.md`, `research/` | idea-research, project-brief | `/home/yevhenii/www/skills/skills/product/idea-research/SKILL.md:14`; `/home/yevhenii/www/skills/skills/product/project-brief/SKILL.md:14` |
| `RESEARCH-QUESTIONS-FORMAT.md` | idea-research | `/home/yevhenii/www/skills/skills/product/idea-research/SKILL.md:41` |
| `PROJECT-DESCRIPTION-FORMAT.md` | project-brief | `/home/yevhenii/www/skills/skills/product/project-brief/SKILL.md:24` |
| `.claude-plugin/plugin.json` (JSON, lists the four skill paths) and `marketplace.json` (JSON) | Plugin system | `/home/yevhenii/www/skills/.claude-plugin/plugin.json:18-22`; `/home/yevhenii/www/skills/.claude-plugin/marketplace.json:1-23` |

Skill files are Markdown. Each `SKILL.md` starts with frontmatter (name and description). Example: `/home/yevhenii/www/skills/skills/product/idea-grill/SKILL.md:1-4`.

### 3.2 Prototype engine

**Writes (by the CLI in `/home/yevhenii/www/prototype-engine/src/cli.ts`):**

| File | Written by (command) | Format | Where (path:line) |
|---|---|---|---|
| `prototypes/<slug>/` folder | `new` | Folder | `/home/yevhenii/www/prototype-engine/src/cli.ts:297-300` |
| `prototypes/<slug>/EXPERIENCE.md` | `new` | Markdown spec | `/home/yevhenii/www/prototype-engine/src/cli.ts:302`, `:304` |
| `prototypes/<slug>/prototype.yaml` | `new`. `scaffold` changes the `shell:` line with a pattern match. | YAML-style text | `/home/yevhenii/www/prototype-engine/src/cli.ts:306-308`, `:284-288` |
| `prototypes/<slug>/BUILD_PROMPT.md` (placeholder) | `new` | Markdown | `/home/yevhenii/www/prototype-engine/src/cli.ts:310-312` |
| `prototypes/<slug>/BUILD_PROMPT.md` (full prompt) | `build` | Markdown with a fenced text block | `/home/yevhenii/www/prototype-engine/src/cli.ts:359-361` |
| `prototypes/<slug>/qa/CHECKLIST.md` | `new` | Markdown checklist | `/home/yevhenii/www/prototype-engine/src/cli.ts:314-316` |
| `prototypes/<slug>/qa/RESULT.md` | `review` (keeps old text below the new checklist) | Markdown checklist | `/home/yevhenii/www/prototype-engine/src/cli.ts:385-388` |
| `prototypes/<slug>/site/` folder and its files | `scaffold` (runs the official tools, then edits files) | Folder; `package.json` and `tsconfig` are JSON; `astro.config.ts`, `vite.config.ts`, `src/App.tsx` are TypeScript; `src/pages/index.astro` is Astro | `/home/yevhenii/www/prototype-engine/src/cli.ts:118-124` (package.json), `:151-163` (Astro), `:172-204` (React and tsconfig, vite config, `src/index.css`, `src/App.tsx`, removals) |
| `patterns/<pattern-id>/PATTERN.md` | `extract-pattern` | Markdown | `/home/yevhenii/www/prototype-engine/src/cli.ts:404-419` (write at `:414-417`) |

**Reads (by the CLI):**

| File or folder | Read by (command) | Where (path:line) |
|---|---|---|
| `docs/stack-policy.md` | `build` (injected into the prompt) | `/home/yevhenii/www/prototype-engine/src/cli.ts:327`, `:321-325` |
| `docs/customer-first.md` | `build` (injected into the prompt) | `/home/yevhenii/www/prototype-engine/src/cli.ts:328` |
| `prototypes/<slug>/EXPERIENCE.md` | `build` | `/home/yevhenii/www/prototype-engine/src/cli.ts:334` |
| `prototypes/<slug>/prototype.yaml` | `scaffold` | `/home/yevhenii/www/prototype-engine/src/cli.ts:284-286` |
| `site/package.json` | `scaffold` (JSON edit) | `/home/yevhenii/www/prototype-engine/src/cli.ts:233-243` |
| `patterns/` folder (folder names only) | `build` | `/home/yevhenii/www/prototype-engine/src/cli.ts:343-352` |
| `qa/RESULT.md` (if it exists) | `review` | `/home/yevhenii/www/prototype-engine/src/cli.ts:385-386` |
| Environment: `PROTOTYPE_ENGINE_ROOT`, `CLAUDE_BIN` | CLI | `/home/yevhenii/www/prototype-engine/src/cli.ts:20`, `:26`, `:363` |

**Repo files (not written by the CLI):**

| File or folder | Format | Where (path:line) |
|---|---|---|
| `docs/` (7 files: `customer-first.md`, `prototype-loop.md`, `mcp.md`, `architecture.md`, `stack-policy.md`, `agents/domain.md`, `agents/issue-tracker.md`) | Markdown | `/home/yevhenii/www/prototype-engine/docs/` |
| `.claude/skills/` (8 folders: `prototype-engine`, `web-design`, `web-motion`, `web-3d`, `web-video`, `web-visual-qa`, `web-patterns`, `web-production`) | Markdown with frontmatter | `/home/yevhenii/www/prototype-engine/.claude/skills/prototype-engine/SKILL.md:1-4` |
| `patterns/README.md`; `patterns/cinematic-hero/` (`PATTERN.md`, `recipe.md`); `patterns/architecture-hero/` (`PATTERN.md` only) | Markdown | `/home/yevhenii/www/prototype-engine/patterns/README.md:5-10`; `/home/yevhenii/www/prototype-engine/patterns/architecture-hero/PATTERN.md:33` |
| `templates/astro-marketing/public/` | Empty folder | `/home/yevhenii/www/prototype-engine/templates/` |
| `outputs/`, `qa/` (root) | Empty folders | `/home/yevhenii/www/prototype-engine/` |
| `package.json` (JSON). `bin` is `src/cli.ts`. Check script is `vp check`. Node 22.18 or newer. | JSON | `/home/yevhenii/www/prototype-engine/package.json:4-8`, `:11`, `:18-20` |
| `README.md`, `CLAUDE.md` | Markdown | `/home/yevhenii/www/prototype-engine/README.md`; `/home/yevhenii/www/prototype-engine/CLAUDE.md` |

**Prototype folders and git (from `.gitignore`):**

- `/home/yevhenii/www/prototype-engine/.gitignore:9` ignores `prototypes/*`.
- `/home/yevhenii/www/prototype-engine/.gitignore:10` un-ignores `prototypes/demo-studio/`.
- So `prototypes/demo-studio/` is in git. Its files still follow any inner `.gitignore` files.
- `prototypes/portfolio-studio/` is not in git under the root rule. It has its own `.git` folder (listing only), so it is a separate repository inside this folder.
- Other root ignore lines: `node_modules/` (`:1`), `dist/` (`:2`), `.idea/` (`:3`), `.vs_code/` (`:4`), `.env*` (`:5`), `.DS_Store` (`:6`), `.vercel/` (`:7`), `.playwright-mcp/` (`:8`).

**Prototype folders present:**

- `prototypes/demo-studio/`: `EXPERIENCE.md`, `prototype.yaml`, `BUILD_PROMPT.md`, `qa/` (`CHECKLIST.md`, `RESULT.md`), `site/` (Astro, with `AGENTS.md`), `src/`, `public/`.
- `prototypes/portfolio-studio/`: `EXPERIENCE.md`, `ASSET-BRIEF.md`, `prototype.yaml`, `qa/` (`CHECKLIST.md`, `shots/`), `src/`, `public/`, `dist/`, `index.html`, `vite.config.js`, `package.json`.

### 3.3 Opportunities (structure only)

| File or folder | Format | Where |
|---|---|---|
| `ideas/<idea-slug>/IDEA-DECISION.md` | Markdown with a `State` line, Filters table, Assumptions table, and a dated revisions section. Layout matches the skill template. | `/home/yevhenii/opportunities/ideas/<idea-slug>/IDEA-DECISION.md:3`, `:46`, `:81`, `:98` |
| `ideas/<idea-slug>/RESEARCH-QUESTIONS.md` | Markdown with four level-2 section headings. Layout matches the skill template. | `/home/yevhenii/opportunities/ideas/<idea-slug>/RESEARCH-QUESTIONS.md:6`, `:34`, `:50`, `:59` |
| `ideas/<idea-slug>/research/` | Folder with 2 Markdown files. Names follow `<question-slug>.md`. | `/home/yevhenii/opportunities/ideas/<idea-slug>/research/` |
| `.git/` | Git repository folder. Not read. No git command was run. | `/home/yevhenii/opportunities/.git` |

The folder does not contain these files that the skills describe (`/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:9-27`):

- `INDUSTRIES.md`
- `clients/` (with `PAINS-INDEX.md` and client folders)
- `ideas/BACKLOG.md`
- `ideas/<idea-slug>/SIGNALS.md`
- `ideas/<idea-slug>/PROJECT-DESCRIPTION.md`

WORKSPACE.md says a missing file means that stage has not run (`WORKSPACE.md:29`).

This folder reads and writes nothing else. It is a store. The skills write into it.

### 3.4 Vision doc and handoff

- Files: `2026-11-03-vision.md`, `2026-11-03-handoff.md`, `README.md` in `/home/yevhenii/www/project-hub-product/docs/sources/`. All are Markdown snapshots (`docs/sources/README.md:3`: "Do not edit them").
- Writes: none.
- Reads: none. These files are inputs to a future product. They name these files the Hub will read or use:
  - `IDEA-DECISION.md`, its `State` line (`2026-11-03-vision.md:126`, `:138`)
  - `SIGNALS.md` (`:125`)
  - `PROJECT-DESCRIPTION.md` (`:127`)
  - `NOTES.md` (`:142`)
  - "A small status file per slug, committed to git" (`:129`). No file format is defined for it.
- Handoff: "No code exists yet, and no repository was changed." (`2026-11-03-handoff.md:3`).

---

## 4. Expectations between parts

### 4.1 Skills expect

- A workspace at `~/opportunities/` (`/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:7`, `:10`).
- External skills `mattpocock-skills:grilling` (`idea-grill/SKILL.md:10`, `:40`) and `mattpocock-skills:research` (`idea-research/SKILL.md:43`). Both are named in `/home/yevhenii/www/skills/skills/product/README.md:17-18`.
- The `AskUserQuestion` tool for every question (`idea-grill/SKILL.md:14`).
- A tool named `opportunity-scan`: named in `WORKSPACE.md:11`, `:19`, `:21`. No folder or file for it exists in the skills repo (`/home/yevhenii/www/skills/skills/` holds only `product`).
- A project repo with a `docs/ideas/<slug>/` folder (`WORKSPACE.md:31`; `project-brief/SKILL.md:40-42`).
- Nothing from the prototype engine. A search of the skills folder finds no reference to the prototype engine.
- Plugin install from `YevheniiVolosiuk/skills` (`/home/yevhenii/www/skills/README.md:46-51`).

### 4.2 Prototype engine expects

- Node.js 22.18 or newer (`/home/yevhenii/www/prototype-engine/README.md:29`; `package.json:18-20`).
- The `npm` tool to run `npm create vite-plus@latest`. This runs the official Astro or Vite tool (`src/cli.ts:83-92`, `:131`, `:169`).
- A Claude Code executable named `claude`, or a name set in `CLAUDE_BIN` (`src/cli.ts:363`, `:20`).
- A Vercel command-line tool named `vercel` (`src/cli.ts:396`; `docs/stack-policy.md:144`; `README.md:24`).
- Docs at `docs/stack-policy.md` and `docs/customer-first.md`, read at run time (`src/cli.ts:327-328`).
- A `patterns/` folder at the engine root (`src/cli.ts:344`).
- The `web-production` skill for promotion (`src/cli.ts:302`: "Client promotion requires the production gate in `.claude/skills/web-production/SKILL.md`").
- Eight skills in `.claude/skills/` (`CLAUDE.md:18-27`).
- `GLOSSARY.md` and `docs/adr/` at the repo root (`CLAUDE.md:71`; `docs/agents/domain.md:7-9`). **Not present** in the engine folder.
- GitHub Issues for `stubbornweb/prototype-engine`, with the `gh` tool (`CLAUDE.md:67`; `docs/agents/issue-tracker.md:5`).
- Context7 docs for Tailwind, library `/tailwindlabs/tailwindcss.com` (`docs/stack-policy.md:90-91`).
- Playwright for browser checks (`docs/stack-policy.md:145`; `docs/mcp.md:13-15`).
- A reference file in another prototype, `prototypes/portfolio-studio/src/lib/useVideoSource.js` (`docs/stack-policy.md:126`).
- An optional MCP service named MotionSites (`docs/mcp.md:3-11`).
- No `.github/` folder exists in the engine root. Its CI status cannot be read from the files (`ls -a` listing).
- Nothing from the skills repo or the Hub. The engine does not name `~/opportunities` or Project Hub.

### 4.3 Opportunities expects

- Its file layout follows the skills workspace layout (`/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:9-27`).
- No config or link file in the folder names another part. Only the folder layout and formats were checked.

### 4.4 Vision doc and handoff expect

- The skills at `https://github.com/YevheniiVolosiuk/skills/tree/main/skills/product` (`2026-11-03-handoff.md:19-20`).
- The engine at `https://github.com/stubbornweb/prototype-engine` (`2026-11-03-handoff.md:21`). The handoff says it could not be read there (`:22-23`). A local copy now exists at `/home/yevhenii/www/prototype-engine`.
- A local skills clone at `/home/claude/yevheniivolosiuk/skills` (`2026-11-03-handoff.md:25`). The session that read the skills used `/home/yevhenii/www/skills`.
- `prototype-engine new` takes `--brief` (`2026-11-03-vision.md:127`). This matches `src/cli.ts:29-31`.
- A `promote` command for prototype-to-client (`2026-11-03-vision.md:128`). **No such command exists**. The command switch in `src/cli.ts:425-445` has no `promote` case. `README.md:5` and `README.md:72` describe client promotion in plain words only.
- A `--from` option that reads `PROJECT-DESCRIPTION.md` (`2026-11-03-vision.md:127`). Not present in `src/cli.ts`.
- `IDEA-DECISION.md` with a `State` line, read by the Hub (`2026-11-03-vision.md:126`, `:138`).
- `SIGNALS.md` created by client-intake (`2026-11-03-vision.md:125`).
- `npm run check` in CI for the CLI (`2026-11-03-vision.md:140`). The engine has a `check` script (`package.json:11`). No CI folder exists in the engine root.
- A `LICENSE` file for the skills repo, because `plugin.json` declares MIT (`2026-11-03-vision.md:140`; `/home/yevhenii/www/skills/.claude-plugin/plugin.json:9`). **No LICENSE file exists** in `/home/yevhenii/www/skills`.
- A `prototypes/<slug>/` folder that is moved out of the engine folder (`2026-11-03-vision.md:141`).
- `NOTES.md` as raw client messages (`2026-11-03-vision.md:142`). This matches `client-intake/SKILL.md:14-18`.
- The skills and the Hub use the same slug (`2026-11-03-vision.md:137`).

---

## 5. Clashes table

Types:

- **One thing, two names:** one concept has two or more names.
- **One name, two things:** one word means two or more concepts.
- **Concept in two places:** one concept is written or stored in two places, or the docs and the files differ.

| Type | Concept or name | Where each use is (path:line) | What differs |
|---|---|---|---|
| One thing, two names | Product engine set | Vision: "Finding Engine" (`/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:113`; `2026-11-03-handoff.md:19`). Skills repo: "Personal agent skills" (`/home/yevhenii/www/skills/README.md:3`). | The vision calls the skills "Finding Engine." The skills repo does not use that name. |
| One thing, two names | Project Hub | "Project Hub" (`/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:1`, `:13`); "Hub" (`:117`, `:135`); "Cockpit" (`:178`). | "Cockpit" appears once. The vision says the final name is open (`:199`). |
| One thing, two names | Vite+ scaffolder | `vite-plus` package (`/home/yevhenii/www/prototype-engine/src/cli.ts:92`); "Vite+" (`docs/stack-policy.md:58-61`, `:66`; `src/cli.ts:83`); `vite` tool (`src/cli.ts:169`). | "vite" is the create-vite tool. "Vite+" runs create-vite or create-astro. |
| One thing, two names | React shell | `react` value (`src/cli.ts:65`, `:37-44`); "React + Vite+" (`docs/stack-policy.md:30`); `shell: vite` (`/home/yevhenii/www/prototype-engine/prototypes/portfolio-studio/prototype.yaml:8`). | The portfolio file uses `vite`. The CLI accepts only `astro`, `react` or `undecided` (`src/cli.ts:41-43`). |
| One thing, two names | Styling version value | `styling: tailwind-latest-major` (`src/cli.ts:307`; `prototypes/demo-studio/prototype.yaml:8`); `styling: tailwind-v4` (`prototypes/portfolio-studio/prototype.yaml:10`). | One value is a "latest major" label. The other pins v4. |
| One thing, two names | Owner name | `stubbornweb` (`/home/yevhenii/www/prototype-engine/CLAUDE.md:67`; `2026-11-03-handoff.md:21`); `@Stubborned` (`2026-11-03-vision.md:3`); `YevheniiVolosiuk` (`/home/yevhenii/www/skills/.claude-plugin/plugin.json:6`, `:8`; `2026-11-03-handoff.md:19`). | Three names. The files do not say whether they are the same person. |
| One thing, two names | VS Code folder | `.vs_code/` (`/home/yevhenii/www/prototype-engine/.gitignore:4`); `.vscode/` (`/home/yevhenii/www/prototype-engine/prototypes/demo-studio/site/.vscode/`). | The ignore rule names a folder that does not match the real folder name. |
| One thing, two names | Going from prototype to client work | "promote" (`/home/yevhenii/www/prototype-engine/README.md:5`; `.claude/skills/web-production/SKILL.md:3`; `2026-11-03-vision.md:128`); "client promotion" (`README.md:72`; `src/cli.ts:302`); "Client production mode" (`CLAUDE.md:15`). | The vision says no `promote` command exists (`:128`). The CLI has none (`src/cli.ts:425-445`). |
| One thing, two names | Research file name pattern | `research/<question-slug>.md` (`/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:25`, `:38`); `research/<slug>.md` (`/home/yevhenii/www/skills/skills/product/idea-research/RESEARCH-QUESTIONS-FORMAT.md:14`; `/home/yevhenii/www/skills/skills/product/project-brief/PROJECT-DESCRIPTION-FORMAT.md:36`). | One pattern says `question-slug`. The others say `slug`. |
| One thing, two names | Idea folder | `ideas/<slug>/` ("idea folder", `/home/yevhenii/www/skills/skills/product/idea-grill/SKILL.md:24`); "idea workspace" (`project-brief/SKILL.md:14`; `idea-research/SKILL.md:14`); "project memory" (`WORKSPACE.md:3`). | Three names for the same place. |
| One name, two things | `product` | Skills category (`/home/yevhenii/www/skills/skills/product/README.md:1`; `/home/yevhenii/www/skills/.claude-plugin/plugin.json:12`); ecosystem products (`/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-vision.md:111`); the client's product in engine copy (`/home/yevhenii/www/prototype-engine/docs/customer-first.md:51-52`). | Skills category, planned products, and the client's own product. |
| One name, two things | `client` | Person who posts work (`/home/yevhenii/www/skills/skills/product/client-intake/SKILL.md:8`, `:14`); business that hires a prototype (`/home/yevhenii/www/prototype-engine/CLAUDE.md:6`; `src/cli.ts:302`); paying user of the portal (`2026-11-03-vision.md:33`). | The engine calls the end reader a "customer" (`docs/customer-first.md:6-8`). |
| One name, two things | `project` | Written definition (`/home/yevhenii/www/skills/skills/product/project-brief/SKILL.md:8`); repo for a client (`/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:31`); prototype folder in the engine code (`/home/yevhenii/www/prototype-engine/src/cli.ts:89`, `:219`, `:224`); client work (`2026-11-03-vision.md:32`, `:54`). | The engine code uses "project" for a prototype folder. |
| One name, two things | `brief` | A document (`/home/yevhenii/www/skills/skills/product/project-brief/SKILL.md:6`, `:8`); a one-line `--brief` string (`/home/yevhenii/www/prototype-engine/src/cli.ts:29-31`, `:302`, `:307`); "brief → prototype" (`2026-11-03-vision.md:121`, `:127`). | A full file in skills. A short text in the engine. |
| One name, two things | `site` | Folder `site/` inside a prototype (`/home/yevhenii/www/prototype-engine/src/cli.ts:274`; `docs/stack-policy.md:50`); a client's website (`2026-11-03-vision.md:53`; `2026-11-03-handoff.md:62`). | A code folder in the engine. A live website in the vision. |
| One name, two things | `status` | Assumption state column (`/home/yevhenii/www/skills/skills/product/idea-grill/IDEA-DECISION-FORMAT.md:33`); stage key `status: prototype` (`/home/yevhenii/www/prototype-engine/src/cli.ts:307`); project progress (`2026-11-03-vision.md:54`, `:76`). | Three meanings. The skills also use `State` for the verdict (`IDEA-DECISION-FORMAT.md:3`). |
| One name, two things | `mode` and `status` (prototype stage) | `status: prototype` (`src/cli.ts:307`; `prototypes/demo-studio/prototype.yaml:3`; `prototypes/portfolio-studio/prototype.yaml:6`); `mode: prototype` (`prototypes/portfolio-studio/prototype.yaml:14`); "Operating modes" (`/home/yevhenii/www/prototype-engine/CLAUDE.md:10-16`). | Same value, two keys. The `mode` key appears only in the portfolio file. |
| One name, two things | `research` | Folder `research/` (`/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:24`); skill `idea-research` (`idea-research/SKILL.md:6`); external skill `mattpocock-skills:research` (`idea-research/SKILL.md:43`). | A folder and two skills. |
| One name, two things | `prototype-engine` | Repo folder (`/home/yevhenii/www/prototype-engine/README.md:1`); CLI command (`src/cli.ts:20`; `package.json:6-8`); skill (`.claude/skills/prototype-engine/SKILL.md:2`). | Repo, command and skill share one name. |
| One name, two things | `private` | Engine npm flag `"private": true` (`/home/yevhenii/www/prototype-engine/package.json:4`); opportunities GitHub visibility "private" (`/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:7`). | The npm flag is about publishing to npm. The other is GitHub visibility. |
| Concept in two places | Idea folder location | `ideas/<slug>/` (`/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:20`); `<project-root>/docs/ideas/<slug>/` (`WORKSPACE.md:31`; `project-brief/SKILL.md:42`; `2026-11-03-vision.md:128`); real folder `ideas/<idea-slug>/` (`/home/yevhenii/opportunities/ideas/`). | The same folder moves when a project repo exists. |
| Concept in two places | Slug rule | Docs: lowercase kebab-case, named for the thing it does (`/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:42-45`); code: `slugify()` converts any text and trims dashes (`/home/yevhenii/www/prototype-engine/src/cli.ts:53-59`); vision: "one slug everywhere" (`2026-11-03-vision.md:137`). | Docs state a rule. Code converts input. The two do not share a check. |
| Concept in two places | Decision record template and real file | Template (`/home/yevhenii/www/skills/skills/product/idea-grill/IDEA-DECISION-FORMAT.md:1-4`, no version field); real file (`/home/yevhenii/opportunities/ideas/<idea-slug>/IDEA-DECISION.md:3`, `:81`, `:46`, `:98`). Vision asks for a version field (`2026-11-03-vision.md:138`). | The real file has a second `State` line and a second assumptions table in a dated section. The template says to append such sections (`IDEA-DECISION-FORMAT.md:47-53`). |
| Concept in two places | Prototype QA checklist | Created by `new` (`/home/yevhenii/www/prototype-engine/src/cli.ts:315`); written by `review` (`src/cli.ts:387`); demo file (`/home/yevhenii/www/prototype-engine/prototypes/demo-studio/qa/CHECKLIST.md:3-9`, 7 items); portfolio file (`prototypes/portfolio-studio/qa/CHECKLIST.md`). | Three different lists for the same job. |
| Concept in two places | Build prompt text and heading | Placeholder heading `# Build prompt` (`src/cli.ts:311`); full heading `# Claude Code build prompt` (`src/cli.ts:360`); full text template (`src/cli.ts:336`); demo file (`prototypes/demo-studio/BUILD_PROMPT.md:1`, `:6-16`). | The demo file has no stack-policy or customer-first block. The template at `src/cli.ts:336` includes them. |
| Concept in two places | Stack policy | Source: `/home/yevhenii/www/prototype-engine/docs/stack-policy.md:3-7` ("single source of truth"); summary in `README.md:15-25`; summary in `CLAUDE.md:29-37`. | Two summaries exist. `CLAUDE.md:35` says summaries drift. |
| Concept in two places | Customer and QA rules | Source: `docs/customer-first.md:30-43`; restated in `/home/yevhenii/www/prototype-engine/.claude/skills/web-visual-qa/SKILL.md:14-19`; restated in checklist text (`src/cli.ts:315`). | The skill and checklist use shorter versions of the same rules. |
| Concept in two places | Shell choices | Docs: three rows, including "None" with Astro (`docs/stack-policy.md:24-28`). CLI: `astro` and `react` only (`src/cli.ts:65`, `:128`, `:167`). | Docs describe Astro islands. The CLI has no islands option. |
| Concept in two places | Pattern folder contents | Expected four parts (`/home/yevhenii/www/prototype-engine/patterns/README.md:5-10`); `cinematic-hero/` has `PATTERN.md` and `recipe.md`; `architecture-hero/` has only `PATTERN.md`, with a TODO to add a recipe (`patterns/architecture-hero/PATTERN.md:33`). | One pattern has fewer files than the README asks for. |
| Concept in two places | Named tool that is not in the folder | `opportunity-scan`: named in `/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:11`, `:19`, `:21`; in the vision (`2026-11-03-vision.md:149`); in the handoff (`2026-11-03-handoff.md:70`). | Named in the docs. Not present in the skills repo. |
| Concept in two places | Opportunities workspace layout | Expected layout (`/home/yevhenii/www/skills/skills/product/idea-grill/WORKSPACE.md:9-27`); actual folder has only `ideas/<idea-slug>/` with four files. | The expected `clients/`, `INDUSTRIES.md`, `ideas/BACKLOG.md`, `SIGNALS.md` and `PROJECT-DESCRIPTION.md` are not present. |
| Concept in two places | Skills repo local path | `/home/claude/yevheniivolosiuk/skills` (`/home/yevhenii/www/project-hub-product/docs/sources/2026-11-03-handoff.md:25`); `/home/yevhenii/www/skills` (this session's folder). | A different machine path. |
