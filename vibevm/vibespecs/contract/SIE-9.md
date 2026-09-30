# SIE.9 - Connect a Receiving Use through a Semantic Interface {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Eternal alpha
> **Normativity:** Normative method guidance within SIE; examples are constructed and non-normative.
>
> **Primary working result:** a `ReceivingSemanticInterface@Use` defining the smallest query, view, API, message, schema, report, or other boundary that carries the required meanings and branches to the receiver with interpretation, source and provenance, currentness, accepted loss, access assumptions, errors, unresolved returns, and a path back to the owning source or decision.

## SIE.9:1 - Problem Frame {#problem-frame}

**Use this when** semantic mappings or integrated state exist but the receiving Work still cannot obtain, interpret, challenge, or return the bounded result. Enter when a technically reachable endpoint hides source meanings, currentness, unmatched rows, conflicts, or the difference between “no value” and “source unavailable”.

The primary EntityOfConcern is one semantic interface between the maintained integration arrangement and a named receiving use. The first move is to restate the receiver's action and select the smallest interaction and result form that carries every load-bearing semantic branch. The first result is an interface contract and supplied candidate interface, not a claim that the receiver is authorized or that the service is operationally adequate.

The payoff is a boundary at which semantic meaning, failure, and provenance are usable by ordinary Work. Do not use SIE.9 to design the application's whole user experience, make its decision, operate the service, or accept engineering/quality results. Those owners consume the interface under their own Methods and authority. Stop rather than return a positive interface when a required semantic branch, interpretation, provenance/currentness condition, source-return path, or receiver-side use test cannot be represented or traced.

## SIE.9:2 - Problem {#problem}

Integrated data can remain unusable because the receiver cannot ask the relevant question or distinguish the answer's conditions. An API may omit source edition and effectivity; a report may list a fused value without conflict; a schema may use one null for unknown, not applicable, stale, and timeout; a user may have no path to challenge an identity or mapping premise.

When the interface is treated as transport only, semantic obligations remain in internal documentation. The receiving Work either overtrusts the result or reconstructs meanings informally, creating a second uncontrolled integration at the boundary.

## SIE.9:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Minimality | A small interface is easier to use and maintain, while hiding source, loss, or failure makes it unsafe. |
| Human and machine use | Machines need stable schemas and branch codes; people need interpretations and challenge paths. |
| Abstraction | Receiver-friendly names reduce burden, while source identifiers and exact meanings must remain recoverable. |
| Performance | Rich provenance and alternative claims cost bandwidth and attention, while omitted trace defeats challenge and validation. |
| Security | The receiver needs enough source information to rely, while disclosure can violate provider, privacy, or protection conditions. |
| Evolution | Stable interface promises aid use, while source or mapping changes must not be hidden behind unchanged field names. |

## SIE.9:4 - Solution {#solution}

Design the interface from receiving actions and semantic branches, not from the internal store. Expose the smallest result that preserves interpretation, source/version, currentness, accepted loss, identity and claim status, provenance, access assumptions, errors, unresolved returns, and source-return paths. Bind every field and branch to the use contract, mapping rules, and selected realization.

### SIE.9:4.1 - Pattern-Use Unfolding {#pattern-use-unfolding}

1. **Name the receiver interaction.** State who or what asks, the query/message/report action, timing, input parameters, and the next Work or decision that consumes the answer.
2. **Select the interface form.** Choose query, view, API, message, schema, report, file, or mixed human/machine form based on the receiving Work. Do not inherit the internal realization shape automatically.
3. **Define semantic inputs.** State required identifiers, schemes, configuration/effectivity, time windows, units, locale or code context, permissions, and validation of requests.
4. **Define result claims and interpretation.** For each output, state meaning, grain, scope, interval/effectivity, units/codes, source identifier behavior, accepted loss, and permitted use.
5. **Expose qualified branches.** Represent matched/qualified, unmatched, incompatible, unresolved identity, source-qualified conflict, non-comparability, stale, inaccessible, timeout/source error, and partial result where applicable.
6. **Expose provenance and currentness.** Provide source/edition or a stable reference, observation/retrieval time, mapping/composition rule version, derivation/trace reference, and freshness status needed by the receiver.
7. **State access, protection, and authority assumptions.** Explain what the interface verifies, what the caller supplies, what may be disclosed, and which actions remain unauthorized by the semantic result.
8. **Provide challenge and return paths.** A receiver must be able to identify the source, correspondence, identity, composition, mapping, or operational result that owns a defect or unresolved branch.
9. **Bind service behavior without claiming it.** State latency, availability, pagination/volume, ordering, idempotence or snapshot expectations only where semantic use depends on them; obtain implementation/operation evidence separately.
10. **Define conformance and reopen.** Give representative requests, responses, error branches, compatibility conditions, deprecation/change behavior, and observations that reopen the interface.

