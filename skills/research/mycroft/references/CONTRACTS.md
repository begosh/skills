# Task and evidence contracts

Use these contracts for delegated handoffs or machine-readable artifacts. Direct enquiries can keep equivalent prose. This reference defines what a useful handoff contains; [SCHEMAS.json](SCHEMAS.json) defines JSON structure for TaskBrief, WorkerResult and CriticVerdict.

**JSON validation:** Load the selected schema from SCHEMAS.json and validate the actual object before reporting schema validation. Then perform the semantic checks below and source [review](CRITIQUE.md).

## TaskBrief

Record outcome, constraints, source/entity/date scope, initial inputs, components, evidence needs, missing information and completion criterion. Extend inputs through authorized source discovery.

**Ready:** The criterion identifies a checkable answer, and missing prerequisites are explicit.

## TaskContract

Each commission carries one checkable objective and bounded scope:

- ID, operation (`clarify`, `retrieve`, `extract`, `calculate`, `compare`, `check`; or `split` for non-atomic composite parent nodes) and objective.
- Exact inputs (at most 2 items for atomic tasks), source/entity/date scope and allowed access/writes.
- Dependencies, expected return with a chosen ceiling of 100 to 150 words of structured facts, and a binary, falsifiable acceptance check.
- Work allocation, including any requested output bound.

Each atomic task has exactly one operation:

| Operation | Bounded work |
| --- | --- |
| `clarify` | Ask the user for one material missing prerequisite, only when it blocks progress. |
| `retrieve` | One focused query targeting at most 2 documents. |
| `extract` | One named field group, metric or exact span from one source. |
| `calculate` | One deterministic computation over supplied, verified inputs. |
| `compare` | Two concrete findings against one explicit criterion. |
| `check` | One asserted claim against one primary locator and span. |

Separate locating a source from extracting its fields, and extraction from calculation or judgment. Related tasks may share a runner under [HOST.md](HOST.md#commission-and-schedule).

One tool call may execute several ready tasks, but keep their IDs, inputs, results and acceptance checks separate. Computing a date's weekday and a fare total are separate calculations. Deciding which ticket is cheaper is a `compare` task that depends on the applicable prices and conditions. Preserve those boundaries in the saved task record as well as the visible slips.

A compound investigation uses `split` with bounded child commissions and dependencies. The parent owns consolidation and a branch allocation; a child with multiple operations needs further decomposition. Direct cases may describe this in prose without a separate DAG. Show each accepted atomic slip and its dependencies before dispatch. A senior shows its child slips before issuing them.

**Ready:** The commissioned runner can identify its inputs, permitted work, expected evidence, output cap, and acceptance criterion.

## WorkerResult

Return `task_id`, `status`, `answer`, `covered_scope`, `sources`, `claims`, `gaps` and `checks`. Optional next-enquiry and observed-usage fields support continuation.

Each source carries an ID, locator and read status. Each claim carries an ID, claim text, [evidential status](EVIDENCE.md#claims-and-captures) and nonempty support with source ID, precise locator and exact excerpt. Inferences include verified inputs and derivation; conditions belong with the affected claim.

Check source/claim ID uniqueness and support resolution. Supporting sources must have been read sufficiently, and excerpts/locators must match that captured version. Complete factual conclusions need supported claims. Empty findings are valid for failed/blocked/partial execution when the unmet scope is explicit.

**Return ready:** Every consequential conclusion has inspectable support or a named gap, and coverage, status, checks and usage describe performed work.

## CriticVerdict

Return verdict, review mode/scope, concrete issues/remedies, admission conditions and quarantined claim IDs/reasons.

[CRITIQUE.md](CRITIQUE.md#verdict-and-repair) defines dispositions and repair policy. The record must preserve the corresponding issues, conditions and quarantined claims.

**Verdict ready:** Every material defect identifies its affected finding and consequence; accepted conditions can be carried into synthesis.

## Publication and event records

Follow the requested project format. A structured dossier contains brief, accepted/qualified claims, sources, gaps, execution status, checks and artifact locators.

An event records sequence, phase, actor/enquiry, action, concise grounds, actual status and relevant locators; timestamps come from observation. [EVIDENCE.md](EVIDENCE.md#records-and-continuation) owns logging, saved-artifact checks and continuation.
