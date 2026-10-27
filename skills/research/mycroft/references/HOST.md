# Host capabilities and work limits

Read this reference for delegation, execution allowances or missing host facilities. The coordinator owns acceptance and canonical writes; an investigator may own a separately assigned artifact.

## Bind capabilities

Inspect the actual source routes, delegation tool, worker slots, agent-role restrictions, execution/retained-state support and writable location needed for the case. Check runner access separately when it matters. Use current tool metadata and project instructions; configured access is not evidence of a successful connection.

A behavioral read-only assignment is not an enforced filesystem/network sandbox. Bind code and source access to the host's actual permission boundary.

## Capability binding

Four capabilities decide the shape of a case. Establish each from the host's live tool metadata and project instructions before commissioning; treat the right-hand column as illustrative only, and verify rather than assume.

| Capability | Question to answer | Typical mechanisms (verify per host) |
| --- | --- | --- |
| Delegation | Can this host spawn a scoped child with its own context? | A subagent/Task-style tool, a delegation call, a worker pool, an external runner process, or none |
| Concurrency | How many children run at once, and is there a native depth limit? | Parallel-call slots, native recursion, or a flat team where recursion must be emulated by scheduled calls |
| Execution | Can a child run code and read retained state? | A shell/code tool with persistent or ephemeral state, or no execution at all |
| Storage | Where may outputs be written? | Project-relative artifact directory, a session run directory, or read-only |

Name the binding in the case record: "delegation via X; concurrency N; execution Y; writes to Z". An unverified route is not a capability — test it on the first commission and fall back explicitly if it fails.

## Self-review disclosure

Where delegation is unavailable, or the only reviewer would be the investigator itself, the coordinator performs the work directly and says so. Report the review mode and its scope ("self-reviewed; no independent critic was available"), because a self-review can find arithmetic slips and missing locators but cannot detect the investigator's own framing error. Never present a self-review as independent corroboration.

## Commission and schedule

Give each enquiry one objective, exact evidence scope/inputs, allowed access/writes, dependencies, acceptance criterion, expected return and work allocation. Use [CONTRACTS.md](CONTRACTS.md) for structured handoffs.

Send the minimum useful context and share versioned evidence to avoid repeated retrieval. Commission independent ready work within observed slots, batch wider plans and wait for prerequisite returns. Reuse investigators for related follow-ups when useful. Preserve disagreements for evidence review.

Allocate one case allowance across investigation, semantic calls, retries, review and synthesis. Child work and repairs consume their existing allocation. Distinguish requested limits, measured consumption and runtime-enforced caps; leave unknown usage explicit.

**Commission complete:** Every ready enquiry has an owner, acceptance check, inputs and allocation; pending dependencies remain pending.

## Native depth and semantic calls

Native worker slots, parallel calls, recursion depth and total work are separate controls. Under a flat-team policy, an investigator sends a bounded semantic request to the coordinator, who dispatches the permitted leaf call and returns its evidence.

An ordinary semantic child reads selected passages; a recursive RLM child performs another external-context loop. Algorithmic recursion can therefore use centrally scheduled calls without native grandchildren.

## Missing capability and cancellation

| Missing facility | Available course |
| --- | --- |
| Native delegation/review | Investigate sequentially and identify self-review. |
| A source route | Try a relevant permitted alternative and retain uncovered scope. |
| RLM execution/state/semantic-call route | Use ordinary corpus research and name the actual method. |
| GEPA cases, scorer or execution | Follow the refinement fallback in [GEPA.md](GEPA.md#freeze-and-qualify). |

On cancellation, stop commissioning and request termination where supported. Report termination only when confirmed. Unavailable required work stays an unmet requirement in the final result.

Use existing execution facilities for ordinary cases. Introduce runtime infrastructure only when separately justified and authorized.
