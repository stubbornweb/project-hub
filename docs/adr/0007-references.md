# References

A project keeps its references in a "References" section of its brief, `1-idea/PROJECT-DESCRIPTION.md`. Each engine that reads the brief also gets the references, so no engine needs a new reader.

## The section

One line for each reference: a link, and what to take from it.

```markdown
## References

- [Myth Atlas prompt](https://motionsites.ai/?prompt=phoenix-ignis): the 3D model drag, zoom and spin feel; not the museum look, and not its code
- [apple.com](https://apple.com): the scroll effect, not the colours or the logo
```

- The "what to take" part says which pattern to borrow. The engine takes the pattern and writes its own code. It does not copy the look or the code of the reference.
- A reference is a link only, with no images.
- When a link can break, for example a prompt that a site can remove or put behind a login, the owner saves a copy as `1-idea/references/<name>.md`. The line then links to that file.

## Who adds references

- `client-intake` saves the examples that a client sends. `project-brief` copies them into the section.
- `project-brief` asks the owner for example sites when it writes the brief.
- The owner can add a line by hand at any stage.

## What is not a reference

- A link that no project uses yet. It goes in the Hub's link library.
- A part that the owner wants in many projects. It is a pattern of the Prototype Engine, and it enters the engine through a practice proposal (ADR 0005).

## Considered options

- **A `2-design/REFERENCES.md` file.** Rejected: every engine needs code to read a second file, and `2-design/` would exist before the design stage has output (ADR 0003).
- **A file at the repo root.** Rejected: the product code takes the root.
- **A link only, with no "what to take".** Rejected: the engine then guesses what to take, and it can copy the whole look.
- **Screenshots next to the brief.** Rejected for now: a second place, a naming rule and image files in git. A saved copy covers a link that can break.
- **No saved place: paste the reference into the Claude Code session.** Rejected: a session forgets it when it ends, and the Prototype Engine starts from files.

## Consequences

- Nothing changes by this decision. After the map, these changes follow:
  - `PROJECT-DESCRIPTION-FORMAT.md` gets the "References" section, and `project-brief` asks for example sites.
  - `client-intake` saves the examples that a client sends.
- The Prototype Engine gets the references when it reads the brief inside a meta repo (ADR 0003).
