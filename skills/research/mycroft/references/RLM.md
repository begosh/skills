# RLM — external-context inspection and bounded branching

Read this reference when the evidence is too large for one context window: a corpus of documents, a deep directory tree, an archive, a ledger with hundreds of entries. It owns two things the body only summarises — the **external-context inspection loop** and the **normative branching limits**.

The file is prose, like the rest of the package. Where the host can spawn children, branching uses them; where it cannot, the same loop runs on centrally scheduled leaf calls and is recorded as algorithmic recursion ([HOST.md](HOST.md)).

## When the loop applies

| Signal | Neutral response |
| --- | --- |
| Corpus exceeds one readable context | Index it, then inspect slices rather than reading it whole |
| Search space is wide and sparse (one decisive fact in thousands of rows) | Partition into disjoint slices; stop the branch on the first decisive hit |
| Answer requires counting or comparing across many items | Aggregate by deterministic script, not by reading each item into the context |
| Host offers native recursion | Use it, within the depth and fan-out limits below |
| Host offers no recursion | Emulate: the coordinator schedules leaf calls and consolidates them |

If a single authoritative source answers the question, none of this applies — that is a Direct case in the body's case-sizing table.

## The inspection loop

1. **Index.** Record what the corpus is, how it is partitioned, and what a slice boundary is (file, page, row range, table). Store the index in the case record so later slices are addressable.
2. **Slice disjointly.** Slices must not overlap; overlap buys duplicated evidence and double-counted claims. Declare the slice rule before inspecting ("wharves 1–10", "lines 1–500").
3. **Inspect one slice per call.** Each call returns only the atomic extraction its contract asks for — a named field, a metric, an exact span — with locator and excerpt. Not a summary of the slice.
4. **Short-circuit on the needle.** The moment a slice yields the decisive fact or a falsifying counterexample, stop commissioning siblings and report the branch closed. Pending calls are cancelled where the host supports it, and the cancellation is recorded.
5. **Aggregate deterministically.** Counts, sums and comparisons run as code over the returned records. A model that "adds up" forty excerpts is producing an estimate, not a total.
6. **Consolidate upward.** Sub-workers report only to their branch parent, which deduplicates, resolves minor conflicts, notes uncovered scope, and returns one clean result. Nothing at depth 2 talks to the coordinator directly.
7. **Verify coverage.** State which slices were inspected, which failed, and which were never reached. Partial coverage is a result; silent truncation is a defect.

## Branching limits (normative)

| Invariant | Rule | On breach |
| --- | --- | --- |
| **Depth ceiling** | Coordinator is depth 0, commissioned runners depth 1, their sub-workers depth 2. Default maximum is 2; hard cap 3. Depth-2 workers are leaves. | A depth-2 worker that wants to branch returns a coverage gap instead |
| **Fan-out budget** | 3–6 sub-workers per branch, never an unbounded swarm | Partition into successive batches rather than one wide wave |
| **Early needle hit** | Stop the branch on decisive proof or a falsifying counterexample | Cancel or early-exit pending siblings; record what was not inspected |
| **Upward consolidation** | Sub-workers report only to their branch parent | Reject any return addressed to the coordinator from depth 2 |

Fan-out multiplies: an unconstrained tree costs $O(\text{fan-out}^{\text{depth}})$ calls. State the planned call budget before dispatching, and stop when it is spent.

There is no separate "Wiggins" tier. A runner that delegates *is* the branch coordinator for its branch; naming it does not add a depth level, and saying so prevents the four invariants from being read as five roles.

## Semantic subcalls

Where a slice needs judgement rather than extraction — "does this clause permit early termination?" — the call is a **semantic subcall**: it reads selected passages and answers one bounded question with a verdict and its supporting span. A semantic subcall is not a summariser; it returns a decision plus evidence, and its verdict is a claim subject to [review](CRITIQUE.md).

Where the host forbids grandchildren, a runner returns a semantic request to the coordinator, which schedules the permitted leaf call and returns the evidence. The recursion is then algorithmic — same loop, different scheduler — and must be described that way rather than as native delegation.

## Records

Keep the slice index, the dispatch/return status per enquiry, the early-termination point, aggregate calculations, uncovered slices and the observed call count. A branch that was planned but not executed is an unmet requirement, not a completed inspection.

**Inspection complete:** every declared slice has an inspected, failed or uncovered status; aggregates are computed from records; and the consolidated return states its coverage.
