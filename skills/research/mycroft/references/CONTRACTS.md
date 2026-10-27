# Mycroft Contracts & Typed Signatures

All communication between Mycroft and his specialist subagents is strictly typed. Chatty conversational preambles are prohibited; subagents exchange structured, schema-validated JSON payloads.

---

## 1. TaskBrief Signature (Phase 1 Output)

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "TaskBrief",
  "type": "object",
  "required": ["outcome", "constraints", "components", "evidence_needs", "missing_information"],
  "properties": {
    "outcome": { "type": "string", "maxLength": 500 },
    "constraints": {
      "type": "array",
      "items": { "type": "string", "maxLength": 300 }
    },
    "components": {
      "type": "array",
      "items": { "type": "string", "maxLength": 300 }
    },
    "evidence_needs": {
      "type": "array",
      "items": { "type": "string", "maxLength": 300 }
    },
    "missing_information": {
      "type": "array",
      "items": { "type": "string", "maxLength": 300 }
    }
  }
}
```

---

## 2. Leaf TaskContract Signature (DAG Node)

Each leaf task dispatched to a subagent has exactly one operation and bounded scope:

* **Supported Operations**:
  - `extract`: Bounded field extraction from supplied text.
  - `retrieve`: Focused document/code lookup (max 1 target).
  - `calculate`: Deterministic numeric formula over verified inputs.
  - `compare`: Explicit multi-faceted comparison between 2 findings.
  - `check`: Binary predicate test against primary evidence (`PASS`, `FAIL`, `REVIEW`).

```json
{
  "id": "task.prep.mixing",
  "operation": "extract",
  "objective": "Extract exact mixing and kneading durations, actions, and unstated temperatures from L03-L04.",
  "inputs": ["fixture:pizza_extraction_source"],
  "target_lines": ["L03", "L04"],
  "expected_output": "Chronological mixing and kneading actions with explicit gaps for unstated temperatures.",
  "acceptance_check": "Preserves L03-L04 order; captures 2m mix and 8m knead; marks temperatures as unstated; invents no extra details.",
  "max_words": 100
}
```

---

## 3. WorkerResult Signature (Specialist Output)

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "WorkerResult",
  "type": "object",
  "required": ["task_id", "answer", "claims", "gaps"],
  "properties": {
    "task_id": { "type": "string" },
    "answer": { "type": "string", "maxLength": 1000 },
    "sources": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["id", "locator"],
        "properties": {
          "id": { "type": "string" },
          "locator": { "type": "string" },
          "retrieval_type": { "type": "string" }
        }
      }
    },
    "claims": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["claim_text", "source_id", "line_citations"],
        "properties": {
          "claim_text": { "type": "string" },
          "source_id": { "type": "string" },
          "line_citations": { "type": "array", "items": { "type": "string" } },
          "exact_quote": { "type": "string" }
        }
      }
    },
    "gaps": {
      "type": "array",
      "items": { "type": "string" }
    }
  }
}
```

---

## 4. CriticVerdict Signature (The Diogenes Gate)

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "CriticVerdict",
  "type": "object",
  "required": ["verdict", "issues", "quarantined_claims"],
  "properties": {
    "verdict": { "type": "string", "enum": ["PASS", "FAIL", "ADMIT_WITH_CONDITIONS"] },
    "issues": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["target_task", "severity", "defect", "remedy"],
        "properties": {
          "target_task": { "type": "string" },
          "severity": { "type": "string", "enum": ["MATERIAL", "MINOR"] },
          "defect": { "type": "string" },
          "remedy": { "type": "string" }
        }
      }
    },
    "quarantined_claims": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["claim_text", "reason"],
        "properties": {
          "claim_text": { "type": "string" },
          "reason": { "type": "string" }
        }
      }
    }
  }
}
```
