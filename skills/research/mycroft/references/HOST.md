# Host capabilities and work limits

Read before commissioning. Use current tool metadata and project instructions to establish capabilities; verify configured routes through actual work.

## Bind capabilities

Record the facilities needed for this case:

| Capability | Establish |
| --- | --- |
| Delegation | Permitted mechanism for a scoped worker with its own context, or its absence. Verify the route on the first commission. |
| Concurrency and depth | Available worker slots, agent-role restrictions and whether workers may commission children. |
| Execution | Facilities for calculations and checks, retained state and runner access where relevant. |
| Storage | Permitted writable location, or a read-only limitation. See [storage and execution](#storage-and-execution). |
| Source access | Available source routes and material access gaps. |

A behavioral read-only assignment does not enforce a filesystem or network sandbox. Use the host's actual permission boundaries.

Binding is complete when each required facility has an observed route or an explicit limitation.

## Investigation and review roles

In every tier, evidence runners perform exploration when delegation works and is permitted. The coordinator owns framing, decomposition, cited-original audit, acceptance, synthesis and canonical writes. A runner may write a separately assigned artifact.

Only unavailable, disallowed or failed delegation permits coordinator investigation. Disclose that fallback. An absent independent critic permits coordinator self-review, but does not transfer exploration to the coordinator.

State the actual review mode and scope, such as "delegated investigation; coordinator self-review; no independent critic". Self-review is not independent corroboration and may retain the investigator's framing errors. Describe only workers actually commissioned.

## Commission and schedule

Use [CONTRACTS.md](CONTRACTS.md) for commission content. Send the minimum useful context and share versioned evidence to avoid repeated retrieval.

Close planning critics when Mycroft accepts the plan. Start evidence work in fresh runner contexts with concrete missions; reuse an evidence runner for related slips within its branch. Each slip remains atomic. One runner can handle several dependent slips, so Direct cases need no extra worker for each operation.

Dispatch independent ready tasks within available slots; queue wider plans and wait for prerequisites. Preserve branch ownership when reusing workers.

For a useful composite branch, apply [RLM.md](RLM.md). Reserve child capacity before starting parent runners; queue other parents rather than filling all slots with seniors waiting to dispatch. Prefer native child dispatch when permitted and supported. Otherwise, the senior returns child slips for central scheduling and retains consolidation ownership. Disclose that fallback. [LONDON.md](LONDON.md) defines its narrative.

Allocate one allowance across planning, investigation, semantic calls, review, repairs and synthesis. Descendants consume their branch allocation. Renaming a task or changing a source does not reset either allowance. Prioritize the decisive missing answer before subsidiary comparisons.

Stop a branch when its acceptance check is satisfied, its stopping condition applies or its allowance is spent. Report blocked core evidence and uncovered scope. Distinguish requested limits, observed consumption and runtime-enforced caps; leave unknown usage explicit.

Scheduling is complete when every ready task has an owner, inputs, acceptance check and allocation, and dependent tasks remain pending.

## Storage and execution

Choose one permitted output directory at the work root: `./artifacts/` or `.mycroft/runs/<timestamp>/`, unless project conventions specify another. Keep outputs outside the corpus being inspected. Write human-readable and machine-readable dossiers there; [EVIDENCE.md](EVIDENCE.md#records-and-continuation) defines their content.

If storage is read-only, deliver the supported answer in chat, state that artifacts could not be saved and claim no artifact path. Re-read files before reporting them as saved.

Run deterministic calculations and checks through the host's execution facility. Without execution, mark those tasks unexecuted and retain the resulting gap. Use existing facilities; new runtime infrastructure needs separate justification and authorization.

## Missing facilities and cancellation

| Missing facility | Course |
| --- | --- |
| Delegation unavailable, disallowed or failed | Disclose it and investigate sequentially; state actual review mode. |
| Independent critic | Keep delegated investigation and disclose coordinator self-review. |
| Source route | Try a relevant permitted alternative and retain uncovered scope. |
| RLM execution, state or semantic-call route | Use ordinary corpus research and name the actual method. |
| GEPA cases, scorer or execution | Use [GEPA's fallback](GEPA.md#freeze-and-qualify). |
| Storage or execution | Apply [storage and execution](#storage-and-execution). |

Under a flat-team policy, workers return bounded child or semantic requests for central scheduling. Selected-passage calls and recursive external-context loops remain distinct methods under [RLM.md](RLM.md#semantic-subcalls).

On cancellation, stop commissioning and request termination where supported. Report termination only when confirmed. Unavailable required work remains an unmet requirement.
