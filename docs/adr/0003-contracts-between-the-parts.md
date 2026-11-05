# Contracts between the parts

Each part of the studio writes plain files, and the next part reads them. These files are the contracts. The Hub reads only files that are pushed to the default branch on GitHub, and it never changes them. No engine needs the Hub.

## Slug

- A slug uses only `a-z`, `0-9` and single dashes. It starts and ends with a letter or a digit, and it has 40 characters or fewer.
- Every tool rejects a wrong slug and shows this rule. No tool changes a slug by itself.
- A slug never changes after its idea folder is made.
- A project slug must not be the name of a studio repo (`studio`, `hub`, `idea-engine`, `design-engine`, `prototype-engine`, `idea-workspace`).
- Client slugs are a separate list, so a client slug can be the same as a project slug.

## Local paths

Every tool uses two fixed paths and no environment variables:

- `~/www/idea-workspace/` holds the idea folders (`ideas/<slug>/`) and the client folders (`clients/<client-slug>/`).
- `~/www/prototypes/<slug>/` holds quick experiments. It has no git.

## Stages

The stages are `idea`, `design`, `prototype`, `build`, `live` and `closed`. A project can start at any stage, skip stages and move back. An idea before PROCEED is always in the `idea` stage.

## Project repo

A project repo has this layout. A stage folder exists only when its stage has output.

```
<slug>/
├── PROJECT.md          the project file
├── README.md           includes the entry note when the project joined at a later stage
├── 1-idea/             the idea folder: IDEA-DECISION.md, research/, PROJECT-DESCRIPTION.md, references/ (ADR 0007)
├── 2-design/
├── 3-prototype/        prototype.yaml, EXPERIENCE.md, site/, qa/
├── 5-live/             results checks
└── package.json, src/ ...   the product code (build stage)
```

The product code takes the repo root, so the build stage has no folder.

## Project file

`PROJECT.md` is the only file the Hub needs from a project repo:

```markdown
# Acme booking site

**Format:** 1
**Stage:** prototype
**Client:** acme
```

- The `**Client:**` line exists only for a client project. An agent finds the client folder at `~/www/idea-workspace/clients/<client-slug>/`.
- The repo name is the slug, so the file has no slug line.
- A `PROJECT.md` at the root marks a project repo. The Hub and the engines use it to find project repos.
- `project-start` sets the stage that the project enters at. Each engine sets its own stage when it starts work. The owner sets `build`, `live` and `closed` by hand.

An idea before PROCEED has no project file. The Hub reads its verdict from the `**Verdict:**` line of `IDEA-DECISION.md` in the idea workspace. This line was `**State:**` before, but the glossary avoids the word "state" for a verdict.

## Format versions

`IDEA-DECISION.md` and `PROJECT.md` are the files the Hub parses. Each has a `**Format:** 1` line under the title. Raise the number only when a change would break the Hub. Other files have no version.

## Starting a project

`project-start` is an Idea Engine skill. It runs once, when an idea gets PROCEED, or when a project joins at a later stage:

1. It makes the repo `stubbornweb/<slug>`, or it adopts the repo if one already exists. A client project repo is private.
2. It moves the idea folder from `~/www/idea-workspace/ideas/<slug>/` into `1-idea/`, if the idea folder exists.
3. It moves a quick experiment from `~/www/prototypes/<slug>/` into `3-prototype/`, if one exists.
4. It writes `PROJECT.md` with the stage the project enters at, and the entry note in `README.md` when the project joins at a later stage.

After that, `project-brief` writes `1-idea/PROJECT-DESCRIPTION.md`.

## Prototype Engine input

The folder the Prototype Engine runs in decides its input:

- Inside a project repo, it reads `1-idea/PROJECT-DESCRIPTION.md`, writes into `3-prototype/` and sets the stage to `prototype`. A project has one prototype. A new direction replaces the old one, and git keeps the old one.
- Anywhere else, `--pitch "<one line>"` makes a quick experiment in `~/www/prototypes/<slug>/`.

`prototype.yaml` has no `status:` key. Its `pitch:` key exists only for a quick experiment.

## Considered options

- **Stage and client as GitHub repo topics, with no file.** Rejected: topic names are always public, even on a private repo, so a client topic shows the client's name.
- **Project facts in `AGENTS.md`, or in `docs/agents/` with a link from `AGENTS.md`.** Rejected: `AGENTS.md` holds instructions, not data that changes. A linked file is still a file, plus a link that the Hub must follow.
- **YAML frontmatter for the format version.** Rejected: no file uses frontmatter today. Every file uses bold lines such as `**Verdict:**`.
- **A record of the tool version on every file.** Rejected: every skill must then know its version, and no repo has release tags.
- **A `--from` option on `prototype-engine new`.** Rejected: the current folder already shows where the brief is.
- **A `promote` command in the Prototype Engine.** Rejected: PROCEED is an Idea Engine verdict, and many projects have no prototype at PROCEED.
- **Project creation inside `project-brief`.** Rejected: `project-brief` also runs for existing projects that have no brief.
- **Product code in a `4-build/` folder.** Rejected: existing sites must then move their code and change their deploy settings.
- **Several prototypes per project.** Rejected: every tool must then ask which prototype to use.
- **Tools that change a wrong slug into a right one.** Rejected: a quietly changed slug breaks the rule of one slug everywhere.

## Consequences

- Nothing changes by this decision. After the map, these changes follow:
  - The Idea Engine gets the `project-start` skill. `WORKSPACE.md` uses the two fixed paths and drops `docs/ideas/<slug>/`.
  - `IDEA-DECISION-FORMAT.md` gets the `**Format:** 1` line, and its `**State:**` line becomes `**Verdict:**`. `DECISION-STATES.md`, the skills that read the line and the existing decision records change with it.
  - `project-brief` writes into `1-idea/`.
  - The Prototype Engine drops `PROTOTYPE_ENGINE_ROOT`, renames `--brief` to `--pitch`, rejects a wrong slug, reads the brief inside a project repo and sets the stage.
- ADR 0006 decides the format of a results check in `5-live/`.
