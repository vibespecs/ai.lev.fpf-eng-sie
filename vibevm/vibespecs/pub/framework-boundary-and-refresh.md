# Framework Boundary and Refresh {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. A section of the publication that is not a pattern. See LICENSE.md for the list of changes.

## Intended use and ordinary non-use {#intended-use-and-ordinary-non-use}

Use this framework when the working result must make separately governed meanings, identities, claims, or representations usable together for a named receiver. Use one pattern or a small cooperating set and stop at the first decision-changing result or honest blocker.

Do not use SIE for local modeling with no cross-source receiving-use question, physical data movement, pipeline operation, one application's schema design, master-data authority, product configuration or release, generic representation choice, or the receiver's operational decision. Obtain those results from their owning practices. A local mapping inside one source can remain local unless it changes a cross-source semantic result.

## PatternID and reader order {#patternid-and-reader-order}

`SIE.*` is the Semantic Integration Engineering PatternID namespace. Numbers are stable addresses, not steps or maturity levels. The Table of Contents gives reader order. A dependency names a result needed by one use; it does not require every lower-numbered body to run.

## Supplied pattern repertoire {#supplied-pattern-repertoire}

The complete first edition supplies `SIE.1`–`SIE.12`. The model, change, and commons entries return these domain results:

- `SIE.3 - Construct or Reuse a Semantic Model for a Named Use`: adequate reuse or the semantic development required by a demonstrated gap.
- `SIE.11 - Trace Semantic Change and Revalidate Affected Uses`: direct affected-use results, with a common account when a receiver needs it.
- `SIE.12 - Govern Modular Semantic Commons without Universal Authority`: a working shared-module arrangement for actual users.

A supplied Method guides the work; an inaccessible source, unresolved meaning, missing right, or absent implementation result can still limit a particular use.

## Package anatomy and direct result relations {#package-anatomy-and-direct-result-relations}

| Package part | Supplying body or return | Minimum inspectable content |
| --- | --- | --- |
| use contract | `SIE.1` | receiver, use, answer claims, tolerated loss/uncertainty, freshness/latency/quality, authority, representative tests, stop and reopen |
| source manifest | `SIE.2`; SIE.3 qualification when needed | assets, schemes, editions/effectivity, meanings and identifiers used, owners/authority, provenance/access, gaps, and references to required model qualifications |
| correspondence set | `SIE.4` | endpoints, relation or incompatibility, orientation, bounded use, permitted loss, justification/evidence, source versions, counterexamples and unresolved rows |
| cross-source identity disposition | `SIE.5` | load-bearing endpoints, grain and interval, disposition kind, schemes and issuers, evidence, authority boundary, downstream references for the relied-on identity; an explanation of unused identity only when it affects interpretation or later reliance |
| source-qualified claim composition | `SIE.6` | source claims, scope, interval, authority, uncertainty, derivation, relied-on identity premises, comparable/conflicting/non-comparable/unresolved relation, qualified view or explicit conflict |
| mapping specification | `SIE.7` | schemes, accepted semantic inputs, rules, conditions, cardinalities, units/codes, defaults, errors, loss, trace, examples and tests |
| realization and interface | `SIE.8`, `SIE.9` | virtual/materialized/hybrid decision, required implementation result, receiver contract, interpretation, currentness, errors, provenance, access assumptions and return path |
| validation account | `SIE.10` | evidence sufficient for the bounded disposition; every load-bearing layer and required cases for a positive use claim; material unexamined reach, pass/narrow/unresolved/stop, and reopen condition |

`SIE.1 → SIE.2` supplies the use and source cut. `SIE.2 → SIE.3` is conditional. `SIE.2` and any supplied use-fit model feed `SIE.4`–`SIE.6`. `SIE.4` can expose an identity question for `SIE.5` and supplies semantic premises to `SIE.7`. `SIE.5` supplies load-bearing identity premises to `SIE.6`, `SIE.7`, and `SIE.10`. `SIE.6` supplies a qualified composition or explicit conflict branch to `SIE.7` and `SIE.9`. `SIE.7 → SIE.8 → SIE.9 → SIE.10` connects executable semantics to realization, receiver, and bounded validation. SIE.11 revisits only affected reliance, using these dependencies where material. SIE.12 supplies shared-module arrangements when actual users require them. These relations may iterate.

## Pattern selection and first returned result {#pattern-selection-and-first-returned-result}

