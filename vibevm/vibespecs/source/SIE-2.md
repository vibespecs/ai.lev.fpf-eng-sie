# SIE.2 - Recover and Qualify Source Semantics and Authority: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## SIE.2:5 - Archetypal Grounding - AP242 and QIF Source Cut {#archetypal-grounding-ap242-and-qif-source-cut}

For the AP242/QIF query in `SIE.1`, the team inventories only source premises that can change the configuration-bound answer.

| Source row | Qualification for the constructed use |
| --- | --- |
| AP242:2025 edition 4 | Product-definition, configuration/change, and effectivity source for the case. Record the official publication identity and current stage 90.92, “to be revised”. The source owner defines its model; Systems Engineering decides which released configuration applies locally. |
| local AP242 exchange/profile | Record the exact application protocol/profile, implementation conventions, export version, local extensions, identifiers, and configuration/effectivity fields actually supplied. The standard title alone does not establish those facts. |
| QIF source | Record the applicable ISO 23952:2020 carrier/profile, plan, characteristic, and result meanings, identifiers, measurement context, status, and local quality authority. A QIF result identifier does not establish AP242 feature identity. |
| local source records | Record export or API occurrence, timestamps, derivation, access, issuer, local configuration or inspection status, and gaps. A reachable file is not automatically current or authorized for review. |

The inventory marks an unresolved local AP242 extension used by one feature class. Because its meaning can change the correspondence, the package stops that row and returns to the extension owner. Other rows can continue. If neither AP242 nor QIF can express a required tolerance-state distinction, the inventory requests a qualified `UseFitSemanticModel@Use`; it does not invent the distinction in the transform.

## SIE.2:6 - Bias-Annotation {#bias-annotation}

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Governance | Custody or access is mistaken for semantic or value authority. | Record each authority scope and the evidence for it separately. |
| Architecture | The inventory mirrors the integration platform rather than governed sources. | Identify source assets and meanings independently of the selected realization. |
| Ontology/Epistemology | Term, concept, type, relation, identifier, claim, data, and referent collapse into one “field”. | Use separate inventory positions and preserve unresolved senses. |
| Pragmatics | Exhaustive documentation delays the use without changing it. | Inspect only premises that can change an answer, loss, test, or stop. |
| Didactics | A standards citation is read as proof that the local export conforms or is current. | Record the local profile, occurrence, evidence, extension, and effectivity separately. |

## SIE.2:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| Data dictionary by column name | Add source-local definition, scope, edition, units/codes, examples, and authority. |
| Standards title as implementation evidence | Inspect the actual profile, export, extension, occurrence, and conformance evidence. |
| “Same ID format means same object.” | Record scheme, issuer, grain, interval, and identified-entity claim; use `SIE.5` for cross-source identity. |
| Provenance equals truth | Keep derivation and source authority separate from domain truth and receiving acceptance. |
| Read every source | Start from the contract and add only action-changing premises. |
| Patch a model gap in code | Return the missing semantic-model result before relying on the rule. |

## SIE.2:10 - Rationale {#rationale}

Semantic integration cannot preserve a meaning that has not been recovered at the source. Source-local recovery also prevents a shared vocabulary from becoming a hidden replacement for source authority. Qualification by use keeps the inventory finite and prevents documentation breadth from substituting for a workable package.

## SIE.2:11 - SoTA-Echoing {#sota-echoing}

The best-known line combines terminology work, metadata-registry discipline, provenance, and source-local meaning recovery. The serious default is schema inspection plus organizational folklore. Its defect is not informality alone; it leaves no stable relation among the source claim, edition, authority, and mapping premise. SIE.2 adapts the line into a use-qualified manifest with an explicit inadequate-model return.

| Source line | Adopt, adapt, or reject | Role and limit |
| --- | --- | --- |
| Current FPF `F.0.1` and `F.0.2` | adopt | Recover source-local meaning and episteme identity; do not establish a cross-source correspondence or domain truth. |
| [ISO 704:2022](https://www.iso.org/standard/79077.html) | adapt | Keeps objects, concepts, definitions, and designations distinct; it does not decide the receiving integration. |
| [ISO/IEC 11179-3:2023](https://www.iso.org/standard/78915.html) and its [item-mapping amendment](https://www.iso.org/standard/89914.html?browse=tc) | adapt | Contribute registry-item identity, versions, definitions, and mapping metadata; no automatic cross-source identity or fitness follows. |
| [PROV-O](https://www.w3.org/TR/prov-o/) | adapt | Distinguishes entities, activities, agents, derivation, revision, invalidation, attribution, and primary source; provenance establishes neither truth nor permission. |
| schema-only discovery | reject as sufficient | Structure and samples can locate questions but cannot replace source-local meaning, edition, authority, and applicability. |

Reopen when a source change alters a relied-on meaning, scheme, edition, effectivity, authority, access condition, or provenance chain, or when repeated cases show that an inventory position cannot support the downstream decision.


## SIE.2:End {#end}
