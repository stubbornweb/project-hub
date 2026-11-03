# Repo layout: tools, output and studio documents apart

Each part of the studio has its own repo, and every project has one **project repo**. All studio repos belong to `stubbornweb`. The repos are:

| Repo | Holds | Visibility |
| --- | --- | --- |
| `studio` (today `project-hub`) | Glossary, system ADRs, the system brief, wayfinder maps, the one plugin marketplace | public |
| `hub` | The Hub. Made when the Hub build starts | public |
| `idea-engine` (today `YevheniiVolosiuk/skills`) | Idea Engine skills, as one plugin | public |
| `prototype-engine` | Prototype Engine CLI, skills, templates and patterns, as one plugin | public |
| `design-engine` | Design Engine tools. Made only when the engine has its first tool | public |
| `idea-workspace` (today `opportunities`) | Idea folders and client folders | private |
| `<slug>`, one per project | The idea folder and the output of every stage | private for a client project, public or private for an own project |

Rules:

- **Engine repos hold only tools.** No engine keeps output inside its repo. The example prototype `demo-studio` and the patterns in `patterns/` are part of the tool, so they stay. Remove client content from a pattern before it goes into the repo.
- **A project repo is made at PROCEED.** The idea folder moves into it. After that, every engine writes into it. Each stage has its own top folder, in stage order.
- **A prototype before PROCEED** lives in a local scratch folder, `~/www/prototypes/<slug>/`, with no git. At PROCEED it moves into the project repo.
- **Client folders stay in the idea workspace**, because one client can order several projects. A client project repo names its client by the client's slug.
- **Each engine repo is a Claude Code plugin**, so its skills work inside any project repo. The `studio` repo holds the one marketplace that lists them.
- The registry repos (`web-developmet-registry`, `the-registry`) are not part of the studio.

## Considered options

- **One big repo for all engines, or one skills repo for all skills.** Rejected: the engines change at different speeds, and the vision doc keeps them apart.
- **Studio documents in the `hub` repo.** Rejected: the Hub is one part. Studio documents inside it would break the rule that the Hub only reads from the other parts.
- **Studio documents in the idea workspace.** Rejected: that repo is private and holds raw client messages.
- **Prototype output in `prototype-engine/prototypes/<slug>/`, as today.** Rejected: output then lives inside a tool repo.
- **A project repo at the first prototype.** Rejected: most experiments die, and each one would leave a repo behind.
- **Every repo public.** Rejected: the idea workspace and client project repos hold raw client messages and client code. A public repo cannot be fully made private again.

## Consequences

- Repos to rename or move later: `project-hub` to `studio`, `opportunities` to `idea-workspace`, `YevheniiVolosiuk/skills` to `stubbornweb/idea-engine`. `prototypes/portfolio-studio/` (repo `stubbornweb/yevhenii-portfolio`) moves out of the engine folder.
- The 8 web skills move from `prototype-engine/.claude/skills/` into the Prototype Engine plugin.
- The exact names of the stage folders, how an engine finds the project repo, and the link to the client go to the contracts between the parts.
