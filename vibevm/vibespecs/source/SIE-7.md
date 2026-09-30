# SIE.7 - Specify Semantic Extraction and Transformation Mappings: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## SIE.7:5 - Archetypal Grounding - AP242/QIF Mapping Rules {#archetypal-grounding-ap242-qif-mapping-rules}

The AP242/QIF package needs a row set for the configuration-bound inspection query. Its specification includes these constructed rules:

| Rule | Semantic and executable behavior |
| --- | --- |
| `MAP-SIE-APQ-01` | Select the released AP242 product-definition revision/configuration supplied by Systems Engineering and filter features by effectivity `E`. Do not select “latest” as a substitute. |
| `MAP-SIE-APQ-02` | For each accepted `SIE.4` plan-characteristic-concerns-feature row, join exact source identifiers only under the referenced `SIE.5` feature disposition. Preserve AP242 and QIF IDs and issuers. |
| `MAP-SIE-APQ-03` | Compose AP242 definition/effectivity and QIF plan/result claims through the referenced `SIE.6` result. Emit compatible qualified claims, explicit contradiction, non-comparability, or unresolved branches; never overwrite. |
| `MAP-SIE-APQ-04` | Convert units only through the contract-approved code/unit table and retain original value, unit, conversion rule, precision, and loss. An unknown unit stops that result row. |
| `MAP-SIE-APQ-05` | Return unmatched AP242 feature, unmatched QIF characteristic, stale result, missing provenance, and source-error states distinctly. No state defaults to an accepted match. |

Positive examples cover one known configuration/feature/characteristic/result chain. Boundary cases cover one-to-many characteristics and repeated results. Negative cases cover an obsolete revision, incompatible feature, unresolved identity, unknown unit, contradictory result status, and absent QIF plan. A SQL view, R2RML mapping, QVT transformation, or application code may implement the rules; none changes the specification without reopening the affected rule.

## SIE.7:6 - Bias-Annotation {#bias-annotation}

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Governance | Mapping code silently decides source priority, identity, or authoritative value. | Require references to accepted premises and the direct authority for conversions or defaults. |
| Architecture | A tool's expressiveness defines the semantic rule. | State implementation-independent behavior and return an implementation gap when the tool cannot preserve it. |
| Ontology/Epistemology | Correspondence truth, transformation rule, performed transformation, and output claim collapse. | Keep the rule and its evidence separate from execution occurrences and resulting claims. |
| Pragmatics | The specification reproduces every implementation detail. | Include only behavior needed to preserve semantics, errors, trace, and conformance. |
| Didactics | Examples are copied as the complete rule. | State the general condition and use examples as tests, including counterexamples. |

## SIE.7:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| SQL is the mapping | Extract the semantic rule, premises, loss, errors, and tests; treat SQL as one implementation. |
| Crosswalk equals transformation | Add selection, direction, cardinality, conversions, defaults, errors, trace, and examples. |
| Null for every failure | Define distinct semantic and operational states and their receiver behavior. |
| Latest record wins | Use the direct configuration/effectivity or justified interval rule. |
| Normalize identifiers | Preserve scheme and issuer and reference the identity disposition. |
| Hidden unit conversion | Record source/target units, authority, precision, loss, and counterexample tests. |

## SIE.7:10 - Rationale {#rationale}

A semantic correspondence states a relation; an executable mapping states how source occurrences produce target claims under conditions. Making that extra structure explicit prevents implementation convenience from becoming a semantic decision and lets Data Engineering own execution without inheriting unstated SIE authority.

## SIE.7:11 - SoTA-Echoing {#sota-echoing}

The best-known line combines declarative mapping languages, model transformation, traceability, and representation-preservation checks. The serious default is code-first ETL. Code is necessary in many realizations, but as the sole specification it hides semantic premises and loss. SIE.7 adapts the line into a technology-independent, receiving-use mapping contract with explicit negative states.

| Source line | Adopt, adapt, or reject | Role and limit |
| --- | --- | --- |
| Current FPF `A.6.3.RT` | adopt | Governs preservation through representation transition; it does not specify this domain mapping. |
| [R2RML](https://www.w3.org/TR/r2rml/) | adapt | Demonstrates declarative relational-to-RDF mapping structures; RDF and relational sources are optional technology families. |
| [OMG QVT 1.3](https://www.omg.org/spec/QVT/) | adapt | Contributes model-query/view/transformation and trace forms; MOF/QVT is not mandatory. |
| [PROV-O](https://www.w3.org/TR/prov-o/) | adapt | Supports derivation and activity/agent/entity trace; provenance does not prove semantic preservation. |
| code-first ETL as sole contract | reject as sufficient | Execution can be tested only against an independently recoverable rule, loss, and branch contract. |

Reopen when an input or target scheme changes, a correspondence/identity/composition premise changes, a counterexample defeats the rule, the receiver changes accepted loss, or implementations cannot satisfy the preservation predicate.


## SIE.7:End {#end}
