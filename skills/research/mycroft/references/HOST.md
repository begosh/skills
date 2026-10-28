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

When delegation is available and permitted, investigative work goes to the Baker Street runners even if no independent critic is available. The coordinator may self-review their cited originals and the synthesis from his chair; absence of a critic does not transfer exploratory legwork to him.

Only when delegation is unavailable, disallowed, or fails does the coordinator investigate directly, stating that limitation. Report the review mode actually used and its scope (for example, "delegated investigation; coordinator self-review; no independent critic"), because self-review can find arithmetic slips and missing locators but cannot detect the reviewer's own framing error. Never present self-review as independent corroboration or describe workers that were not commissioned.

## Commission and schedule

Give each enquiry one objective, exact evidence scope/inputs, allowed access/writes, dependencies, acceptance criterion, expected return and work allocation. Use [CONTRACTS.md](CONTRACTS.md) for structured handoffs.

Mycroft owns the initial question decomposition and its required outputs. Planning perspectives advise that decision; they are not evidence runners. Close any delegated planning critique when its plan is accepted, then commission fresh investigative contexts with concrete mission names. Reuse an investigator for related work inside its evidence branch, rather than cycling planning personas through unrelated searches.

Send the minimum useful context and share versioned evidence to avoid repeated retrieval. Commission independent ready work within observed slots, batch wider plans and wait for prerequisite returns. Preserve disagreements for evidence review.

For a composite branch, use an explicit `split` commission: the senior runner owns named atomic child contracts, bounded source territory, consolidation and a branch-wide allocation. Prefer native child dispatch when permitted. Reserve capacity for children before starting parent runners; queue other parents rather than filling every slot with seniors who cannot dispatch. When a host forbids native children, the parent returns its concrete child slips for central scheduling. Name that fallback and retain the parent as the consolidation owner.

**Wiggins is the dispatch role, not an automatic extra agent level.** In the narrative Mycroft hands him the slips, he calls the senior runner, and that runner whistles for sub-runners when actual branching occurs. Count depth by real execution contexts: Mycroft/dispatch at depth 0, senior runner at 1, its children at 2. Tell the user which children were actually sent, queued or cancelled, and show returns going back through their parent. Use [LONDON.md](LONDON.md) for the visible scenes.

Apply this scheduling in every tier. Direct cases use equivalent prose contracts and one runner per investigative leaf; independent ready leaves share the available concurrency. A small case reduces recordkeeping, not working delegation. Mycroft owns framing, commissions, source audit, synthesis, and canonical writes; the runners own exploration. Ground in-character dispatches and returns in actual tool activity.

Allocate one case allowance across investigation, semantic calls, retries, review and synthesis. Child work and repairs consume their existing allocation. Track cumulative case and branch work: renaming a leaf or changing a source does not reset that allowance. Prioritize the user's decisive missing answer before expanding subsidiary comparisons. Close a branch on sufficient evidence or its stopping condition, and report blocked core evidence promptly. Distinguish requested limits, measured consumption and runtime-enforced caps; leave unknown usage explicit.

**Commission complete:** Every ready enquiry has an owner, acceptance check, inputs and allocation; pending dependencies remain pending.

## Native depth and semantic calls

Native worker slots, parallel calls, recursion depth and total work are separate controls. Under a flat-team policy, an investigator sends a bounded semantic request to the coordinator, who dispatches the permitted leaf call and returns its evidence.

An ordinary semantic child reads selected passages; a recursive RLM child performs another external-context loop. Algorithmic recursion can therefore use centrally scheduled calls without native grandchildren.

## Missing capability and cancellation

| Missing facility | Available course |
| --- | --- |
| Native delegation unavailable, disallowed, or failed | Disclose the limitation, investigate sequentially, and state the actual review mode. |
| Independent critic only | Retain delegated investigation; self-review cited sources and synthesis, disclosing that review scope. |
| A source route | Try a relevant permitted alternative and retain uncovered scope. |
| RLM execution/state/semantic-call route | Use ordinary corpus research and name the actual method. |
| GEPA cases, scorer or execution | Follow the refinement fallback in [GEPA.md](GEPA.md#freeze-and-qualify). |

On cancellation, stop commissioning and request termination where supported. Report termination only when confirmed. Unavailable required work stays an unmet requirement in the final result.

Use existing execution facilities for ordinary cases. Introduce runtime infrastructure only when separately justified and authorized.