| Working question | Start or return | First result |
| --- | --- | --- |
| What use and loss boundary govern the integration? | `SIE.1` | `SemanticIntegrationUseContract@Use` |
| What does each source mean and own? | `SIE.2` | `SourceSemanticInventory@Use` |
| Are the available models adequate, or what content must change? | `SIE.3` when adequacy is unsettled | `UseFitSemanticModel@Use` or exact blocker |
| Which endpoints correspond or remain incompatible? | `SIE.4` | `QualifiedCorrespondenceSet@Use` |
| Which identifiers concern the same entity at this grain and interval? | `SIE.5` | `CrossSourceIdentityDisposition@Use` |
| How can governed claims be composed without hiding conflict? | `SIE.6` | `SourceQualifiedClaimFusion@Use` |
| Which executable rules implement the accepted semantics? | `SIE.7` | `ExecutableSemanticMappingSpecification@Use` |
| Should the arrangement be virtual, materialized, or hybrid? | `SIE.8` | `SemanticRealizationDecision@Use` |
| What interface carries the meaning into receiving Work? | `SIE.9` | `ReceivingSemanticInterface@Use` |
| Is the result usable for the named receiver? | `SIE.10` | `SemanticIntegrationValidationAccount@Use` |
| What follows from a changed semantic premise? | `SIE.11` | qualified direct result, scoped gap, or a common affected-use account when needed |
| How should shared semantic modules be maintained? | `SIE.12` for actual commons users | `ModularSemanticCommonsAccount@Community` or exact blocker |

## Source use and currentness {#source-use-and-currentness}

The source contributions guide particular actions and qualifications. Each body states what a source contributes and what remains outside its authority.

