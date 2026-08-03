# claude-skills

My own twist on Claude skills — a small collection of `SKILL.md` files I use with Claude Code to get more consistent results out of the tasks I repeat most: writing commits, analysing websites, and designing web interfaces.

Each skill is a self-contained folder with a single `SKILL.md`. No dependencies, no build step.

## What's inside

| Skill | What it does |
| --- | --- |
| [commit-message](commit-message/SKILL.md) | Reads `git diff HEAD` and writes a structured commit message — title, short context, bulleted changes including renames and deletions. |
| [web-analysis](web-analysis/SKILL.md) | Analyses a website or app from a link: design patterns, layout, colour scheme and typography, plus the practical details (purpose, features, contact info, locations, opening hours), condensed into a short summary. |
| [web-design](web-design/SKILL.md) | The big one. Builds and redesigns web interfaces with a deliberate visual point of view — how to derive a design direction from the subject instead of defaulting to it, a catalogue of what makes UI read as AI-generated (colour, type, layout, spacing, components, effects, motion, copy), an anti-default audit, and pass/fail verification gates for accessibility and interaction states. |

## Installing

Skills are picked up from `~/.claude/skills/` (available everywhere) or `.claude/skills/` inside a project (that project only).

```bash
git clone https://github.com/nestix6/claude-skills.git
cd claude-skills

# all of them, for every project
cp -r commit-message web-analysis web-design ~/.claude/skills/

# or just one, scoped to the project you're in
cp -r web-design /path/to/your/project/.claude/skills/
```

## Using them

Claude Code reads each skill's `description` and invokes it when the task matches — ask for a commit message and `commit-message` applies itself. You can also call one by name:

```
/web-design a landing page for a freight invoicing tool
```

## Contributing

Contributions and forks are welcome. Open a PR with a new skill or an improvement to an existing one — keep the frontmatter (`name`, `description`) intact, since the description is what decides when the skill fires.

## Issues

Found something broken, or a skill that misfires? Report it in [Issues](https://github.com/nestix6/claude-skills/issues).

## License

[MIT](LICENSE).
