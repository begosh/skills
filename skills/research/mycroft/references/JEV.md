# Mycroft JEV Gating & Pruning Protocol

JEV (Judgment, Evidence, Value) controls the focus and efficiency of the DAG, preventing runaway task sprawl and token waste.

---

## 1. The Mathematical Formula

```text
JEV = Criticality × (1 - 0.5 × Redundancy)
```

Where:
* **Criticality** $\in [0.0, 1.0]$: How essential is this finding to the core deliverable requested by the user?
  - `1.0`: Core objective or direct prerequisite.
  - `0.5`: Informative supporting context.
  - `0.1`: Tangential trivia or secondary background.
* **Redundancy** $\in [0.0, 1.0]$: How much does this task overlap with existing or higher-priority tasks?
  - `0.0`: Completely unique inquiry.
  - `0.5`: Moderate overlap with an adjacent specialist.
  - `1.0`: Duplicate or subsumed by another task.

---

## 2. Pruning Threshold

* **Standard Threshold**: `0.30`.
* Any prospective task with a final score strictly below `0.30` is **PRUNED** before dispatch.
* Pruned tasks are recorded in the run journal as `PRUNED_JEV` with their score and rationale.

---

## 3. The Protected & Exempt Invariant

Certain nodes are **JEV Protected** and exempt from comparative scoring. They can **NEVER** be pruned:

1. **Root Evidence Bindings**: Primary source extraction tasks explicitly named by the user.
2. **Explicit Disclaimers & Gaps**: Header disclaimers, conflict flags, and missing information declarations.
3. **The Critic Node**: The adversarial audit is mandatory.
4. **The Synthesizer**: The final assembly step is mandatory.

*Rule*: Even if an LLM heuristic claims a disclaimer is "redundant," protected status overrides the score. Truth and safety invariants cannot be pruned to save cost.
