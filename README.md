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
| **[mycroft](skills/research/mycroft/SKILL.md)** | `research` | Cerebral, evidence-led research orchestrator driven by native subagents. Uses Triad decomposition, DSPy typed contracts, JEV pruning, adversarial critique, and GEPA learning. |

---

## Highlight: Mycroft — The Omniscient Orchestrator

Mycroft Holmes sits in the armchair of the Diogenes Club and views the entire system. He does not run around doing hasty legwork; he orchestrates investigations through specialist subagents ("Sherlocks"), enforces rigorous evidence discipline, challenges all claims adversarially, and synthesizes hardened, authoritative dossiers.

### Core Architecture

1. **Autonomous Momentum**: Only pauses if fundamentally uncertain about the user's intent. Otherwise advances autonomously from problem framing through specialist dispatch, critique, and synthesis to publication.
2. **Triad Decomposition**: Eliminates anchoring bias on complex problems by dispatching three parallel viewpoints:
   - *The Mechanist*: Ground truth, implementation constraints, mechanics.
   - *The Adversary*: Failure modes, stress tests, edge cases, vulnerabilities.
   - *The Pragmatist*: Pareto trade-offs, real-world utility, operational simplicity.
3. **DSPy Typed Contracts**: Specialists report strictly structured leaf contracts (`findings`, `sources`, line-level `claims`, explicit `gaps`). Uncorroborated consensus is rejected; claims require primary source locators and exact excerpts.
4. **JEV Decision Gating**: Joint Expected Value gating ($JEV = Criticality \times (1 - 0.5 \times Redundancy)$) prunes tasks below `0.30` while strictly preserving disclaimers and unstated condition gaps.
5. **The Diogenes Review & Bounded Repair**: An independent Critic subagent executes a 4-point adversarial audit, allowing up to 2 bounded repair cycles before quarantining unverified claims.
6. **Durable Publication**: Emits immutable records under `.mycroft/runs/<timestamp>/` (`report.md`, `report.json`, `operations.jsonl`) and reflects critique defects as Failure Packets for offline GEPA Pareto optimization.

---

## Contributing

To add a new skill to this repository:
1. Create a directory under `skills/<category>/<skill-name>/`.
2. Include a `SKILL.md` with standard YAML frontmatter and an `agents/openai.yaml` definition.
3. Update the category `README.md`, top-level `README.md`, and `.claude-plugin/plugin.json`.
