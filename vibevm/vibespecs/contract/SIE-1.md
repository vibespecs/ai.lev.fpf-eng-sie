# SIE.1 - Bound the Receiving Use and Semantic Contract {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Eternal alpha
> **Normativity:** Normative method guidance within SIE; examples are constructed and non-normative.
>
> **Primary working result:** a `SemanticIntegrationUseContract@Use` that names one receiver and use, required answer claims, source cut, tolerated loss and uncertainty, currentness, latency, quality, authority, representative tests, stop conditions, and reopen conditions.

## SIE.1:1 - Problem Frame {#problem-frame}

**Use this when** a request says “integrate the data”, “align the models”, “build the knowledge graph”, or “make one source of truth”, but the intended receiver and decision-changing answer are not yet explicit. The recognizable failure is a technically impressive integration whose values cannot be interpreted, trusted, or used safely by the Work that requested it.

The primary EntityOfConcern is one semantic-integration use: a named receiver performing a named query, decision, operation, or engineering workflow under stated conditions. The first move is to state that use and the answer claims it needs. The first result is a bounded contract that lets later workers decide which semantic loss, source age, unresolved row, and test outcome are acceptable.

The practical gain is a testable stopping rule before source, ontology, mapping, or platform choices accumulate. Do not use this pattern to authorize the receiving decision, decide product configuration, choose master identity, operate a data pipeline, or define generic evidence law. Obtain those results from their owners. Do not reopen a current contract merely because another source exists; reopen it when the receiver, use, answer, conditions, authority, or acceptance boundary changes.

## SIE.1:2 - Problem {#problem}

Without a receiving-use contract, “semantic integration” expands toward every source and every possible reuse. Similar labels are merged without a loss budget, freshness is treated as an implementation detail, and a passing schema or sample query is reported as success. The project cannot distinguish an informative unmatched row from a defect, or a harmless delay from a stale answer that changes action.

Technology then supplies the hidden contract. A graph platform encourages graph-shaped outputs, a warehouse encourages copying, and an API encourages whichever fields are easiest to expose. None says which answer claims the receiver may rely on, who owns them, or when the correct result is to stop.

## SIE.1:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Breadth | More sources may enable future reuse, while every added source creates meanings, authority, currentness, and validation obligations. |
| Speed | A quick join can demonstrate access, while early conflation makes later correction expensive and hard to trace. |
| Loss | A useful common view often coarsens detail, while silent loss can reverse a decision or erase incompatibility. |
| Freshness and latency | Query-time access can be current but slow or fragile; copied data can be fast but stale and harder to govern. |
| Authority | Source owners, integrators, and receivers contribute different decisions; visibility or custody does not transfer authority. |
| Assurance | A finite representative test is needed now, while no test establishes universal semantic correctness. |
| Reuse | A broad contract appears reusable, while a small contract is easier to validate and honestly reopen. |

## SIE.1:4 - Solution {#solution}

Construct the smallest semantic contract that can change the named receiving action. Begin from the receiver and work backward to required answer claims, source contexts, meanings, losses, currentness, quality, authority, representative cases, and exact stops. Treat the contract as an input to later SIE patterns, not as proof that any source, correspondence, identity, mapping, interface, or implementation exists.

### SIE.1:4.1 - Pattern-Use Unfolding {#pattern-use-unfolding}

1. **Name the receiver and receiving Work.** Identify the System or role that will use the result, the query, decision, operation, or workflow, the horizon, and the first useful answer.
2. **State the answer claims.** Write the fields or propositions the receiver needs, including scope, grain, interval or effectivity, and the action each claim can change. Keep a value, its provenance, its authority, and the receiver's decision distinct.
3. **Select the source cut.** Name only the governed contexts and candidate source assets that can change the answer. Mark sources whose inclusion is uncertain rather than adding them silently.
4. **State preserved distinctions and tolerated loss.** Name identities, versions, units, codes, relations, claim scopes, and incompatibilities that must survive. For each permitted coarsening or omission, state why the receiver can tolerate it.
5. **State currentness, latency, availability, and quality conditions.** Choose thresholds or explicit unresolved returns only where they change use. Do not copy every available quality dimension into the contract.
6. **Recover authority, permission, and protection boundaries.** Name who defines source meanings, who may grant access, who decides identities or authoritative values, who accepts semantic loss, and who owns the receiving action. Record an exact blocker where a required relation is absent.
7. **Design representative tests before implementation.** Include at least one expected positive case, one negative or unmatched case, and one unlike or changed-source case that could defeat the proposed integration. Name the expected branch rather than requiring every test to return a value.
8. **State pass, narrow, unresolved, and stop outcomes.** A contract permits a bounded usable subset or explicit incompatibility when that is useful. Stop when a load-bearing meaning, source edition, identity authority, permission, or acceptance rule is unavailable.
9. **State reopen conditions and next result.** Identify observations that change the contract and the smallest next result, often `SourceSemanticInventory@Use` from `SIE.2`.

