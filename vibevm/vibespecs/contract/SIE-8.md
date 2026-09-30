# SIE.8 - Choose Virtual, Materialized, or Hybrid Semantic Realization {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Eternal alpha
> **Normativity:** Normative method guidance within SIE; examples are constructed and non-normative.
>
> **Primary working result:** a `SemanticRealizationDecision@Use`: a supported choice, sufficient rejection, worthwhile probe, or missing-input result for a named semantic-integration use. A positive choice identifies the implementation results it still requires.

## SIE.8:1 - Problem Frame {#problem-frame}

**Use this when** accepted semantic mappings exist and the current question is whether to evaluate them at query time, persist integrated results, or combine both. Enter also when a graph database, warehouse, federation, cache, search index, API composition, or “virtual knowledge graph” has already been proposed and its semantic consequences need comparison.

The primary EntityOfConcern is one realization decision for a named semantic-integration use. The first move is to derive realization-sensitive criteria from the use contract and mapping specification. The first result is a bounded choice, probe, rejection, or missing-input return that leaves physical implementation and operation with their owners.

The payoff is a realization selected because it preserves the required meanings and service conditions, not because one carrier is fashionable or already available. Do not use SIE.8 to build, deploy, or operate a data service, select a whole enterprise platform, authorize access, or prove that the interface works. Data Engineering, platform, security, provider, finance, and other direct owners supply those results.

## SIE.8:2 - Problem {#problem}

Materialization can improve latency and independence from source availability but creates copied state, invalidation, custody, storage, and refresh obligations. Virtual access can preserve source currency and authority but inherits source latency, availability, access, and query-capability limits. A hybrid can isolate hot or stable subsets but adds coherence and branch complexity.

When the choice is made from technology labels, these consequences remain hidden until operation. A copied graph is described as semantic truth, a federation as automatically current, or a cache as harmless optimization. The same mapping semantics can yield different provenance, currentness, error, and recovery behavior in each realization.

## SIE.8:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Freshness | Virtual reads can observe current source state, while network and source delays can still make answers stale or inconsistent. |
| Latency | Materialization and caching can respond quickly, while refresh and invalidation may violate the use's time boundary. |
| Availability | Copies can survive source outages, while they can conceal that authority or access conditions changed. |
| Source authority | Querying the source keeps custody visible, while a receiver may need stable snapshots and reproducible answers. |
| Security and permission | Fewer copies reduce exposure, while live federation can broaden runtime credentials and cross-source disclosure. |
| Provenance and reproducibility | Materialized snapshots aid replay, while virtual results need captured queries, source versions, and occurrence metadata. |
| Operability and recovery | A simpler runtime can reduce failure modes, while hybrid arrangements add invalidation and coherence responsibilities. |
| Cost | Storage, compute, licenses, egress, support, and provider dependency trade differently across cases. |

## SIE.8:4 - Solution {#solution}

First use decisive conditions to exclude arrangements that cannot serve the contract. Describe and compare the serious remaining alternatives as complete arrangements, including source access, rule execution, state/copy behavior, provenance, currentness, failure branches, security, operation, recovery, exit, and joint resource demand. Return a supported choice, sufficient rejection, worthwhile probe, or missing-input result for the named use.

### SIE.8:4.1 - Pattern-Use Unfolding {#pattern-use-unfolding}

1. **Fix the receiving result.** Reference the `SIE.1` answer, `SIE.7` rules, required source/identity/claim branches, and validation conditions that a successful candidate must preserve.
2. **Apply decisive exclusions.** A known source prohibition or other sufficient condition can defeat an arrangement. Record the condition and evidence needed for that conclusion and stop developing the excluded alternative. If no serious candidate remains, return the bounded rejection or the exact missing result.
3. **Describe a serious virtual alternative.** When query-time access remains a candidate, state source access, rule evaluation, pushdown or mediation, credentials, latency/availability behavior, provenance capture, and failure return.
4. **Describe a serious materialized alternative.** When copying remains a candidate, state copied or derived state, snapshot identity, refresh/invalidation, storage and custody, source deletion/correction behavior, provenance, recovery, and exit.
5. **Describe a hybrid where warranted.** Identify which permitted subset is materialized and which source-sensitive part remains virtual. State coherence, invalidation, and fallback behavior. Confirm permission for each subset selected for copying.
6. **Compare complete remaining arrangements.** Use the conditions that can change the receiving result: freshness, latency, availability, access, protection, source authority, reproducibility, provenance, operability, recovery, cost, and semantic loss. Include concurrent source calls, shared credentials, trace, retries, support, and other demands within each applicable resource envelope. Pairwise feasibility cannot establish a jointly infeasible arrangement.
7. **Examine relevant failure and change cases.** Use the source outages, corrections, access changes, mapping changes, stale or partial refresh, provenance loss, and recovery cases needed for the proposed conclusion. Earlier sufficient evidence can support a bounded rejection; a positive selection needs its load-bearing conditions.
8. **Choose or identify worthwhile further work.** Select a supported arrangement, reject it, or return the missing result. Commission a discriminating probe only when its obtainable result can change the decision enough to justify its full burden and displaced work. Keep an unresolved comparison explicit when further inquiry is unavailable or not worthwhile. State the reasons for the disposition that its receiver needs.
9. **Name implementation returns for a selected choice.** Identify the Data Engineering, platform, provider, security, legal, finance, or operating results required to realize that choice.
10. **Return the conditions needed by this result.** For a selected realization or supplied receiving result, give `SIE.9` its service, error, currentness, and fallback meanings. Retain observations that can reopen the conclusion where they change continued reliance.

