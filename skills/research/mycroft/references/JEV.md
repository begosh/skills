# JEV — Planning value

Use the Joint Expected Value heuristic for overlapping or low-value optional enquiries.

## Protect, score and choose

Preserve required evidence, its prerequisites, necessary review/synthesis, material conflicts and missing-condition disclosures before scoring. Protect the dependency closure. Unavailable required evidence stays an explicit gap.

```text
JEV = criticality × (1 - 0.5 × redundancy)
```

Both inputs are estimates in [0, 1]. Criticality measures decision importance; redundancy measures overlap with accepted evidence or planned enquiries. The skill's configurable 0.30 threshold is a planning default, not an empirically validated constant or factual-confidence measure.

Optional branches below the threshold may be omitted after checking dependencies and answer coverage. For example, criticality 0.4 and redundancy 0.8 produce 0.24. The coordinator owns the decision.

**Pruning complete:** Required dependencies remain covered, and omitted work cannot change a required conclusion without appearing as a gap.

## Record

When used, record task IDs, estimates, calculated scores, protected status, retained/omitted decisions and concise grounds in the [case record](EVIDENCE.md#records-and-continuation).