| Source family | Contribution used here | Qualification and reopen |
| --- | --- | --- |
| Current FPF | source-local meaning, episteme identity, direct Bridge truth, bounded representation use, claim/provenance reliance, representation transition, currentness and affected-use distinctions | FPF retains the generic concepts and assurance law. A changed relied-on result reopens only its SIE consumer. |
| Current Method Engineering | situational criteria and the separate repertoire, variant, introduction, and revision Methods in `ME.2`, `ME.15`–`ME.17` | SIE supplies domain content; it does not duplicate Method identity or lifecycle decisions. |
| Current Systems Engineering | engineering-description, configuration/effectivity, change, release, integration, and assurance results | SIE can supply a qualified semantic premise; SYSE retains engineering decisions. |
| [ISO 704:2022](https://www.iso.org/standard/79077.html) and [ISO/IEC 11179-3:2023](https://www.iso.org/standard/78915.html) | distinguish objects, concepts, definitions, designations, registry items, versions, and mapping metadata | do not establish cross-source identity, truth, or receiving-use fitness |
| [LOT](https://doi.org/10.1016/j.engappai.2022.104755), [maintained LOT resources](https://github.com/oeg-upm/LOT-resources), and [LOT4KG](https://lot.linkeddata.es/LOT4KG/) | competency/use questions, domain-participant validation, qualified reuse or development, and dependencies between an ontology and a selected graph realization | reuse can finish the model question; LOT4KG's maintained activities do not establish a final peer-reviewed edition or a measured advantage |
| [OWL 2](https://www.w3.org/TR/owl2-overview/) and the public [ISO/IEC 21838-1:2021](https://www.iso.org/standard/71954.html) description | explicit language semantics and profile choices when formalization is useful; a deliberately selected top-level basis when coherence needs it | formal validity does not supply domain adequacy; no universal ontology or full-standard conformance is required or claimed |
| [OBO Foundry principles](https://obofoundry.org/principles/fp-000-summary.html), including [term stability](https://obofoundry.org/principles/fp-019-term-stability.html), [contact responsibility](https://obofoundry.org/principles/fp-011-locus-of-authority.html), and [notification](https://obofoundry.org/principles/fp-013-notification.html) | actual module users, stable identification, scoped shared content, reachable responsibility, and notice of changes affecting reliance | adapt to the particular commons; contact does not itself assign content or release rights, and an OBO-specific notice interval is not universal |
| [SKOS](https://www.w3.org/TR/skos-reference/), [SSSOM 1.0](https://mapping-commons.github.io/sssom/1.0/spec-model/), and [OAEI 2025](https://oaei.ontologymatching.org/2025/results/) | correspondence kinds, reusable mapping metadata, and task-dependent alignment evidence | a label, similarity score, or matcher output remains a candidate premise |
| [ISO 8000-115:2024](https://www.iso.org/standard/88847.html?browse=tc), [PROV-O](https://www.w3.org/TR/prov-o/), [SEMI traceability](https://www.semi.org/en/products-services/standards/traceability), and [GS1 EPCIS 2.0.1](https://ref.gs1.org/standards/epcis/2.0.1/) | identifier-owner/use-restriction inputs, provenance relations, and domain identity/traceability probes | they create no cross-source equivalence, master identity, authoritative value, or receiving action |
| [R2RML](https://www.w3.org/TR/r2rml/), [OMG QVT 1.3](https://www.omg.org/spec/QVT/), and [Ontop](https://ontop-vkg.org/research/publications.html) | bounded executable mapping and virtual/materialized realization forms | no mandatory RDF, MOF, graph store, or source authority |
| [SHACL](https://www.w3.org/TR/shacl/), [DQV](https://www.w3.org/TR/vocab-dqv/), [Data on the Web Best Practices](https://www.w3.org/TR/dwbp/), [ISO/IEC 25012:2008](https://www.iso.org/standard/35736.html), and [ISO 8000-61:2016](https://www.iso.org/standard/63086.html) | distinct validation, quality, provenance/version, and quality-management questions | no one layer or score proves receiving-use adequacy |
| [ISO 10303-242:2025](https://www.iso.org/standard/84300.html?browse=tc) and [ISO 23952:2020](https://www.iso.org/standard/77461.html) | versioned product-definition/configuration and manufacturing-quality source cases | AP242 edition 4 is at stage 90.92, “to be revised”; a changed relied-on successor reopens the affected source, mapping, interface, and case only |

The foundation source cut was qualified on 4 September 2026. The model, evolution, and commons contributions were qualified on 8 September using LOT, the maintained LOT4KG description, OWL 2, and the selected OBO principles. LOT4KG's site cites an under-review manuscript and contains mixed date metadata; its inspected activities supply method guidance rather than proof of a final peer-reviewed edition or measured advantage. The earlier [2024 joint-methodology proposal](https://2024.eswc-conferences.org/wp-content/uploads/2024/05/77770275.pdf) is historical background; its future-work account does not describe the maintained method's current evolution activities. The public ISO/IEC 21838-1:2021 description and stage 90.20 systematic review since 15 July 2026 delimit its use here; no full-standard conformance is claimed. Reopen only choices affected by changed relied-on content or use conditions.

## Related modeling and engineering work {#related-modeling-and-engineering-work}

Use SIE for the contribution that makes separately governed meanings usable together. The following working questions locate that contribution and the decisions that remain with neighboring practices.

| Working question | SIE contribution | Boundary retained |
| --- | --- | --- |
| Terminology and ontology across source models | `SIE.2` recovers source meanings, `SIE.3` qualifies or develops model content for an integration use, and `SIE.4` supplies correspondences | generic terminology, ontology, formal science, and local modeling remain with their direct owners |
| A model needed for a receiving integration answer | `SIE.2`, `SIE.3`, `SIE.4`, `SIE.7`, and `SIE.10` apply when the model supplies a named semantic-integration result | local model construction and research remain outside SIE |
| Formal apparatus needed by a semantic mapping or validation | exact formal apparatus may become a source, mapping, or validation premise | formal modeling itself is not an SIE lifecycle |
| Connected engineering descriptions and changed lifecycle information | SIE can return a qualified semantic interface, mapping package, identity/claim result, or affected-use result | SYSE keeps engineering descriptions, configuration, release, assurance, and digital-thread decisions; Data Engineering keeps pipeline operation |

## FPF, neighboring practice, and authority boundaries {#fpf-neighboring-practice-and-authority-boundaries}

FPF owns generic representation, grounding, evidence, source/currentness, identity, comparison, and assurance distinctions. Method Engineering owns Method identity, qualification, trial, fit, worth, repertoire, variant, introduction, and revision. Systems Engineering owns engineered-System, engineering-description, configuration, integration, release, and assurance decisions. Data Engineering owns extraction execution, pipeline/service construction, orchestration, observability, reliability, and recovery. MDM and domain authorities own master identity, authoritative values, survivorship, and domain truth. Applications and operating or decision owners own authorization, risk acceptance, and actual outcomes.

SIE supplies Methods for use-qualified model content, cross-source meanings and correspondences, identity and claim composition, executable mappings, realization, interfaces, validation, changed semantic reliance, and modular commons. Return every non-SIE result to its owner with the exact dependent action.

## Representative case coverage {#representative-case-coverage}

The five applications are constructed method demonstrations, not evidence of a production integration, product release, recall decision, analytic validity, provider performance, or practical effectiveness.

| Case | What it tests | Boundary for reuse |
| --- | --- | --- |
| AP242/QIF | configuration/effectivity, feature identity, source-qualified composition, mapping, interface, and receiving-use validation | engineering and quality authorities retain release and acceptance; AP242 revision reopens affected premises |
| semiconductor traceability | several identifier schemes, grains, issuers, time, contradiction, and disclosure | MDM/domain and recall authorities retain identity, value, and action |
| quality/provenance | mapping coverage, units, defaults, derivation, currentness, and a representative analytic | Data Engineering and source owners repair their results; quality measures do not decide use alone |
| high-change providers | sufficient model reuse, explicit semantic difference, virtual realization, availability/error branches, changed promise horizon, and non-comparability | providers retain source meanings and permissions; purchasing owns action |
| equipment-classification commons | module boundaries, local correspondences, identification, decision and release rights, semantic change, migration, and notice | contacts communicate; source owners and receiving users retain their respective decisions |

## Edition return {#edition-return}

**Semantic Integration Engineering Principles Framework — First Edition, 20 September 2026** designates the source, twelve authoritative pattern bodies, and deterministic carrier of the complete twelve-pattern first edition. The publication supplies practitioner guidance and constructed examples. An implemented service, maintained commons, or receiving decision needs the corresponding actual work and evidence.

## Publication boundary {#publication-boundary}

This publication combines twelve authoritative pattern bodies with the shared reader account. The bodies govern their Methods; the Readme, Preface, applications, Table of Contents, and boundary account help readers find and combine them.

Use an instructional Guide for sequenced learning and memory formation. Use the Engineering DPF Suite Reference for cross-framework discovery. Neither publication replaces the pattern bodies or supplies a missing SIE result.
