# The Diogenes review

Read this reference before accepting consequential findings. The critic reports defects; the coordinator owns acceptance and final judgment.

## Audit

Read cited originals and apply every relevant check:

1. **Entailment and scope:** The passage supports the claim for the right entity, version, date and conditions. Derived claims include verified inputs and a labeled derivation.
2. **Independent support:** Trace accounts to their underlying sources. Agent agreement, valid JSON and matching hashes establish neither truth nor independent corroboration.
3. **Sequence and dependencies:** Preserve chronology, calculation inputs and causal prerequisites. A proposal, deployed change and observed result are distinct states.
4. **Missing conditions and conflicts:** Retain material unstated inputs, conflicting originals and unread scope.

Recalculate arithmetic through execution, checking verified inputs and tolerances. Two originals giving different figures for the same fact both appear in the dossier and answer, with their disposition (such as superseded, estimate or disputed) and the reason. Silently choosing one figure is a defect even when the choice is correct.

Give an independent critic the question, relevant dossiers and readable support after investigation returns. If independent review is unavailable, perform self-review and identify its scope and lack of independence.

## Verdict and repair

Return affected claims, concrete defects/consequences, source locators, admission conditions and focused remedies. Use [CriticVerdict](CONTRACTS.md#criticverdict) for a structured handoff. Finding no material defect within the inspected scope is a valid result.

Give each material finding an evidence-grounded verdict:

| Verdict | Requirement |
| --- | --- |
| `PASS` | No material defect within the inspected scope. |
| `ADMIT_WITH_CONDITIONS` | Support holds under explicit conditions retained in the finding and final answer. |
| `FAIL` | A concrete defect or unmet review requirement prevents admission. |

The coordinator admits supported claims, qualifies conditional claims and marks unrepaired unsupported conclusions `QUARANTINED`. Material conflicts and unmet requirements remain in the main answer even when a rejected claim is placed in an appendix. [EVIDENCE.md](EVIDENCE.md#records-and-continuation) defines defect records.

Repair a rejected enquiry with its specific defect and remaining allocation. Default to at most two targeted repair cycles after the initial attempt, stopping earlier when access or expected benefit makes another retry unproductive. Reuse accepted evidence and preserve acceptance criteria. Final assembly receives a source-support check; one targeted assembly repair is usually sufficient.

**Review complete:** Every material conclusion has an evidence-grounded disposition and retained conditions. An unresolved required finding leaves the case partial; an optional excluded claim need not prevent completion.
