# SIE.3 - Construct or Reuse a Semantic Model for a Named Use: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## SIE.3:5 - Archetypal Grounding {#archetypal-grounding}

### SIE.3:5.1 - Reuse for Provider Availability {#reuse-for-provider-availability}

The receiving interface returns separately attributed provider quantities. Its questions are “How much is on hand now?” and “How much can this provider promise under its reservation and time-horizon rules?”

An available model already distinguishes both measures, their provider, unit, observation time, and relevant horizon. The integrator checks the following cases:

| Case | Required model interpretation |
| --- | --- |
| Provider A reports 12 on hand; provider B reports 9 available to promise. | Two qualified quantities with distinct measure meanings. |
| Both values happen to equal 12. | Numerical equality does not remove the difference between the measures. |
| The provider changes the promise horizon. | The horizon remains part of the promise meaning used by the receiver. |

The model represents these cases and has suitable access and maintenance conditions. The completed result references that edition for the two questions. It supplies no common quantity formed by adding the values; that operation would require a separately justified receiving meaning.

### SIE.3:5.2 - Extend an Inspection Model {#extend-an-inspection-model}

A constructed product-definition and inspection integration asks: “What observation concerns requirement Q for feature F in configuration R?” The source model already describes the feature and its requirement, but represents no actual observation.

| Model content | Development and case |
| --- | --- |
| Existing feature and requirement | Reuse their qualified definitions and configuration applicability. |
| Observation | Add the actual observation as distinct from its plan and the requirement being checked. |
| Observation relation | State which configured feature and applicable requirement it concerns. |
| Unit and time | Express the interpretation required for this observation and question. |
| Counterexamples | A planned inspection is not an observation; an observation of another configuration does not answer this question. |

The domain participants confirm those distinctions and identify any unresolved source-specific interpretation. The module can then supply SIE.4 and SIE.7 with the required meanings. In an AP242/QIF installation, its actual profiles, configuration relations, and inspection meanings must come from the qualified source results; the constructed model above is the working example, not a claim about a particular exchange's conformance.

## SIE.3:6 - Bias-Annotation {#bias-annotation}

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Governance | One participant's preferred vocabulary silently becomes the shared meaning. | Obtain the meanings needed by the receiving use and preserve unresolved authority or source disagreement. |
| Architecture | A platform choice determines the model's concepts. | State the questions and distinctions before selecting formalization or realization. |
| Ontology/Epistemology | Requirement, plan, observation, and result collapse because they share a label. | Use a counterexample that changes the receiving answer. |
| Pragmatics | A new ontology is built despite adequate reusable content. | Try the existing model and finish when the use is supported. |
| Didactics | A formal diagram appears sufficient without a working example. | Show how the model answers the question and excludes its counterexample. |

## SIE.3:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| Model from familiar labels | Recover relation meanings and replay a discriminating question. |
| Construction as proof of progress | Return adequate existing content when the use is already supported. |
| Hidden repair in a transformation rule | Develop the missing semantic distinction and give the rule a qualified premise. |
| Language validity used as domain adequacy | Check the domain answer as well as the selected formal properties. |

## SIE.3:10 - Architectural Rationale {#architectural-rationale}

Questions and counterexamples locate the distinctions that an integration must preserve. Reuse is therefore judged by its contribution to the question; extension is justified by a specific gap. Keeping model content, its maintained edition, its formal encoding, and its instances distinct makes both adequacy and later change easier to assess.

## SIE.3:11 - SoTA-Echoing {#sota-echoing}

The practice question is how to settle an available model's adequacy for the receiving questions when that adequacy is still unknown. For the inspection question in §5.2, the selected starting line is requirements-led model qualification: recover the distinction between requirement, plan, and observation, try the available meanings, and develop only the gap that survives that trial. This adapts [LOT](https://doi.org/10.1016/j.engappai.2022.104755) and its [maintained resources](https://github.com/oeg-upm/LOT-resources).

A serious alternative for that same unsettled question is to develop the model together with a small knowledge-graph prototype, adapting the ontology-and-graph work described by [LOT4KG](https://lot.linkeddata.es/LOT4KG/). The prototype can reveal a missing relation when the receiving query is executed. Compare a bounded prototype with bounded model qualification, rather than charging it for a complete production platform:

| Answer to the same inspection-model question | Comparable work and useful evidence | Choice and accepted trade-off |
| --- | --- | --- |
| Qualify or extend the model before selecting its realization | Examine the required definitions with domain participants and replay the requirement/plan/observation, configuration, unit, and time cases. Keep the model and cases sufficient for that query. | **Adapt** LOT in §4.1.1–5 and §5.2. This settles the semantic distinction without choosing graph encoding or query machinery. It supplies no evidence that an executable mapping or query is correct; SIE.7 and SIE.10 still need that evidence for their own claims. |
| Qualify the model through a small graph and executable query | Examine the same definitions and cases, then encode representative instances and the query. This adds encoding and execution work but can expose errors that a prose-only model trial misses. | **Adapt** the LOT4KG route when execution can settle an uncertainty material to model adequacy, especially when graph realization is already selected. In §5.2, the first unresolved issue is what counts as an observation; executing a query over a class that also includes plans cannot settle that domain meaning. The model-first route is selected for that issue, accepting deferred execution evidence. |

The comparison is qualitative and scoped to the same questions and counterexamples; it is not a claim that one route is always cheaper or more effective. A prototype's additional effort earns its place when it can change the qualification. Neither route can replace domain meaning with successful execution.

The remaining contributions constrain that choice:

| Source and comparison role | Operative move and limit |
| --- | --- |
| LOT supplies the selected requirements, development, publication, and maintenance line. | **Adopt** domain questions and participant validation; **adapt** §4.1.3 and §4.1.7 so sufficient reuse can finish and the receiver can rely on a maintained model. The source does not decide local meanings or establish this model's adequacy. |
| LOT4KG supplies the coupled ontology/graph alternative. | **Adapt** its separation of ontology work and graph construction to the comparison above; **reject** treating graph construction as the only way to qualify a model. Its described activities support this alternative, not a measured superiority claim. |
| [OWL 2 Overview](https://www.w3.org/TR/owl2-overview/) supplies language and profile choices when formal semantics matter. | **Adapt** §4.1.6: check the properties actually claimed for the chosen language as well as the domain cases. Encoding validity cannot replace the model-adequacy question. |
| The public [ISO/IEC 21838-1](https://www.iso.org/standard/71954.html) scope supplies a possible top-level basis. | **Adapt** §4.1.2/6 only when that basis contributes needed coherence. It establishes neither a universal upper-ontology requirement nor local maintenance and versioning rules. |

Reopen the comparison if one required answer depends on a selected query or inference behavior that the model-only trial cannot settle, if a bounded prototype exposes a missed distinction, or if an available model can now answer the same cases with less qualification work. Return only to the affected question and §4.1.2–6. An already qualified model for an unchanged use remains the sufficient direct result in §4.1.3.


## SIE.3:End {#end}
