# Sources, claims and records

Read this reference for open source discovery, captured evidence or a documented run.

## Source discovery

Translate the brief into evidence needs. Honor supplied-only, offline, privacy and access constraints; otherwise choose relevant accessible routes without requiring a user-provided bibliography.

| Evidence need | Useful routes | Evidential scope |
| --- | --- | --- |
| Actual project behavior | Source/config/tests, runtime observations, Git history, releases/issues | Version-specific implementation or observed behavior; an issue report remains attributed evidence. |
| Documented mechanism/API | First-party docs, specifications, original papers and authors' code | Contract and evaluated conditions, with version/transfer limits. |
| Organization-specific decisions | Dated records, local notes and relevant enterprise connectors | Source-qualified decisions, exact entities and unresolved ownership. |
| Missing scenarios | Practitioner accounts, forums and issue trackers | Attributed experiences and hypotheses; anecdotes do not establish prevalence. |
| Other domain facts | Official records, datasets, standards and primary publications | Authority assessed for the particular claim. |

Record `question → source route → purpose → coverage/access gap`. Start with exact entities, versions and evidence horizon. Discover actual tools through [HOST.md](HOST.md) when access is uncertain. Read located originals and follow linked evidence when it can change the answer.

A failed request or no search hit describes the attempted retrieval, not universal absence. Change routes for material gaps and report the scope actually covered.

**Discovery complete:** Each material evidence need has a readable source route or an explicit access/coverage gap.

## Claims and captures

For material claims record the original locator, date/version/scope, relevant span, supporting excerpt, evidential status and conflict/gap:

- **Source assertion:** what a source says, with its authority and limits.
- **Observation:** what the performed inspection or check established.
- **Inference:** a derived conclusion with verified inputs and a checkable derivation.
- **Disputed:** a conclusion with unresolved conflicting support.

Keep unread and partial sources explicit. A snippet can support only the bounded claim its contents establish. For structured returns, [CONTRACTS.md](CONTRACTS.md#workerresult) defines the corresponding fields.

For captured corpora, preserve original locators, extraction status and stable span conventions. Raw-byte hashes and normalized-text digests identify different representations; changing evidence requires rechecking cached locators and conclusions. Preserve raw attachments and manual judgments under project conventions.

**Evidence ready:** Each material claim has inspectable support and status; unread scope, conflicts and missing conditions are recorded for review.

## Records and continuation

Use one project-local case record when continuation or a documented run needs it. Keep the brief, evidence map, enquiry/dependency statuses, accepted findings, gaps, allocated/observed work and next step. Link bulky corpora and results. Use [CONTRACTS.md](CONTRACTS.md#publication-and-event-records) for requested structured publication.

Provide brief progress at consequential source, dispatch, return, acceptance and recovery events unless quiet output is requested. An event records sequence, phase, actor/enquiry, action, concise grounds, actual outcome/status and locator; add observed timestamps when available. Keep proposed work, returned findings and accepted conclusions distinct. Record outcomes rather than private reasoning or raw secrets.

For JEV, RLM or GEPA used in a case, link the records required by that procedure. A requested or attempted mechanism that did not execute needs its reason and resulting gap; unrelated unused mechanisms need no inventory. Derive counts, costs and timing from observed records.

Before continuation, verify source identities, accepted scope and pending enquiries. Ordinary files aid reconstruction; recovery guarantees depend on the host.

**Record complete:** Saved artifacts resolve, the next step or final result is explicit, and the record accounts for actual decisions/checks and material limits.
