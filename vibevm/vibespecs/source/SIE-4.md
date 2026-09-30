# SIE.4 - Judge Cross-Source Correspondences and Their Permitted Uses: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## SIE.4:5 - Archetypal Grounding - Product Feature and Inspection Characteristic {#archetypal-grounding-product-feature-and-inspection}

In the AP242/QIF application, the lexical candidate `feature ↔ characteristic` is too broad. The source inventory distinguishes an AP242 product-definition feature, a QIF inspection characteristic, the plan relation that applies a characteristic to a feature, and a measured result concerning that characteristic.

| Candidate row | Direct relation judgment | Use qualification and disposition |
| --- | --- | --- |
| AP242 feature `F-17` ↔ QIF characteristic `C-17` | not identity and not class equivalence; the QIF plan asserts that `C-17` concerns the identified product feature under configuration/effectivity `R/E` | accepted-for-use as a directed `inspection-characteristic-concerns-feature` relation only after `SIE.5` qualifies the feature endpoint; no reverse substitution |
| AP242 feature type `hole` ↔ QIF characteristic type `diameter` | a diameter characteristic can characterize some holes, but the types are neither equal nor simply broader/narrower | accepted-for-use for navigation from a selected plan row with a qualified feature endpoint to its linked hole feature and diameter characteristic. Return their separate source identifiers and types with the plan relation; forbidden as a global type crosswalk |
| AP242 feature `F-22` ↔ QIF characteristic `C-99` | the candidate arose from a shared local label; effectivity and plan evidence do not support the relation | rejected; the interface returns unmatched rather than joining |
| legacy feature class ↔ current QIF characteristic class | one local extension lacks an authoritative definition | unresolved and stopped for dependent mapping; return to the extension owner |

The set records endpoint editions and counterexamples such as a non-dimensional inspection characteristic and a feature absent at effectivity `E`. It establishes semantic premises; it does not decide that identifiers denote the same entity or specify executable joins.

## SIE.4:6 - Bias-Annotation {#bias-annotation}

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Governance | A matcher or integrator silently becomes the domain relation authority. | Record the warrant, decision scope, and required domain authority for each accepted row. |
| Architecture | Available mapping technology limits the relation vocabulary. | State the semantic relation first; choose its carrier later. |
| Ontology/Epistemology | Similarity, correlation, broader/narrower relation, and equivalence collapse. | Use the narrowest supported relation and preserve uncertainty and counterexamples. |
| Pragmatics | Every possible endpoint pair is reviewed. | Restrict rows to relations that can change the contract or a dependent result. |
| Didactics | Direction arrows are read as a mandatory processing order. | Explain orientation as relation or transformation meaning, not lifecycle sequence. |

## SIE.4:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| Same label, therefore same meaning | Recover endpoint senses and test counterexamples. |
| Matcher score as truth | Treat the score as candidate evidence; obtain a relation warrant and use decision. |
| Every relation is `sameAs` | Distinguish identity, equivalence, broader/narrower, related, concerns, transforms-to, difference, and incompatibility. |
| One global crosswalk | Qualify rows by use, source editions, loss, and forbidden reuse. |
| Symmetric spreadsheet mapping | State orientation and test whether the inverse is supported. |
| Delete failed rows | Retain rejected, unresolved, and incompatible dispositions for receiver and validation behavior. |

## SIE.4:10 - Rationale {#rationale}

A direct relation and permission to use that relation answer different questions. Keeping them separate allows a true relation to be rejected for a loss-sensitive use and a qualified narrow relation to support one operation without being promoted globally. This is the smallest structure that protects both semantic truth and practical action.

## SIE.4:11 - SoTA-Echoing {#sota-echoing}

The best-known line combines explicit relation vocabularies, mapping metadata, alignment evaluation, and direct Bridge truth. The serious default is a two-column crosswalk plus confidence score. Its defect is that it hides endpoint senses, relation algebra, bounded-use loss, and counterexamples. SIE.4 adapts current mapping practice into a set whose negative dispositions and use qualification are first-class.

| Source line | Adopt, adapt, or reject | Role and limit |
| --- | --- | --- |
| Current FPF `F.9` | adopt | Governs each direct cross-context Bridge and separate bounded-use claim; a package row must not replace Bridge truth. |
| [SKOS Reference](https://www.w3.org/TR/skos-reference/) | adapt | Supplies distinct mapping relation forms and cautions through their semantics; SKOS does not prove a candidate relation or authorize substitution. |
| [SSSOM 1.0](https://mapping-commons.github.io/sssom/1.0/spec-model/) | adapt | Contributes inspectable subjects, predicates, objects, provenance, justification, confidence, and source versions; metadata completeness is not relation truth. |
| [OAEI 2025 results](https://oaei.ontologymatching.org/2025/results/) | adapt | Demonstrate task- and track-dependent alignment evaluation; benchmark performance does not decide a local row. |
| label-only or score-only crosswalk | reject as sufficient | It can nominate candidates but cannot establish endpoint senses, relation, permitted loss, or authority. |

Reopen when an endpoint meaning or edition changes, a counterexample defeats the relation or use qualification, the receiver's loss boundary changes, or a better relation vocabulary materially changes action.


## SIE.4:End {#end}
