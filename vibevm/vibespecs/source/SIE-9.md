# SIE.9 - Connect a Receiving Use through a Semantic Interface: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## SIE.9:5 - Archetypal Grounding - AP242/QIF Review Interface {#archetypal-grounding-ap242-qif-review-interface}

The quality engineer uses a view or API with request parameters `productDefinitionRevision`, `configuration`, `featureIdentifier`, and `effectivity`. The candidate response preserves these positions:

| Response position | Constructed behavior |
| --- | --- |
| `feature` | AP242 source identifier, issuer/profile, configuration/effectivity, source edition, and receiver-friendly label |
| `inspectionCharacteristic` | QIF source identifier, plan and characteristic meanings, source edition, and the accepted correspondence-row reference |
| `inspectionResult` | source-qualified QIF claim, observation time/status, unit and original value, provenance, and any conversion rule |
| `identityDisposition` | referenced `SIE.5` result and its grain/interval, not a copied boolean |
| `claimStatus` | qualified, conflict, non-comparable, or unresolved with the `SIE.6` composition reference |
| `freshness` | released AP242 configuration/effectivity used, QIF observation window, retrieval time, and stale status |
| `rowDisposition` | matched, unmatched-feature, unmatched-characteristic, incompatible, unresolved-identity, stale, source-error, or prohibited |
| `returnPath` | source record and mapping/correspondence/identity/composition rule references plus the direct engineering or quality owner for the decision |

A known match returns a qualified row. A feature absent at effectivity `E` returns unmatched rather than the nearest label. An unresolved identity returns that branch without claiming no inspection exists. A source timeout returns partial/incomplete only if the contract permits it. The interface does not accept the result or release the configuration.

## SIE.9:6 - Bias-Annotation {#bias-annotation}

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Governance | Interface access is mistaken for permission to act or disclose. | State verified/assumed permissions, disclosure limits, and the direct action authority. |
| Architecture | Internal graph or warehouse schema becomes the public contract. | Design from receiving actions and preserve realization independence where useful. |
| Ontology/Epistemology | Field name, status code, and claim meaning collapse. | Define every output and branch with scope, source, time, and permitted use. |
| Pragmatics | Full provenance overwhelms routine use. | Expose the action-changing summary and a stable trace path to detailed premises. |
| Didactics | Error branches look like exceptional implementation failures. | Teach unmatched, incompatible, conflict, and unresolved as normal semantic outcomes. |

## SIE.9:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| Expose the integrated table | Start from the receiving action and design only the claims and branches it needs. |
| One null or HTTP error for every absence | Distinguish semantic absence/unresolved states from access, timeout, and implementation failure. |
| Provenance in internal logs only | Expose the action-changing provenance/currentness summary and stable trace reference. |
| Hide source IDs behind one key | Preserve source schemes and identity-disposition references. |
| Endpoint is available, therefore usable | Validate meanings, branches, currentness, service conditions, and representative Work through `SIE.10`. |
| Semantic result authorizes action | Name the application, engineering, quality, safety, legal, or other decision owner. |

## SIE.9:10 - Rationale {#rationale}

An integration result has practical value only when it crosses into receiving Work without losing the conditions that make it meaningful. The interface is therefore semantic, not merely syntactic: it carries interpretation, qualification, and return paths while leaving decision authority with the receiver.

## SIE.9:11 - SoTA-Echoing {#sota-echoing}

The best-known line combines explicit API/data-contract practice, data-on-the-Web provenance/version guidance, event interfaces, and standards-based engineering exchange. The serious default is transport-first interface design. Its defect is that success is reduced to reachability and schema conformance. SIE.9 mutates the line by making semantic branches, currentness, provenance, and challenge paths part of the receiving contract.

| Source line | Adopt, adapt, or reject | Role and limit |
| --- | --- | --- |
| [Data on the Web Best Practices](https://www.w3.org/TR/dwbp/) | adapt | Contributes metadata, provenance, version, access, and reuse questions; Web publication is optional. |
| [GS1 EPCIS 2.0.1](https://ref.gs1.org/standards/epcis/2.0.1/) | adapt | Supplies an event-oriented cross-enterprise interface case with identifiers and query semantics; it does not decide SIE identity or receiving action. |
| [ISO 10303-242:2025](https://www.iso.org/standard/84300.html?browse=tc) and [ISO 23952:2020](https://www.iso.org/standard/77461.html) | adapt | Supply unlike versioned engineering source/interface cases; their model scopes and direct authorities remain intact. |
| internal-schema or transport-first API | reject as sufficient | Reachability and schema shape cannot establish semantic interpretation, provenance, loss, branch behavior, or receiving-use fitness. |

Reopen when the receiver or action changes, a source/mapping/realization premise changes, observed service behavior violates a semantic condition, branch handling causes unsafe interpretation, or a protocol change defeats compatibility.


## SIE.9:End {#end}
