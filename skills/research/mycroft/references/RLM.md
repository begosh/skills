# RLM — recursive evidence branches and external-context inspection

Read this reference before dispatching a composite evidence branch or inspecting evidence too large for one context window. Mycroft first decomposes the enquiry into concrete evidence branches. A senior runner may then split its assigned branch into atomic child questions or disjoint corpus slices. This reference owns that recursive delegation pattern, the **external-context inspection loop**, and the **normative branching limits**; it does not assert that a separate RLM runtime or model training was executed.

The file is prose, like the rest of the package. Where the host can spawn children, branching uses them; where it cannot, the same loop runs on centrally scheduled leaf calls and is recorded as algorithmic recursion ([HOST.md](HOST.md)).

## When the loop applies

| Signal | Neutral response |
| --- | --- |
| A scoped evidence branch contains independent child questions whose consolidation belongs together | Senior runner creates explicit atomic child contracts within its branch allocation |
| Corpus exceeds one readable context | Index it, then inspect slices rather than reading it whole |
| Search space is wide and sparse (one decisive fact in thousands of rows) | Partition into disjoint slices; stop the branch on the first decisive hit |
| Answer requires counting or comparing across many items | Aggregate by deterministic script, not by reading each item into the context |
| Host offers native recursion | Use it, within the depth and fan-out limits below |
| Host offers no recursion | Coordinator schedules permitted leaf calls; the senior runner consolidates its branch |

If a few direct leaves answer the question without useful parent consolidation, dispatch those leaves directly. Use a senior branch when it reduces root context or coordinates a genuinely composite enquiry; do not manufacture a large archive or sub-workers for a theatrical scene.

## Branch handoff and visible fan-out

Mycroft supplies the branch objective, source territory, required answer and stopping condition. The senior runner records `operation: split`, names its child leaves and verifies they are independently bounded before dispatch. A child performs one primitive; the senior consolidates evidence and gaps upward. Mycroft retains ownership of the overall question and any change in scope.

In the story Wiggins calls the senior runner, who whistles for named sub-runners and assigns their questions or slices. Announce the planned split before dispatch, then identify the children actually commissioned and those still queued. Native branching uses real child calls whenever host permissions and reserved capacity allow; central scheduling is a disclosed fallback. [HOST.md](HOST.md) owns slot allocation and [LONDON.md](LONDON.md) supplies examples.

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
| **Depth ceiling** | Coordinator is depth 0, commissioned runners depth 1, their sub-workers depth 2. Default maximum is 2; hard cap 3 only when the case plan explicitly declares it and the host permits it. Workers at the declared ceiling are leaves. | A worker at the declared ceiling returns a coverage gap; no worker raises its own limit |
| **Fan-out budget** | 3–6 sub-workers per branch, never an unbounded swarm | Partition into successive batches rather than one wide wave |
| **Early needle hit** | Stop the branch on decisive proof or a falsifying counterexample | Cancel or early-exit pending siblings; record what was not inspected |
| **Upward consolidation** | Sub-workers report only to their branch parent | Reject any return addressed to the coordinator from depth 2 |

Fan-out multiplies: an unconstrained tree costs $O(\text{fan-out}^{\text{depth}})$ calls. State the planned call budget before dispatching, and stop when it is spent.

There is no separate technical "Wiggins" tier. He voices the dispatch function at Mycroft's level. A runner that delegates is the branch coordinator for its branch; the scene does not add another execution context or depth level.

## Semantic subcalls

Where a slice needs judgement rather than extraction — "does this clause permit early termination?" — the call is a **semantic subcall**: it reads selected passages and answers one bounded question with a verdict and its supporting span. A semantic subcall is not a summariser; it returns a decision plus evidence, and its verdict is a claim subject to [review](CRITIQUE.md).

Where the host forbids grandchildren, a runner returns a semantic request to the coordinator, which schedules the permitted leaf call and returns the evidence. The recursion is then algorithmic — same loop, different scheduler — and must be described that way rather than as native delegation.

## Records

Keep the child-question plan or slice index, dispatch/return status per enquiry, early-termination point, aggregate calculations, uncovered scope and observed cumulative call count. Descendants and repairs share the branch and case allowance; a new task ID is not a new allowance. A branch that was planned but not executed is an unmet requirement, not a completed inspection. Record actual parent/child relationships so the narrative fan-out can be checked against tool activity.

**Inspection complete:** every declared slice has an inspected, failed or uncovered status; aggregates are computed from records; and the consolidated return states its coverage.
