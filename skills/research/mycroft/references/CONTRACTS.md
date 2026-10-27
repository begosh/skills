# Task and evidence contracts

Use these contracts for delegated handoffs or machine-readable artifacts. Direct enquiries can keep equivalent prose. This reference defines what a useful handoff contains; [SCHEMAS.json](SCHEMAS.json) defines JSON structure for TaskBrief, WorkerResult and CriticVerdict.

**JSON validation:** Load the selected schema from SCHEMAS.json and validate the actual object before reporting schema validation. Then perform the semantic checks below and source [review](CRITIQUE.md).

## TaskBrief

Record outcome, constraints, source/entity/date scope, initial inputs, components, evidence needs, missing information and completion criterion. Extend inputs through authorized source discovery.

**Ready:** The criterion identifies a checkable answer, and missing prerequisites are explicit.

## TaskContract

Each commission carries one checkable objective and bounded scope:

- ID, operation (`clarify`, `retrieve`, `extract`, `calculate`, `compare`, `check`; or `split` for non-atomic composite parent nodes) and objective.
- Exact inputs (strictly bounded: maximum 1–2 items for atomic leaves), source/entity/date scope and allowed access/writes.
- Dependencies, expected return (strictly bounded: maximum 100–150 words of structured facts/numbers) and checkable acceptance check.
- Work allocation, including any requested output bound.

Atomic leaf operations are strictly `clarify`, `retrieve`, `extract`, `calculate`, `compare`, and `check`. Composite operations must use `split` and be recursively decompiled further. Broad enquiries are never admitted as atomic tasks. [HOST.md](HOST.md) owns allocation and scheduling policy.

**Ready:** The commissioned runner can identify its inputs, permitted work, expected evidence, output cap, and acceptance criterion.

## WorkerResult

Return `task_id`, `status`, `answer`, `covered_scope`, `sources`, `claims`, `gaps` and `checks`. Optional next-enquiry and observed-usage fields support continuation.

Each source carries an ID, locator and read status. Each claim carries an ID, claim text, [evidential status](EVIDENCE.md#claims-and-captures) and nonempty support with source ID, precise locator and exact excerpt. Inferences include verified inputs and derivation; conditions belong with the affected claim.

Check source/claim ID uniqueness and support resolution. Supporting sources must have been read sufficiently, and excerpts/locators must match that captured version. Complete factual conclusions need supported claims. Empty findings are valid for failed/blocked/partial execution when the unmet scope is explicit.

**Return ready:** Every consequential conclusion has inspectable support or a named gap, and coverage, status, checks and usage describe performed work.

## CriticVerdict

Return verdict, review mode/scope, concrete issues/remedies, admission conditions and quarantined claim IDs/reasons.

`PASS` applies to inspected scope. `ADMIT_WITH_CONDITIONS` requires actual retained conditions. `FAIL` requires concrete defects or unmet review requirements. [CRITIQUE.md](CRITIQUE.md) owns dispositions and repair policy.

**Verdict ready:** Every material defect identifies its affected finding and consequence; accepted conditions can be carried into synthesis.

## Publication and event records

Follow the requested project format. A structured dossier contains brief, accepted/qualified claims, sources, gaps, execution status, checks and artifact locators.

An event records sequence, phase, actor/enquiry, action, concise grounds, actual status and relevant locators; timestamps come from observation. [EVIDENCE.md](EVIDENCE.md#records-and-continuation) owns logging, saved-artifact checks and continuation.
