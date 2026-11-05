# How practices enter an engine

The `learn-from-source` skill turns one source into practice proposals for one engine. The owner approves each proposal, and each approved proposal enters the engine as one pull request. An engine uses a "worth testing" practice in real projects, because only use can prove it.

## The skill

- The skill is in the `studio` plugin, in the `studio` repo. The studio marketplace lists this plugin next to the engine plugins.
- The owner runs the skill inside the repo of the engine to change. The current folder is the target engine.
- The skill reads the source and the engine's rule files. It reads the engine list (the marketplace file) and the studio's goals (the system brief) from the `studio` repo on GitHub with `gh`.

## What the skill shows

The skill sorts the good points of the source into three groups and shows them in the chat:

1. **For this engine:** practice proposals with the seven parts from the decision on AI practice proposals.
2. **For another engine:** one line per point, with the name of the engine. The owner can run the skill again in that engine's repo.
3. **For no engine:** one line that names the missing stage or tool and suggests a new engine. The owner can start it as a new idea with `idea-grill`.

## From proposal to change

- The owner approves or rejects each proposal in the chat. A rejected proposal leaves no record.
- For each approved proposal, the skill opens one pull request on the engine repo. The pull request description holds the seven parts. The owner merges it.

## "Worth testing" and "proven"

- A "worth testing" practice lives in its normal rule file, with one label line: `_Worth testing. Source: <link>_`.
- A rule without this label is proven.
- The owner decides when a practice is proven, at any time. If it helped, a pull request removes the label line. If it failed, a pull request removes the rule.

## Considered options

- **A copy of the skill in each engine repo.** Rejected: a fix must then go into each copy.
- **A new repo for the skill.** Rejected: one more repo with its own CI, licence and `AGENTS.md`, for one skill that serves no stage.
- **One run in the `studio` repo for all engines, with a new fixed path `~/www/<engine>/`.** Rejected: a third fixed path, and one run that changes several repos is harder to follow and to fix.
- **A local copy of the engine list and goals, at `~/www/studio/` or inside the skill.** Rejected: an old copy gives old answers.
- **Every proposal as a pull request at once, where merge means approve.** Rejected: the agent writes the change also for each rejected proposal, and a "rebuild" proposal can be big.
- **Every proposal as a GitHub issue.** Rejected: more steps and a list of waiting work to maintain.
- **"Worth testing" practices in a separate file that no skill reads.** Rejected: nothing uses them, so nothing proves them.
- **A practice becomes proven after a fixed number of projects.** Rejected: it needs a record of use per project.
- **A new idea folder for each "no engine" point.** Rejected: the skill then writes outside the current repo, and one source rarely justifies a whole engine.

## Consequences

- The `studio` repo holds one plugin besides its documents.
- The results check asks the owner about each "worth testing" rule (ADR 0006).
