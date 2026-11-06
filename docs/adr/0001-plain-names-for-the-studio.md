# Plain names for the studio and its parts

The owner may sell parts of the studio, or the whole studio, in the future, but not now. So every part gets a plain name now, and each part can stand alone. A brand name, with a trademark check, is chosen only when a part goes on sale. The names are: the studio (the whole system), the Idea Engine (before: Finding Engine), the Design Engine, the Prototype Engine, and the Hub (before: Project Hub). A repo for one part takes the part's name in lowercase with dashes and no prefix (`hub`, `idea-engine`, `design-engine`, `prototype-engine`). A code repo takes the project's slug, and a meta repo takes the slug with `-meta` at the end. The shared words are in [GLOSSARY.md](../../GLOSSARY.md).

## Considered options

- **"Product Engine" for the first engine.** Rejected: KissMyApps uses the same name, and "product" already had three meanings.
- **"Project Hub".** Rejected: it is one letter away from KissMyApps "Product Hub", and "project" had four meanings.
- **A `studio-` prefix for repo names.** Rejected: longer names, and "studio" is a working word that can change at a sale.
- **Brand names now.** Rejected: they need trademark and domain checks for several names, and nothing is for sale yet.

## Consequences

- Nothing is renamed by this decision. The renames of repos, folders, CLI options and docs happen after the map, and the repo layout ticket decides which repos exist.
- The Prototype Engine's `--brief` option, its `status:` key and its use of "project" for a prototype folder change name later, as part of the contracts between the parts.