### SIE.9:4.2 - Record the Result {#record-the-result}

| Interface position | Required content |
| --- | --- |
| receiver interaction | caller/reader, receiving Work, request, timing, next action |
| interface form | query/view/API/message/schema/report/file and why it fits the Work |
| request semantics | parameters, identifiers/schemes, configuration/effectivity, windows, units/codes, permissions |
| response semantics | claims, grain, scope, interval, units/codes, source IDs, accepted loss, permitted use |
| branch model | qualified, unmatched, incompatible, unresolved identity, conflict, non-comparable, stale, inaccessible, source error, partial |
| provenance/currentness | source/edition, times, rule versions, derivation/trace, freshness status |
| protection/authority | verified and assumed conditions, disclosure limits, action not authorized |
| challenge/return | stable path to source, semantic premise, mapping, implementation, or direct decision owner |
| service/conformance | action-sensitive service conditions, examples, errors, compatibility/deprecation, reopen |

### SIE.9:4.3 - What Changes in Practice {#what-changes-in-practice}

The receiver no longer has to infer semantic meaning from field names or call the integration team to understand a missing row. Qualified, incompatible, conflicting, stale, and source-error states become part of the normal interface contract, and every challenge can be returned to a specific premise or owner.

## SIE.9:7 - Conformance Checklist {#conformance-checklist}

- [ ] The interface is tied to one named receiver, Work, request, and next action.
- [ ] The form is chosen for receiving use rather than copied from internal realization.
- [ ] Request identifiers, schemes, configuration/effectivity, windows, units/codes, and permissions are explicit.
- [ ] Response claims state meaning, grain, scope, interval, source identifiers, loss, and permitted use.
- [ ] Qualified, unmatched, incompatible, unresolved identity, conflict, non-comparability, stale, inaccessible, source-error, and partial branches remain distinguishable where applicable.
- [ ] Source/edition, observation/retrieval time, rule versions, derivation/trace, and freshness are recoverable.
- [ ] Protection, disclosure, and authority assumptions are explicit; the interface grants no unstated authorization.
- [ ] The receiver can return a defect or gap to a specific source, semantic premise, mapping, implementation, or decision owner.
- [ ] Action-sensitive latency, availability, snapshot, and volume behavior are stated without claiming unobserved performance.
- [ ] Representative requests, responses, errors, compatibility/deprecation behavior, and reopen conditions are present.

## SIE.9:9 - Consequences {#consequences}

The semantic arrangement becomes directly usable and challengeable. Receivers can distinguish a negative semantic result from an operational failure, and implementations can evolve behind a stable bounded contract while preserving source and rule trace.

The cost is a richer branch model and deliberate presentation of uncertainty and provenance. Some internal schemas or protocols must be wrapped rather than exposed directly.

## SIE.9:12 - Relations {#relations}

- `SIE.1` supplies the receiving action, answer claims, loss, service conditions, tests, and authority boundary.
- `SIE.2` supplies source meanings, identifiers, editions, access, provenance, and currentness.
- `SIE.4`–`SIE.7` supply correspondence, identity, composition, and executable mapping references and branches.
- `SIE.8` supplies selected realization, service assumptions, fallback, and missing implementation results.
- `SIE.10` validates the candidate interface and representative receiving workflow.
- Applications and direct professional owners retain authorization, risk acceptance, and actual outcomes; Data Engineering and Operations retain service execution.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-eng-sie/contract/SIE-1#root, spec://ai.lev/fpf-eng-sie/contract/SIE-7#root, spec://ai.lev/fpf-eng-sie/contract/SIE-8#root; conditional SIE.4-SIE.6 results @status:spec/done

#source spec://ai.lev/fpf-eng-sie/source/SIE-9
