# SIE.5 - Resolve Cross-Source Identity without Erasing Identifier Authority: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## SIE.5:5 - Archetypal Grounding - Semiconductor Recall Trace {#archetypal-grounding-semiconductor-recall-trace}

A recall-triage query crosses a wafer identifier from a fabrication source, die coordinates, device serials, package identifiers, supplier lot identifiers, GS1 event identifiers, and an enterprise material master. The receiving question is whether a shipped device can be traced to an affected fabrication lot.

| Endpoint question | Constructed disposition |
| --- | --- |
| wafer `W-204` and supplier lot `L-88` | not identity; the supplier record asserts that the wafer is a member/output associated with the lot under a bounded process interval. Preserve both identifiers and relation provenance. |
| die coordinate `(x17,y9)` on wafer `W-204` and device serial `D-771` | same physical die/device at the selected post-singulation grain only when the packaging event and issuer records connect them; accepted with interval and event evidence. |
| device serial `D-771` and package code `P-55` | unresolved because the package identifier is reused after rework and the event history lacks effectivity. Stop the dependent trace branch. |
| enterprise material master `M-12` and device serial `D-771` | family/type membership, not individual identity. The master describes a material/product class and authoritative enterprise attributes within its stewardship scope. |
| GS1 event `E-901` and device `D-771` | event and object are different entities; the event may concern the device. Never merge their identifiers. |

Tests cover reused package identifiers, a die split/merge error, contradictory supplier events, a missing cross-enterprise link, and a later correction. The interface returns supported trace segments and the unresolved `P-55` branch. MDM or the domain steward may later decide a master identity; SIE.5 has not done so.

## SIE.5:6 - Bias-Annotation {#bias-annotation}

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Governance | The integration registry becomes the de facto master-data authority. | State the bounded disposition and retain MDM/domain decision ownership. |
| Architecture | One canonical key is required because the platform prefers it. | Carry a surrogate technical key only with source IDs and the identity disposition it indexes. |
| Ontology/Epistemology | Same individual, part, version, variant, alternate, and family relations collapse. | Fix grain and interval, then choose the narrowest warranted relation. |
| Pragmatics | Every identifier pair receives a costly adjudication. | Decide only pairs that are load-bearing for the receiving use; leave independent rows untouched. |
| Didactics | “Same” is read as timeless universal identity. | Display conditions, interval/effectivity, scheme, and forbidden reuse beside the disposition. |

## SIE.5:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| Same string, same entity | Add scheme, issuer, grain, interval, and discriminating evidence. |
| Universal `sameAs` | Use the narrowest relation and record unresolved or different cases. |
| Master key by integration fiat | Return master-identity and survivorship decisions to their authority. |
| Version equals object | State whether the use concerns one continuing entity, a version-specific configuration, or a relation among them. |
| Part joined as whole | Fix the entity grain and preserve part-whole relations explicitly. |
| Drop unresolved rows | Expose them as interface and validation branches with dependent actions. |

## SIE.5:10 - Rationale {#rationale}

Identifiers are governed signs, not entities. Cross-source identity is therefore a relation claim that depends on scheme, grain, interval, evidence, and use. Preserving source identifiers and authority makes the claim reversible and prevents integration convenience from becoming a master-data or domain decision.

## SIE.5:11 - SoTA-Echoing {#sota-echoing}

The best-known line combines explicit identifier ownership and restrictions, provenance-qualified alternate/specialization relations, and domain traceability practice. The serious default is entity resolution that optimizes a match score or golden record. Its defect is not probabilistic matching itself; it is allowing the score or merged record to erase grain, issuer, interval, and decision authority. SIE.5 mutates the line into a bounded disposition consumed explicitly by downstream semantic results.

| Source line | Adopt, adapt, or reject | Role and limit |
| --- | --- | --- |
| Current FPF identity and relation law | adopt | Keeps identity and direct relations as explicit claims; generic law does not decide a domain pair. |
| [ISO 8000-115:2024](https://www.iso.org/standard/88847.html?browse=tc) | adapt | Contributes identifier owner, use restriction, semantics, and resolution inputs; excludes identifier creation, query/response syntax, and resolution method and does not decide equivalence. |
| [PROV-O](https://www.w3.org/TR/prov-o/) | adapt | Supplies specialization, alternates, derivation, attribution, revision, and invalidation relations useful to evidence; provenance relations are not blanket identity. |
| [SEMI traceability standards](https://www.semi.org/en/products-services/standards/traceability) and [GS1 EPCIS 2.0.1](https://ref.gs1.org/standards/epcis/2.0.1/) | adapt | Supply semiconductor and event-based identity/traceability probes; scheme use does not create enterprise master identity or authorize recall. |
| golden-record or score-only merging | reject as sufficient | It may support candidate generation or a steward decision but cannot erase source identifiers, relation kinds, and authority. |

Reopen when an identifier scheme or issuer rule changes, new event/configuration evidence changes the disposition, the required grain or interval changes, or repeated cases show that the disposition vocabulary cannot preserve an action-changing relation.


## SIE.5:End {#end}
