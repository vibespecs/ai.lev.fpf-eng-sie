# SIE.11 - Trace Semantic Change and Revalidate Affected Uses: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## SIE.11:5 - Archetypal Grounding {#archetypal-grounding}

### SIE.11:5.1 - Compatible Reference Repair {#compatible-reference-repair}

A publisher moves a vocabulary definition to a new documentation address. The integrator can access both the relied-on content and its new location. The definition, applicability, and access needed by the mapping remain compatible.

The integrator updates the reference used by that mapping. Its existing qualification still answers the unchanged question. This is the completed result for the reference-maintenance use; no multi-use account is needed.

If the later definition cannot be inspected, the same evidence cannot support this conclusion. The result then names the inaccessible comparison and the reliance it leaves unresolved.

### SIE.11:5.2 - Changed Promise Horizon {#changed-promise-horizon}

A provider changes `availableToPromise` from the reservation meaning used for present availability to a promise for a future horizon. The API field and its numeric type stay the same. The semantic-integration maintainer compares the two meanings and inspects the actual consumers.

| Use | Reliance and result |
| --- | --- |
| Present-availability endpoint | Its mapping treated the quantity as answering “available now”. That premise changed. Repair the mapping and interface meaning, or withhold that answer until a qualified present-time source is supplied. SIE.10 checks the supported receiving result. |
| Future planning view | It can potentially use the new quantity when it exposes the horizon and the receiving question agrees. Validate those conditions instead of assuming that every use must stop. |
| Descriptive product catalogue | Its definitions and product descriptions do not consume the changed quantity. Where that independence is established, retain its matching result. |
| A consumer with unavailable interpretation | The maintainer cannot determine how it uses the quantity. Return that scoped uncertainty; the other completed branches retain their own results. |

If the service owner needs an integration-wide continuation decision, the account combines those results and the remaining uncertainty. It does not state that all uses are unaffected. The provider controls its source definition; the integrator controls the supplied semantic interface; each application owner determines whether the qualified answer is adequate for its decision.

## SIE.11:6 - Bias-Annotation {#bias-annotation}

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Governance | The integration maintainer appears to authorize the application's decision. | Return the qualified integration result to the receiving decision owner. |
| Architecture | Every linked component is treated as an affected consumer. | Follow the changed proposition through dependencies that can alter results. |
| Ontology/Epistemology | An unchanged field name is read as unchanged meaning. | Compare the actual definition, applicability, and receiving interpretation. |
| Pragmatics | All validation restarts after every source version change. | Retain matching results and finish sufficient direct repairs. |
| Didactics | A list of completed checks looks like complete coverage. | State which uses the evidence covers and preserve unresolved reach. |

## SIE.11:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| Schema compatibility as semantic compatibility | Compare the question answered by the field, including its horizon and applicability. |
| Every reference occurrence requires revalidation | Establish whether the result relies on the changed proposition. |
| One repaired branch clears the whole integration | Bound the conclusion by discovered and assessed uses. |
| Summary required before its constituent decisions | Complete direct domain results first and summarize only when a receiver needs it. |

## SIE.11:10 - Architectural Rationale {#architectural-rationale}

The changed proposition, rather than the changed carrier, determines semantic impact. Direct domain Methods decide the affected result; discovery determines where those questions arise. Keeping those contributions distinct permits reuse, independent completion, and honest limits on wider conclusions.

## SIE.11:11 - SoTA-Echoing {#sota-echoing}

The practice question is which receiving uses must change when one semantic premise has changed and the affected scope is still unsettled. In §5.2, both the present-availability endpoint and other consumers exist; knowing the changed field alone does not settle their reliance. The selected line combines A.10/A.10.1's premise comparison and scoped discovery with the integration-specific returns in §4.2.

The serious alternative is a bounded full regression: identify the same receiving scope, update the tests to the new source meaning, and revalidate every registered use in it. This can be preferable when the suite is small and inexpensive or a reliable dependency analysis would cost more. It is not merely rerunning old tests against an unchanged schema.

| Answer to the same multi-use horizon change | Work and evidence at the same scope | Selection and accepted trade-off |
| --- | --- | --- |
| Discover changed reliance and revalidate affected results | Compare the two meanings, inspect source-side and receiver-side dependencies, qualify coverage, and retest results that rely on the changed horizon. Keep applicable evidence for the independent catalogue. | **Adopt** A.10/A.10.1 in §4.1.1–3/5–7; **adapt** §4.2 and §5.2 to semantic model, mapping, interface, and validation results. This avoids repeating the catalogue's unrelated checks and lets supported branches finish. It spends effort establishing dependencies and leaves an inaccessible consumer unresolved. |
| Revalidate every identified use in the same receiving scope | Make the same meaning and coverage comparison, then execute the appropriate receiving-use checks for every member, including those ultimately found independent. | Retain this alternative when those checks are cheaper or more dependable than selective impact analysis. It may reduce reliance on a detailed dependency model, but can repeat unaffected checks and delay a common release. It still cannot clear an unknown consumer or infer meaning from schema compatibility. |

For the worked horizon case, the established catalogue independence and separable endpoint results justify selective revalidation. The accepted trade-off is the work needed to establish that independence and the explicit limit on the unknown consumer; no universal cost or completeness advantage is claimed. §4.1.7 prevents local completions from being mistaken for a wider no-impact result. For one already known use, the direct domain result remains sufficient under §1.

[LOT4KG](https://lot.linkeddata.es/LOT4KG/) supplies a current candidate line for changes that propagate between an ontology, mappings, graph content, constraints, and validation. **Adapt** those relationships in §4.1.4–5 and §4.2 when a KG realization is selected. They help locate which integration result needs work; they do not choose source truth, application action, or a universal regression policy. For other realizations, the same return question is answered from their actual semantic dependencies. **Reject** a changed version alone as evidence that every use failed, and an unchanged carrier alone as evidence that every use passed.

Reopen this comparison when one actual affected use was missed, when a dependency or coverage claim is defeated, or when the cost of qualifying selective impact exceeds the available full receiving-use regression. Reconsider only the affected discovery and checking choice in §4.1.3–5. Changed results still require their domain evidence whichever strategy is selected.


## SIE.11:End {#end}
