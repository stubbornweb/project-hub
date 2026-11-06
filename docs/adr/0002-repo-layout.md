# Repo layout: tools, notes and code apart

Each part of the studio has its own repo. Every idea has one **meta repo** for its notes and the output of every stage. Every product gets one **code repo** for its code. All studio repos belong to `stubbornweb`. The repos are:

| Repo | Holds | Visibility |
| --- | --- | --- |
| `studio` | Glossary, system ADRs, the system brief, wayfinder maps, the one plugin marketplace, the `studio` plugin. It is the meta repo of the studio itself, and the engine repos are its code repos | public |
| `hub` | The Hub. Made when the Hub build starts | public |
| `idea-engine` | Idea Engine skills, as one plugin | public |
| `prototype-engine` | Prototype Engine CLI, skills, templates and patterns, as one plugin | public |
| `design-engine` | Design Engine tools. Made only when the engine has its first tool | public |
| `clients-meta` | Client folders. Made when the first client arrives | private |
| `<slug>-meta`, one per idea | The notes, research, sources and the output of every stage | private |
| `<slug>`, one per product | Only the product code. Made when the build starts | private for a client project, public or private for an own project |

Rules:

- **Engine repos hold only tools.** No engine keeps output inside its repo. The example prototype `demo-studio` and the patterns in `patterns/` are part of the tool, so they stay. Remove client content from a pattern before it goes into the repo.
- **A meta repo is made when work on an idea starts:** the first `idea-grill`, a quick experiment, or an existing product that joins. It stays the same repo when the idea becomes a project, so nothing moves at PROCEED. Each stage has its own top folder, in stage order.
- **A REJECT verdict archives the meta repo.** PARK and REFINE keep it open, because the owner comes back to the idea. An archived repo is read-only, and `gh repo list --no-archived` hides it.
- **A code repo is made when the build starts.** It holds the code, its CI and the files for agents, and no notes. The notes stay in the meta repo.
- **Client folders are in `clients-meta`**, because one client can order several projects.
- **Each engine repo is a Claude Code plugin**, so its skills work inside any meta repo or code repo. The `studio` repo holds the one marketplace that lists them.
- The registry repos (`web-developmet-registry`, `the-registry`) are not part of the studio.

## Considered options

- **One big repo for all engines, or one skills repo for all skills.** Rejected: the engines change at different speeds, and the vision doc keeps them apart.
- **Studio documents in the `hub` repo.** Rejected: the Hub is one part. Studio documents inside it would break the rule that the Hub only reads from the other parts.
- **Prototype output in `prototype-engine/prototypes/<slug>/`.** Rejected: output then lives inside a tool repo.
- **One project repo with the notes and the code together, made at PROCEED.** Rejected: the code repo then holds many Markdown files, and the idea files must move between repos at PROCEED.
- **One shared meta repo for all ideas and projects.** Rejected: a client cannot get access to only their own project. The studio also already uses one meta repo (`studio`) with code repos, so one pattern now works everywhere. Most ideas die, but an archived meta repo costs nothing.
- **A local scratch folder with no git for quick experiments.** Rejected: the experiment has no backup, and it must move when its idea gets PROCEED.
- **Every repo public.** Rejected: meta repos, `clients-meta` and client code repos hold raw client messages and client code. A public repo cannot be fully made private again.

## Consequences

- The 8 web skills move from `prototype-engine/.claude/skills/` into the Prototype Engine plugin.
- The ideas in `idea-workspace` move into their own meta repos. Then `idea-workspace` is archived.
- The portfolio repo `stubbornweb/yevhenii-portfolio` goes into `yevheniibuilds-meta/3-prototype/site/`, and then it is archived.
- ADR 0003 gives the folder names, the project file, and how a meta repo is made.