### SIE.8:4.2 - Record the Result {#record-the-result}

The result follows the conclusion actually supplied. A sufficient rejection of one proposed arrangement is complete with the receiving use, named proposal, decisive grounds and evidence, scope, and material limits. It does not require a comparison with unrequested alternatives or an implementation and interface design. Unused positions create no empty fields, waivers, or explanations of omission.

| Decision content | When it is needed | Content supplied |
| --- | --- | --- |
| Receiving use and disposition | Every result | The question and proposed arrangement or comparison scope, supported choice/rejection/probe/missing-input result, grounds, and material limits. |
| Decisive exclusion | A proposed arrangement is rejected on sufficient grounds | The condition that defeats it, the evidence and applicability needed for that condition, and the scope of the rejection. |
| Candidate arrangements and comparison | A comparison remains live or a positive choice is made | Serious remaining alternatives as complete arrangements: required semantic branches, access, state, execution, currentness, latency, provenance, protection, failure, operation, recovery, exit, and joint resource demand. |
| Failure/change evidence | The supplied conclusion depends on it | Evidence for its load-bearing conditions. One qualified prohibition can suffice for rejection; positive selection needs the relevant failure and change cases for the claimed arrangement. |
| Further inquiry | A probe is proposed | Obtainability, possible decision contribution, full burden, displaced work, and how its result can change the decision. |
| Implementation returns | A realization has been selected | Exact required direct-owner results, what is supplied or still missing, and the acceptance evidence needed to realize that choice. |
| Interface semantics | A selected realization or receiving result needs them | Currentness, source/error, incomplete-result and fallback meanings supplied to SIE.9. |
| Continued reliance | A condition can materially change the result's use | The observation, source change, or receiving change that reopens the affected decision. |

A positive choice cannot use the rejection boundary to omit a condition on which that choice relies. The selected arrangement and its implementation returns remain qualified by all their actual semantic, service, access, and resource conditions.

### SIE.8:4.3 - What Changes in Practice {#what-changes-in-practice}

The team compares ways to supply the same semantic result rather than comparing product categories. A graph store may survive as a materialized candidate, a federation as a virtual candidate, or neither. The selected decision states what still has to be implemented and operated before any service claim is made.

## SIE.8:7 - Conformance Checklist {#conformance-checklist}

Check the conclusion being returned. Only its applicable checks need an answer; unused branches require neither a record nor an omission explanation.

**For every result**

- [ ] The receiving question, named proposal or comparison scope, disposition, grounds, and material limits are recoverable.
- [ ] The evidence supports that disposition at its stated scope; it creates no broader feasibility, running-service, or achieved-performance claim.

**For a sufficient rejection**

- [ ] The decisive condition and its qualified evidence defeat the named proposal for this use.

That rejection completes the Method when it answers the requested question. The following comparison and implementation checks do not become prerequisites for it.

**For a live comparison or positive selection**

- [ ] A successful candidate preserves the receiving result, mapping rules, and required semantic branches.
- [ ] Serious remaining candidates expose access, state, execution, provenance, failure, operation, recovery, exit, and joint resource demand.
- [ ] Freshness and latency are defined for the receiving use.
- [ ] Source authority, custody, permissions, correction/deletion, and retention consequences are explicit.
- [ ] Security/privacy and runtime credential differences are compared where they can change the result.
- [ ] Reproducibility and provenance behavior are specified for the candidate's virtual occurrences and copied state.
- [ ] Relevant outage, access, mapping, correction, refresh, provenance-loss, and recovery cases support the proposed conclusion.
- [ ] For a selected realization, exact implementation and operating results remain with their direct owners, and SIE.9 receives the required currentness, error, incomplete-result, and fallback meanings.

**For a proposed inquiry**

- [ ] Its obtainable decision contribution justifies the full burden and displaced work.

## SIE.8:9 - Consequences {#consequences}

The realization becomes a reversible bounded decision with visible source, semantic, and operating trade-offs. Interface designers receive explicit currentness and error behavior, while implementers receive a clear invariant to preserve.

The cost is comparison beyond the preferred platform and coordination with operational owners. A selected candidate may still stop because access, security, service, provider, or cost evidence is missing.

## SIE.8:12 - Relations {#relations}

- `SIE.1` supplies the invariant result and use-sensitive service and protection conditions.
- `SIE.7` supplies executable semantic behavior and loss/error branches every candidate must preserve.
- `SIE.2`, `SIE.5`, and `SIE.6` supply source authority, identity, claim, provenance, and currentness conditions.
- `SIE.9` consumes the selected realization's currentness, latency, availability, provenance, error, access, and fallback semantics.
- `SIE.10` tests the realized candidate and receiving workflow; it can narrow or fail the decision's assumed conditions.
- Data Engineering, platform, provider, security, legal, finance, and Operations owners supply implementation and operating results.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-eng-sie/contract/SIE-1#root, spec://ai.lev/fpf-eng-sie/contract/SIE-7#root; direct Data Engineering, platform, provider, and protection results @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-sie/contract/SIE-9#root @status:spec/done

#source spec://ai.lev/fpf-eng-sie/source/SIE-8