### SIE.1:4.2 - Record the Result {#record-the-result}

| Contract position | Required content |
| --- | --- |
| receiver and use | named receiver, Work, query/decision/operation/workflow, horizon, and first useful answer |
| answer claims | propositions or fields, grain, scope, interval/effectivity, and action changed |
| source cut | governed contexts, candidate assets, inclusion reason, and known access limits |
| semantic boundary | distinctions to preserve, permitted loss, uncertainty treatment, unmatched/incompatible behavior |
| service conditions | currentness, latency, availability, recovery, and quality thresholds that change use |
| authority and protection | meaning owner, identifier or value authority, access/permission, receiver authority, and protected conditions |
| validation | representative positive, negative, unlike/change cases and expected branches |
| disposition | pass, narrow, unresolved, or stop rules; next result and observable reopen conditions |

### SIE.1:4.3 - What Changes in Practice {#what-changes-in-practice}

The team stops treating integration scope as the set of reachable sources. Every later correspondence, identity disposition, mapping rule, realization, interface field, and validation claim must answer to a named receiving use and loss boundary. Explicitly unmatched or incompatible results become valid outcomes rather than defects to hide.

## SIE.1:7 - Conformance Checklist {#conformance-checklist}

- [ ] One named receiver and receiving Work are explicit.
- [ ] The first useful answer is expressed as claims or fields with grain, scope, and interval/effectivity.
- [ ] The source cut is justified by the use rather than by reachability.
- [ ] Preserved distinctions, permitted loss, uncertainty, and unmatched/incompatible behavior are explicit.
- [ ] Currentness, latency, availability, recovery, and quality are included only where action-changing.
- [ ] Meaning, identity/value, access, semantic-loss, and receiving-action authorities remain distinct.
- [ ] Positive, negative, and unlike or changed-source tests have expected branches.
- [ ] Pass, narrow, unresolved, stop, next-result, and reopen rules are stated.
- [ ] The contract claims no correspondence, implementation, validation, authorization, or outcome that has not been obtained.

## SIE.1:9 - Consequences {#consequences}

The contract limits source fan-out, makes semantic loss and authority visible, and gives implementation and validation a shared target. It can stop an integration before expensive model or platform work. It also makes conflicts and narrow usable subsets publishable outcomes.

The cost is early negotiation about the receiver, evidence, loss, and stop conditions. Some attractive future reuse remains outside the first package and must earn its own contract or compatible extension.

## SIE.1:12 - Relations {#relations}

- `SIE.2` consumes the source cut, answer claims, distinctions, and currentness questions to produce `SourceSemanticInventory@Use`.
- `SIE.4`–`SIE.10` consume the compatible contract positions relevant to their results; none may silently widen the receiver or accepted loss.
- `C.37` governs generic use-bounded representation selection. `A.10` and `A.10.1` govern evidence/provenance and generic affected-use questions.
- Applications, Systems Engineering, Operations, quality, safety, legal, and other direct owners supply their acceptance and authority results.
- A changed contract reopens the package branches that rely on the changed premise. `SIE.11` supplies affected-use discovery and integration revalidation where the affected results still need to be established.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): FPF spec://ai.lev/fpf-spec/contract/C-37#root; spec://ai.lev/fpf-eng-me/contract/ME-3#root; direct receiver and source-owner results @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-sie/contract/SIE-10#root, spec://ai.lev/fpf-eng-sie/contract/SIE-2#root, spec://ai.lev/fpf-eng-sie/contract/SIE-3#root, spec://ai.lev/fpf-eng-sie/contract/SIE-8#root, spec://ai.lev/fpf-eng-sie/contract/SIE-9#root @status:spec/done

#source spec://ai.lev/fpf-eng-sie/source/SIE-1
