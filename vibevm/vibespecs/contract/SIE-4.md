# SIE.4 - Judge Cross-Source Correspondences and Their Permitted Uses {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Eternal alpha
> **Normativity:** Normative method guidance within SIE; examples are constructed and non-normative.
>
> **Primary working result:** a `QualifiedCorrespondenceSet@Use` whose rows identify exact source-local endpoints, relation or incompatibility, orientation, bounded use, permitted loss, justification and evidence, source versions, counterexamples, confidence where meaningful, and accepted, rejected, unresolved, or incompatible disposition.

## SIE.4:1 - Problem Frame {#problem-frame}

**Use this when** two or more governed sources contain concepts, types, relations, fields, codes, model elements, or claims that appear to match and a receiving use needs their relation made explicit. Typical triggers are a shared label, a crosswalk, an automated matcher result, a spreadsheet of “equivalences”, or a model-to-model mapping whose semantic premise has never been judged.

The primary EntityOfConcern is one use-qualified cross-source correspondence row. The first move is to recover both endpoint senses and ask which direct relation, difference, or incompatibility is actually supported. The first result is a set that preserves accepted, rejected, unresolved, and incompatible rows rather than forcing every candidate into an equivalence.

The payoff is a defensible semantic premise for identity work, claim composition, executable mappings, and validation. Do not use SIE.4 to construct a missing semantic model, decide cross-source identity, define transformation code, or choose the authoritative value. A local relation inside one governed source remains with its source owner unless the cross-source use makes it an integration premise.

## SIE.4:2 - Problem {#problem}

Correspondence candidates are cheap. Labels can be normalized, lexical similarity scored, hierarchies compared, and model structures aligned. Yet “similar”, “related”, “narrower”, “same field name”, and “safe to substitute here” answer different questions. A row can be a true relation and still lose distinctions that the receiving use requires.

When candidate generation and qualification collapse, downstream mapping code inherits an unstated ontology and loss policy. Counterexamples are discarded as data-quality defects, source versions disappear, and a reviewer cannot tell whether the relation itself or only its use is unsupported.

## SIE.4:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Automation | Matchers can surface many candidates, while their scores do not establish relation truth or permitted use. |
| Reuse | A general crosswalk is attractive, while relation adequacy can change with receiver, grain, interval, and accepted loss. |
| Precision | Exact relation kinds prevent overclaim, while sources may not support a complete formal characterization. |
| Coverage | Pressure favors filling every row, while unresolved and incompatible rows can be the most decision-useful result. |
| Direction | Transformation needs an orientation, while many conceptual relations are not symmetric or safely reversible. |
| Versioning | Stable mapping identifiers aid reuse, while endpoint meaning can change across source editions and profiles. |

## SIE.4:4 - Solution {#solution}

Separate candidate discovery, direct relation judgment, and bounded-use qualification. For each row, identify exact source-local endpoints, state the relation or incompatibility and orientation, justify it with evidence and counterexamples, then decide whether that relation may support the named use under a stated loss boundary. Keep the direct relation and its use qualification independently inspectable.

### SIE.4:4.1 - Pattern-Use Unfolding {#pattern-use-unfolding}

1. **Take the question from the contract.** State the receiving answer and why this endpoint relation can change it.
2. **Bind exact endpoints.** Reference the `SIE.2` source rows, schemes, definitions, editions, profiles, effectivity, units, codes, and local extensions. Do not map labels without their senses.
3. **Generate candidates without promotion.** Lexical, structural, instance, expert, historical, or matcher evidence may nominate a row. Record the candidate source and score where useful, but do not treat nomination as acceptance.
4. **State the direct relation or difference.** Use the narrowest warranted relation vocabulary. State direction and whether the inverse, symmetry, or transitivity is actually supported. If no positive relation is established, choose rejected, unresolved, or incompatible with reason.
5. **Test examples and counterexamples.** Include instances or cases that should satisfy the relation and cases that distinguish endpoints, including version, unit, code, granularity, lifecycle, and authority differences.
6. **Qualify the receiving use.** State which substitution, comparison, join, navigation, or transformation the row permits, what semantic loss it introduces, and which uses remain forbidden.
7. **Preserve evidence and authority.** Record justification, evidence source, reviewer or domain authority where required, uncertainty or confidence, and the owner of any unresolved domain judgment.
8. **Assign a row disposition.** Use accepted-for-use, accepted-with-loss, rejected, unresolved, or incompatible. A row can state a true broader/narrower relation yet be rejected for this use.
9. **State dependencies and tests.** Name whether `SIE.5`, `SIE.6`, or `SIE.7` consumes the row, plus a test or observation that reopens it.

