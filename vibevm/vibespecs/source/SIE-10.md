# SIE.10 - Validate a Semantic Integration Result for Its Receiving Use: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## SIE.10:5 - Archetypal Grounding {#archetypal-grounding}

### SIE.10:5.1 - Positive AP242/QIF Subset Validation {#positive-ap242-qif-subset-validation}

The constructed AP242/QIF package is frozen with named AP242/QIF source occurrences, correspondence set, identity dispositions, claim-composition rules, mapping specification, hybrid realization, and review interface. It uses SIE.1:5's stipulated receiving contract: the preceding 24-hour observation window, two-second response limit, and permission to return qualified evidence while showing unresolved local-extension and unknown-unit branches separately.

| Layer | Constructed probe and result |
| --- | --- |
| carrier/schema | Request and response validate against their declared forms; unmatched, incompatible, unresolved, stale, and source-error states are representable. Passes structurally. |
| semantic-model/endpoints | AP242 feature/configuration/effectivity and QIF plan/characteristic/result senses are recoverable. One local extension remains undefined; rows that consume it are unresolved. |
| correspondence | Known plan/feature relation passes; shared-label false match is rejected; non-dimensional characteristic defeats a global type equivalence. Passes for the accepted row set. |
| identity/authority | Known feature identifier relation passes at revision/configuration/effectivity grain; obsolete revision and unresolved local ID stop their dependent branches. Engineering and quality authority remain external. |
| claim composition | Compatible AP242 definition/effectivity and QIF plan/result claims retain sources; contradictory result status returns conflict; incompatible intervals remain non-comparable. Passes for qualified branches. |
| transformation | Known mapping, one-to-many characteristic, unit conversion, unmatched feature, unknown unit, stale result, missing provenance, and source-timeout cases return the specified branches. One unknown-unit row stops. |
| realization/interface | Stable semantic metadata is available; volatile source data is queried under captured occurrence times. The constructed one-second response meets the two-second limit. Timeout returns incomplete only under the contract; challenge paths resolve to premises. Conditional pass. |
| provenance/currentness/quality | Every accepted output row recovers sources, rules, and times. The configuration matches the released review basis; QIF observations six hours before T meet the 24-hour window, while a 25-hour control returns stale. Undefined-extension rows remain visibly unresolved outside the qualified set. |
| receiving workflow | The quality engineer retrieves a known result, recognizes unmatched/incompatible/conflict states, and stops on unresolved configuration or identity. Passes for the bounded subset. |

The whole-use disposition is **narrow** under the stated contract: the qualified row set is usable for the evidence-return workflow, while the undefined local-extension and unknown-unit branches remain separately visible and unresolved. The receiver's permission covers this partial evidence answer. The account does not accept the inspection result or release the configuration. A definition or unit-table repair reopens only the affected rows and receiving tests.

### SIE.10:5.2 - A Decisive Defect and a Changed Receiving Meaning {#a-decisive-defect-and-a-changed-receiving-meaning}

In a constructed mapping probe, an input of 1 metre produces an output labelled 1 millimetre; the receiving contract requires 1000 millimetres. The input, rule, expected value, and observed output are enough to establish this mapping failure. Return that defect to SIE.7. Other layers remain unexamined; their results are unnecessary for this bounded failure. If the source unit is unavailable instead, the conversion premise remains unresolved at that scope.

Now consider a previously qualified availability interface. Its JSON field and numeric type stay unchanged, but the source changes the value from present availability to a future promise horizon. The receiver still reads the displayed quantity as “available now”. A passing shape check cannot support the earlier use conclusion: the changed interpretation defeats a relied-on premise. SIE.11 identifies the affected mapping and interface uses.

After repair, a positive conclusion for that receiving use needs the corrected interpretation and every other load-bearing condition. Matching earlier evidence can supply unchanged conditions; the known failure or its repair alone cannot establish the whole result.


## SIE.10:6 - Bias-Annotation {#bias-annotation}

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Governance | The validation team is treated as release, quality, safety, or business authority. | State the semantic conclusion and return the owning decision with its conditions. |
| Architecture | Available automated tests define all validation layers. | Add qualified semantic, identity, authority, and receiving-work evidence where automation cannot decide. |
| Ontology/Epistemology | Well-formed representation, true relation, supported claim, and usable decision collapse. | Test each claim at its layer and keep the whole-use composition explicit. |
| Pragmatics | A decisive failure still triggers every layer test. | Finish the bounded failure with sufficient evidence; require full load-bearing coverage for a positive whole-use or permitted subset claim. |
| Didactics | A score invites compensation across hard stops. | Use categorical layer dispositions with evidence and state that stops are non-compensatory. |

## SIE.10:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| Valid schema, therefore valid integration | Test meanings, relations, identity, composition, mappings, provenance, quality, and receiving Work separately. |
| One quality/confidence score | Record layer-specific evidence and categorical dispositions; preserve hard stops. |
| Happy-path demonstration | Add negative, boundary, unlike, changed-source, stale, conflict, and failure cases. |
| Provenance completeness means truth | Test the source claim and receiving adequacy; provenance only makes derivation inspectable. |
| High alignment benchmark score | Validate local endpoint relations and use loss against representative cases. |
| All-or-nothing readiness | A known defect can finish a bounded failure. A positive subset result requires the contract's permission and all premises on which that subset relies. |
| Semantic validation authorizes release | Return the account to the actual engineering, quality, safety, legal, or application authority. |

## SIE.10:10 - Rationale {#rationale}

Semantic integration is a claim chain. Different links require different evidence, and the receiver depends on their composition. Layered validation preserves this structure: no lower layer proves a higher one, while a positive conclusion requires support for every load-bearing premise of the claimed whole use or contract-permitted subset.

## SIE.10:11 - SoTA-Echoing {#sota-echoing}

The best-known line combines constraint validation, ontology-alignment evaluation, provenance, data-quality models, quality management, and user/task validation. The serious defaults are conformance-only testing and aggregate quality scoring. Their defect is not automation or measurement; it is using one layer as a proxy for the whole use. SIE.10 mutates the line into a dependency-aware account with categorical bounded dispositions and representative Work replay.

| Source line | Adopt, adapt, or reject | Role and limit |
| --- | --- | --- |
| [SHACL](https://www.w3.org/TR/shacl/) | adapt | Supplies declared RDF graph constraint validation; passing shapes do not establish all semantics, identity, truth, or use fitness. |
| [DQV](https://www.w3.org/TR/vocab-dqv/) and [ISO/IEC 25012:2008](https://www.iso.org/standard/35736.html) | adapt | Supply quality vocabulary and a data-quality model; select dimensions and measurements by receiving action. |
| [ISO 8000-61:2016](https://www.iso.org/standard/63086.html) | adapt | Contributes data-quality management process questions; process conformance does not prove a particular answer fit. |
| [OAEI 2025 results](https://oaei.ontologymatching.org/2025/results/) | adapt | Provide alignment-evaluation tasks and evidence; benchmark results do not validate a local correspondence set universally. |
| one conformance gate or aggregate score | reject as sufficient | Unlike layers and hard stops must remain separately visible before a whole-use conclusion. |

Reopen when a relied-on source, model, identifier, correspondence, composition, mapping, realization, interface, quality threshold, or receiving workflow changes; when new evidence defeats a layer; or when a representative case exposes an untested load-bearing obligation.


## SIE.10:End {#end}
