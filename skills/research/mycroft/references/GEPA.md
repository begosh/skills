# Reflective Instruction Evolution (GEPA)

Mycroft learns from investigation failures using a native adaptation of Generative Evolutionary Pareto Algorithms (GEPA).

---

## 1. Failure Packet Ingestion

Whenever a specialist attempt fails the Critic's audit or requires an Execution Repair, a **Failure Packet** is logged to `.mycroft/failure_store/`:

```json
{
  "packet_id": "fail_20261027_001",
  "task_id": "task.prep.mixing",
  "role": "Process Specialist",
  "input_context": "L03 Dissolve yeast in the water...",
  "rejected_output": "Dissolve in lukewarm water...",
  "critic_defect": "Inferred 'lukewarm' when source states temperature is unstated.",
  "timestamp": "2026-10-27T00:20:00Z"
}
```

---

## 2. Reflective Mutation

In an offline optimization pass (or via `$mycroft-optimize`), an Evolver agent inspects the failure packet:
1. **Root Cause Analysis**: Why did the instruction induce the model to fail?
2. **Targeted Mutation**: Proposes one focused rule addition or rephrasing (e.g. adding *"Temperature Invariant: If temperature is not explicitly stated, do not infer"*).
3. **Editable Slots Only**: Changes only role guidance; never mutates safety contracts, schemas, or budget caps.

---

## 3. Pareto Frontier Evaluation

The candidate prompt is evaluated against a frozen test corpus across three metrics:
1. **Accuracy**: Defect resolution rate on failed test cases.
2. **Regression Rate**: Must cause **0 regressions** on existing passing test cases.
3. **Token Efficiency**: Must not inflate prompt length unnecessarily (< 10% delta).

A candidate is admitted to `.mycroft/learning-candidates.jsonl` **only if it Pareto-dominates the baseline** (strictly better on at least one metric, no worse on any).