### SIE.4:4.2 - Record the Result {#record-the-result}

| Correspondence position | Required content |
| --- | --- |
| row identity and use | stable row identifier, receiver/use, consuming result |
| source endpoint | source, scheme/model, exact sense, edition/profile/effectivity, identifier |
| target endpoint | source, scheme/model, exact sense, edition/profile/effectivity, identifier |
| direct relation | relation or explicit difference/incompatibility, orientation, inverse/symmetry/transitivity qualification |
| use qualification | permitted operation, accepted loss, forbidden reuse, conditions |
| warrant | candidate origin, justification, evidence, authority, uncertainty/confidence where meaningful |
| challenge | positive examples, counterexamples, negative/unlike cases |
| disposition and continuation | accepted-for-use, accepted-with-loss, rejected, unresolved, incompatible; downstream reference and reopen condition |

### SIE.4:4.3 - What Changes in Practice {#what-changes-in-practice}

The team stops treating a mapping spreadsheet as a bag of equalities. A matcher result becomes a candidate; a domain judgment becomes a relation warrant; and a receiving-use decision states what the relation may safely support. Unresolved and incompatible rows remain visible to the interface and tests.

## SIE.4:7 - Conformance Checklist {#conformance-checklist}

- [ ] Every row serves a named receiving use and consuming result.
- [ ] Both endpoints reference exact source-local senses and applicable editions/profiles.
- [ ] Candidate generation is distinguishable from relation judgment.
- [ ] The direct relation, difference, or incompatibility uses the narrowest warranted kind and states orientation.
- [ ] Inverse, symmetry, and transitivity are not inferred without support.
- [ ] Positive examples and discriminating counterexamples are present where load-bearing.
- [ ] Permitted operation, semantic loss, conditions, and forbidden reuse are explicit.
- [ ] Evidence, uncertainty/confidence, and decision authority are inspectable.
- [ ] Rejected, unresolved, and incompatible rows remain available to downstream interfaces and tests.
- [ ] The set claims neither cross-source identity nor executable transformation by implication.

## SIE.4:9 - Consequences {#consequences}

The correspondence set gives mapping and interface work explicit semantic premises and preserves honest negative results. It makes version and loss dependencies visible and allows a narrow use to proceed while other rows remain unresolved.

The cost is row-level judgment and counterexample work. Automated matchers remain useful for candidate discovery but cannot close the relation or its receiving-use qualification alone.

## SIE.4:12 - Relations {#relations}

- `SIE.2` supplies exact endpoint senses, editions, profiles, authority limits, and model gaps.
- `SIE.3` is a conditional external return when available models cannot express a required endpoint distinction.
- `SIE.5` consumes rows that expose a load-bearing cross-source identity question.
- `SIE.6` uses correspondences to decide which source claims are comparable or composable without erasing scope or conflict.
- `SIE.7` consumes only accepted rows under their stated use and loss conditions; it adds executable transformation semantics.
- `SIE.10` tests correspondence truth and use qualification independently from mapping execution.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-eng-sie/contract/SIE-2#root; supplied spec://ai.lev/fpf-eng-sie/contract/SIE-3#root result when required; FPF spec://ai.lev/fpf-spec/contract/F-9#root @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-adm/contract/ADM-13#root, spec://ai.lev/fpf-eng-adm/contract/ADM-4#root, spec://ai.lev/fpf-eng-sie/contract/SIE-12#root, spec://ai.lev/fpf-eng-sie/contract/SIE-5#root, spec://ai.lev/fpf-eng-sie/contract/SIE-6#root, spec://ai.lev/fpf-eng-sie/contract/SIE-7#root @status:spec/done

#source spec://ai.lev/fpf-eng-sie/source/SIE-4
