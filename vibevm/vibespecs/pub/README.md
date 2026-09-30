# Semantic Integration Engineering Principles Framework Readme {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Readme section of the publication. See LICENSE.md for the list of changes.

## Practical entries {#practical-entries}

Start from the query, decision, or operation that needs a cross-source answer. The constructed connections below show how meanings, identity, executable rules, and receiving use constrain one another. They are selected examples, not a catalogue or a required sequence. Reuse supplied results when their use and conditions still match; open the [Table of Contents](spec://ai.lev/fpf-eng-sie/pub/TOC#root) for another question or the [pattern-selection guide](spec://ai.lev/fpf-eng-sie/pub/framework-boundary-and-refresh#pattern-selection-and-first-returned-result) for a missing result.

The [Preface](spec://ai.lev/fpf-eng-sie/pub/PREFACE#root) explains the repertoire and its [architectural rationale](spec://ai.lev/fpf-eng-sie/pub/PREFACE#preface-7). You can ask an assisting agent: “Explain this and give me your comments in the language of my work, without framework jargon.”

### SIE-INSPECTION - Connect inspection evidence to the configured product {#sie-inspection-connect-inspection-evidence-to-the-configured}

- **Situation:** Product-definition and inspection sources are accessible, but a quality engineer cannot tell which inspection result concerns the feature in the configuration being reviewed.
- **Question:** How can the receiving query return applicable evidence and expose the branches it cannot establish?
- **First useful result or blocker:** The required answer for a named feature, configuration, and effectivity, with the permitted incomplete branches; or the missing configuration or acceptance decision that prevents bounding that answer.
- **Start with:** [SIE.1](spec://ai.lev/fpf-eng-sie/contract/SIE-1#root) when the receiving question is unsettled; [SIE.10](spec://ai.lev/fpf-eng-sie/contract/SIE-10#root) when an existing result already fails that question.
- **Stop or return:** Stop a dependent branch on unresolved feature identity or configuration. Return a source-definition gap to its owner, a transformation defect to SIE.7, and the release or inspection-acceptance decision to the engineering or quality authority.

In [APP-SIE-01](spec://ai.lev/fpf-eng-sie/pub/cross-pattern-application#app-sie-01-ap242-and-qif-product-lifecycle-query), the engineer asks for the QIF plan and result concerning feature `F` in released revision/configuration `R` at effectivity `E`. SIE.1 makes those inputs and the acceptable answer branches explicit. [SIE.2](spec://ai.lev/fpf-eng-sie/contract/SIE-2#root) then supplies the source editions, local definitions, identifier schemes, and authority needed to interpret them. If the available model cannot distinguish a planned inspection from an observation of that configured feature, [SIE.3](spec://ai.lev/fpf-eng-sie/contract/SIE-3#root) develops that missing distinction and tests it against those cases. An adequate existing model can be reused.

Those meanings allow [SIE.4](spec://ai.lev/fpf-eng-sie/contract/SIE-4#root) to state a directed relation: inspection characteristic `C-17` concerns product feature `F-17` under the plan and configuration. [SIE.5](spec://ai.lev/fpf-eng-sie/contract/SIE-5#root) qualifies the feature endpoint at the required grain and effectivity. The relation permits navigation between the records; it does not make a characteristic identical to a product feature. A shared label without the supporting plan and effectivity remains an unmatched candidate. [SIE.6](spec://ai.lev/fpf-eng-sie/contract/SIE-6#root) uses these premises to combine definition, plan, and observation claims while retaining their sources and any conflict.

[SIE.7](spec://ai.lev/fpf-eng-sie/contract/SIE-7#root) turns the accepted relations into selection and transformation rules. The rules select the supplied released configuration, preserve both source identifiers, and expose an unknown unit or unmatched feature. [SIE.8](spec://ai.lev/fpf-eng-sie/contract/SIE-8#root) uses those required behaviours when comparing ways to supply the result; [SIE.9](spec://ai.lev/fpf-eng-sie/contract/SIE-9#root) makes their meanings, timestamps, provenance, and failure branches available in the engineer's query.

The constructed application permits a qualified row set with unresolved local-extension and unknown-unit branches shown separately. SIE.10 can support that narrower answer only with matching evidence for all premises on which it relies, including the engineer's interpretation. A different question can finish much earlier: if a conversion returns 1 millimetre from an input of 1 metre where 1000 millimetres is required, that case establishes the mapping failure and returns it to SIE.7; unrelated layers remain unexamined. When the released configuration changes, [SIE.11](spec://ai.lev/fpf-eng-sie/contract/SIE-11#root) follows the changed applicability through the relied-on identity, mapping, and receiving tests. The query supplies evidence; the responsible authorities still decide release and acceptance.

### SIE-PROVIDERS - Compare live availability under semantic and access limits {#sie-providers-compare-live-availability-under-semantic-and}

- **Situation:** Two provider APIs both expose an availability number, but their quantities and copying permissions differ from what a purchasing comparison assumes.
- **Question:** Which qualified answer can the interface supply within the receiving and access conditions?
- **First useful result or blocker:** Separately attributed quantities with the conditions needed for comparison, or a semantic or access limit that defeats the proposed answer.
- **Start with:** [SIE.2](spec://ai.lev/fpf-eng-sie/contract/SIE-2#root) and [SIE.6](spec://ai.lev/fpf-eng-sie/contract/SIE-6#root) for unsettled meanings and comparison; [SIE.8](spec://ai.lev/fpf-eng-sie/contract/SIE-8#root) when those premises are supplied and realization is the remaining question.
- **Stop or return:** Exclude prohibited copying. Return an infeasible complete answer for a permitted narrower result or an access-owner decision. Reopen the affected meaning and interface when a provider changes the quantity it reports.

In the constructed provider case of [APP-SIE-04](spec://ai.lev/fpf-eng-sie/pub/cross-pattern-application#app-sie-04-high-change-provider-availability-without-a) and SIE.6, Provider A reports 12 on hand and Provider B reports 9 available to promise. SIE.2 recovers the reservation and horizon rules behind the quantities. [SIE.3](spec://ai.lev/fpf-eng-sie/contract/SIE-3#root) can reuse a model that keeps both measures, providers, units, times, and horizons distinct. [SIE.4](spec://ai.lev/fpf-eng-sie/contract/SIE-4#root) supplies the qualified product-family relation. SIE.6 retains separate provider claims: the numbers do not support a common “21 available” total. For the question “Who can supply 8 now?”, A's reservation check and B's promise horizon must also support the receiving use.

Both providers prohibit replication. That prohibition is sufficient for SIE.8 to reject a copied availability store. If the question asks which remaining arrangement to use, compare query-time retrieval and any permitted hybrid with their latency, provenance, failure behaviour, and common resource demands. Develop only serious remaining alternatives. Obtain further evidence when its possible contribution to the choice justifies the burden and displaced work.

The [shared-request example](spec://ai.lev/fpf-eng-sie/pub/PREFACE#sie-preface-6-1-a-shared-request-limit-changes-the-provider) assumes four calls for A, four for B, and three for the required common trace, all under one ten-call allowance. The complete answer needs eleven calls before retries. With permission for an incomplete answer, A plus the trace needs seven: [SIE.9](spec://ai.lev/fpf-eng-sie/contract/SIE-9#root) can expose “12 on hand at T” and “B not retrieved”, retaining the source and rule trace. B has not reported zero. SIE.10 still checks the other conditions needed for that narrower use; if both providers are mandatory, the result is a stop until the allowance or call demand is changed on supported grounds.

Suppose B keeps the same JSON field but changes its promise horizon. [SIE.11](spec://ai.lev/fpf-eng-sie/contract/SIE-11#root) compares the meanings and finds the uses that consume them. An “available now” view returns to claim composition, mapping, interface, and receiving-use validation; a future-planning view may accept the new horizon after checking its own conditions. Product descriptions whose meanings are independent of that quantity can keep their earlier qualification. An inaccessible consumer interpretation remains unresolved. Purchasing decides how to act on the qualified or incomplete answer.

### SIE-COMMONS - Govern shared semantic modules {#sie-commons-govern-shared-semantic-modules}

- **Situation:** Several organizations use a shared classification, and a proposed improvement would change which objects belong to one of its classes.
- **Question:** How can the shared model evolve while each consumer can still identify the meaning its work needs?
- **First useful result or blocker:** The proposed distinction and the users whose questions depend on it, or an unresolved definition or decision right that prevents the change.
- **Start with:** [SIE.12](spec://ai.lev/fpf-eng-sie/contract/SIE-12#root), with [SIE.3](spec://ai.lev/fpf-eng-sie/contract/SIE-3#root) for changed model content and [SIE.11](spec://ai.lev/fpf-eng-sie/contract/SIE-11#root) for actual consumer reliance.
- **Stop or return:** Keep incompatible criteria in scoped modules when their users need them. A pair needing only one interface can complete that agreement; shared-module governance is useful when independently maintained modules and users create that further need.

In [APP-SIE-05](spec://ai.lev/fpf-eng-sie/pub/cross-pattern-application#app-sie-05-a-modular-equipment-classification-commons), two manufacturers and a service partner share equipment classes. A proposal replaces “equipment with a replaceable drive” with “equipment serviced through a replaceable drive module”. Equipment X has only a separately replaceable drive; Y also supports drive-module replacement. These cases expose the changed classification: X belongs to the earlier class but not the proposed one, while Y belongs to both.

SIE.3 uses those cases to make the meanings distinguishable. Under the constructed SIE.12 agreement, the authorized maintainers keep `equip:DriveReplaceable` for the earlier meaning and introduce `equip:DriveModuleServiceable` for the new one. Both definitions and their editions remain recoverable. Source owners continue to supply the product descriptions on which membership depends.

SIE.11 follows each consumer's question. The service partner adopts the new class for module-replacement planning, so [SIE.4](spec://ai.lev/fpf-eng-sie/contract/SIE-4#root) revisits its correspondences and the query uses the revised relation. [SIE.10](spec://ai.lev/fpf-eng-sie/contract/SIE-10#root) checks the integration premises, including the result that admits Y and excludes X. Manufacturer A still needs its spare-drive query under the earlier meaning and can retain matching evidence. The release supplies the access, dependencies, migration information, and notice those uses need. These two completed outcomes leave other consumers' migration to be established where it matters.

## Citation {#citation}

If you use this edition, cite:

```text
Anatoly Levenchuk, with AI-assisted development and review.
Semantic Integration Engineering Principles Framework.
20 September 2026. First edition.
GitHub repository: https://github.com/ailev/FPF
```

For a particular pattern, add its PatternID and title. Retain the edition designation and date, and include a permanent link or stored copy when exact wording matters.
