# Skills

[![skills.sh](https://skills.sh/b/begosh/skills)](https://skills.sh/begosh/skills)

Agent skills for autonomous research, deep architecture, and evidence synthesis.

These skills are designed to be composable, evidence-first, and robust across modern AI coding agents (Claude Code, Google Antigravity, OpenAI Codex, and Cursor).

---

## Installation

### 1. Universal Installation via [skills.sh](https://skills.sh/begosh/skills)

Installs editable skill markdown and contract files directly into your active project workspace:

```bash
# Add all skills from this repository
npx skills@latest add begosh/skills

# Or add a specific skill
npx skills@latest add begosh/skills --skill mycroft
```

### 2. Claude Code Plugin

Install as a managed, auto-updating plugin:

```bash
claude plugin install begosh-skills
```

### 3. Google Antigravity / Gemini CLI / Codex

Copy or link the skill into your local skills directory:

```bash
# Antigravity / Gemini global skills:
# Copy skills/research/mycroft into ~/.gemini/antigravity-cli/skills/mycroft

# Project-level Agent Skills standard:
# Copy skills/research/mycroft into .agents/skills/mycroft
```

---

## Skills Catalog

| Skill | Category | Description |
| :--- | :--- | :--- |
| **[mycroft](skills/research/mycroft/SKILL.md)** | `research` | Evidence-led research with source discovery, bounded specialists, Triad decomposition and review; optional RLM and measured GEPA. |

---

## Highlight: Mycroft — The mind at the club

Mycroft coordinates source discovery, bounded specialist enquiries, evidence review and synthesis. The skill is Markdown; the active host supplies agents, tools, execution and storage.

### Core workflow

1. **Frame and discover**: Define the decision, completion criterion and evidence horizon. Read supplied sources and find additional relevant originals within the requested scope.
2. **Choose useful enquiries**: Investigate directly, commission a critic, or use Mechanist, Adversary and Pragmatist viewpoints for competing decompositions. Schedule through the host's actual tools, available slots and shared case allowance.
3. **Return source-linked findings**: Portable task/result contracts preserve excerpts, exact locators, evidence status, contradictions and gaps. Structured validation and source entailment are separate checks.
4. **Review and repair**: Challenge consequential claims, retain admission conditions and use bounded targeted repair. Disclose self-review or unresolved required evidence.
5. **Use advanced modes when justified**: Optional JEV guides planning value; RLM performs external-context inspection, semantic subcalls and aggregation; explicitly requested GEPA executes measured instruction comparisons and candidate selection.
6. **Deliver observable results**: Save project-appropriate reports and case records, verify artifacts and report actual coverage, checks and remaining uncertainty. Saved files support continuation; execution guarantees come from the host.

---

## Contributing

To add a new skill to this repository:
1. Create a directory under `skills/<category>/<skill-name>/`.
2. Include a `SKILL.md` with standard YAML frontmatter and an `agents/openai.yaml` definition.
3. Update the category `README.md`, top-level `README.md`, and `.claude-plugin/plugin.json`.
