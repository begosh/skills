# Repository Guidelines

Skills in this repository are organized into categorized bucket directories under `skills/`:

- `research/`: Autonomous research, evidence validation, and orchestration skills
- `engineering/`: Architecture, code analysis, and development workflows
- `productivity/`: General task optimization and reasoning tools

Every promoted skill must have:
1. A `SKILL.md` file with standard YAML frontmatter (`name`, `description`).
2. An `agents/openai.yaml` declaring agent interface metadata (`display_name`, `short_description`).
3. An entry in the root `README.md` catalog linking directly to its `SKILL.md`.
4. An entry in `.claude-plugin/plugin.json` for Claude Code plugin compatibility.

## Organization Rules

- Keep each skill self-contained: place task contracts, critique rubrics, and references in a local `references/` subdirectory within the skill folder.
- No uncorroborated assertions or vague instructions in `SKILL.md`; describe concrete contracts, execution stages, and expected outputs.
