# SIE.10 - Validate a Semantic Integration Result for Its Receiving Use {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Eternal alpha
> **Normativity:** Normative method guidance within SIE; examples are constructed and non-normative.
>
> **Primary working result:** a `SemanticIntegrationValidationAccount@Use` that supports a bounded pass, narrow, unresolved, or stop conclusion with appropriate evidence and reopen conditions. A positive receiving-use claim covers all of its load-bearing obligations.

## SIE.10:1 - Problem Frame {#problem-frame}

**Use this when** a candidate semantic interface or mapping package exists and somebody asks whether it is ready, correct, valid, trustworthy, or fit for use. Enter especially when one test family already passes and is being used as evidence for the whole: valid JSON, conforming RDF shapes, successful ETL, high matcher score, complete provenance, good data-quality metrics, or one successful demonstration.

The primary EntityOfConcern is one semantic-integration result under one receiving-use contract and one inspectable package revision. The first move is to identify the receiving claim being judged and whether known evidence already settles a bounded failure or unresolved result. For a positive claim, identify its load-bearing obligations and the evidence that can test them. The first result can be a supported local failure, scoped uncertainty, or qualified positive use.

The payoff is a truthful decision boundary: the receiver knows which result may be relied on, under which source editions and conditions, and which gaps remain. Do not use SIE.10 to authorize product release, accept a quality result, approve a recall, certify a service, or prove business effectiveness. Direct owners consume the bounded validation account and make those decisions.

## SIE.10:2 - Problem {#problem}

Semantic integrations fail across several independent layers. A carrier can be well formed while meanings are wrong; correspondences can be defensible while transformation code violates them; identity rows can pass while claim conflicts are flattened; provenance can be complete while source claims are stale or false; quality dimensions can look good while the representative workflow receives the wrong answer.

One aggregate “quality” or “confidence” score hides which premise failed and what must reopen. It also encourages compensating a hard stop, such as unresolved identity or unauthorized source use, with strong results elsewhere.

## SIE.10:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Layering | Separate tests localize defects, while the receiver needs a whole-use conclusion. |
| Positive evidence | Expected matches demonstrate a path, while negative and unlike cases reveal hidden compression and defaults. |
| Coverage | A positive use claim needs its load-bearing premises supported, while a bounded failure can be settled by sufficient defect evidence. |
| Automation | Schemas, shapes, queries, and metrics scale checks, while semantic and authority judgments often require qualified human/domain input. |
| Change | Stable evidence is reusable, while source editions, rules, interfaces, and receiving conditions can invalidate only some results. |
| Decision pressure | Stakeholders want pass/fail, while narrow or unresolved can be the most useful truthful disposition. |

## SIE.10:4 - Solution {#solution}

Choose the conclusion at its actual scope. A known decisive failure or bounded unresolved premise can finish with sufficient evidence for that result. For a positive whole-use or contract-permitted narrower result, obtain matching evidence for every load-bearing premise, including the receiver's interpretation. Use earlier results when their conditions still match. Preserve hard stops and distinguish unexamined premises from passing ones.

### SIE.10:4.1 - Pattern-Use Unfolding {#pattern-use-unfolding}

Steps 3–10 locate evidence for a positive use conclusion. A sufficient bounded failure or unresolved result can finish at step 2. Reuse matching earlier results for the applicable layers; a changed receiving interpretation can reopen a claim even when its carrier is unchanged.

1. **Identify the validation subject.** Name the mapping, interface, or package result and receiving use being judged. Record the revisions and conditions on which the conclusion depends.
2. **Choose the conclusion and inspect known evidence.** Take the relevant answer claim and stop condition from `SIE.1`. If a demonstrated defect already defeats it, return that bounded failure with sufficient evidence. If a necessary premise is unresolved and that settles the requested question, return the scoped gap. Further obligations remain unexamined. For a positive claim, derive all load-bearing distinctions, loss, currentness/service/quality, authority, protection, branch, and representative-use obligations.
3. **Validate carrier and schema.** Test parseability, declared schemas/shapes, required fields, datatypes, cardinalities, identifiers, and branch encodings. Treat a pass as structural only.
4. **Validate semantic-model and endpoint adequacy.** Test whether source and target concepts, types, relations, constraints, units/codes, and any supplied model express the required distinctions and examples/counterexamples.
5. **Validate correspondences and mappings.** Challenge accepted `SIE.4` rows and execute `SIE.7` positive, boundary, negative, and unlike examples. Check selection, cardinality, conversion, defaults, errors, loss, and trace independently.
6. **Validate identity and authority.** Test every load-bearing `SIE.5` disposition at its grain and interval, including issuer, version, part-whole, reuse, split/merge, and unresolved branches. Verify required authority and permission inputs rather than inferring them from data access.
7. **Validate claim composition.** Test `SIE.6` comparability, conflict, non-comparability, supersession, incomplete-source, and uncertainty branches. Confirm that source claims and derivation remain recoverable.
8. **Validate realization and interface behavior.** Test currentness, latency, availability, snapshot/caching, invalidation, source failure, partial results, access/protection, provenance, error semantics, and challenge paths required by `SIE.8` and `SIE.9`.
9. **Validate provenance, currentness, and quality.** Check that every relied-on output can recover its source and rule premises, that source/version/time status satisfies the use, and that selected quality measurements meet their action-changing thresholds. Do not treat provenance or process conformance as truth.
10. **Replay representative receiving Work.** Run the named query, decision preparation, operation, or engineering workflow with expected positive, negative, and unlike cases. Observe whether the receiver obtains and interprets the required result and stops on forbidden branches.
11. **Assign dispositions at the supported scope.** Use pass, narrow, unresolved, or stop for tested claims, and preserve any material unexamined reach. A positive narrow result states the contract-permitted subset and covers all of that subset's load-bearing premises; excluded branches remain explicit. A hard stop cannot be offset by scores elsewhere.
12. **Record repairs, returns, and reopen.** Send source, semantic, mapping, implementation, authority, or receiver defects to their direct owners; state which layer and consumers require retest after change.

### SIE.10:4.2 - Record the Result {#record-the-result}

| Validation position | Required content |
| --- | --- |
| subject and use | package/interface revision, source/rule versions, realization/test state, receiver and use |
| obligations | premises relevant to the claimed conclusion; all load-bearing contract obligations for a positive use claim |
| layer result | layer, tested claim, method/case, evidence, expected/observed result, pass/narrow/unresolved/stop, defect owner |
| dependency | exact source, correspondence, identity, composition, mapping, realization or interface premise consumed |
| coverage | examined cases and matching earlier results; material unexamined or unresolved premises, distinguished from passing ones |
| use disposition | supported local failure or gap, or positive result with its conditions and full load-bearing coverage; excluded subset and hard stops |
| continuation | repairs or direct-owner returns, focused retest, affected consumers, reopen condition |

### SIE.10:4.3 - What Changes in Practice {#what-changes-in-practice}

The team stops asking whether “the integration” passed one test. Each claim has an appropriate layer, evidence, and owner. A bounded subset can be used without hiding excluded rows, and a source or rule repair triggers focused revalidation instead of an automatic full rebuild or a silent continuation.

## SIE.10:7 - Conformance Checklist {#conformance-checklist}

Apply the layer requirements below to the conclusion being claimed. A bounded failure or unresolved result needs sufficient evidence for that result; a positive use claim needs all of its load-bearing obligations covered.

- [ ] The subject, receiving use, and conditions required by the conclusion are identified.
- [ ] Known decisive evidence can finish a bounded failure or scoped gap; material unexamined premises remain distinct from passing ones.
- [ ] Carrier/schema pass is not reported as semantic or receiving-use pass.
- [ ] Endpoint/model adequacy includes examples and counterexamples for required distinctions.
- [ ] Correspondence judgment and mapping execution are tested separately.
- [ ] Every load-bearing identity disposition, issuer/authority condition, and unresolved branch is tested.
- [ ] Claim composition tests include conflict, non-comparability, incomplete source, and source-claim recoverability.
- [ ] Realization/interface tests cover currentness, failure, partial results, access/protection, provenance, and challenge paths as applicable.
- [ ] Quality dimensions and thresholds are selected by the use and do not replace representative Work.
- [ ] Positive, boundary, negative, unlike, and changed-source cases cover the material failure modes.
- [ ] Whole-use disposition is pass, narrow, unresolved, or stop with no score-based compensation of hard stops.
- [ ] Repairs, direct-owner returns, focused retests, affected consumers, and reopen conditions are explicit.
- [ ] No external release, acceptance, authorization, effect, or universal correctness claim is implied.

## SIE.10:9 - Consequences {#consequences}

Defects are localized to source, semantic, identity, composition, mapping, realization, interface, quality, or receiving-use layers. A bounded useful result can proceed without hiding excluded branches, and later changes can trigger focused replay through explicit dependencies.

The cost is several kinds of evidence and collaboration with domain and receiving practitioners. Some integrations that appear technically complete remain unresolved or stop because their identity, authority, or representative-use premises are missing.

## SIE.10:12 - Relations {#relations}

- `SIE.1` supplies the receiving obligations, accepted loss, authority, representative cases, and stop rules.
- `SIE.2` supplies source meanings, editions, authority, provenance, access, currentness, and gaps.
- `SIE.4`–`SIE.9` supply the correspondence, identity, claim-composition, mapping, realization, and interface subjects and their branch contracts.
- Current FPF `A.10` and `A.10.1` govern evidence/provenance reliance and generic affected-use discovery.
- `SIE.11` traces changed source, model, mapping, or interface premises to the receiving uses that rely on them. Matching earlier validation remains usable for unaffected results; material changes reopen the relevant premises and receiving interpretation.
- Applications, Systems Engineering, quality, safety, legal, MDM, Data Engineering, and Operations owners consume the bounded account and retain their own acceptance, authorization, operation, and outcome decisions.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-eng-sie/contract/SIE-1#root or equivalent use; relevant SIE.2-SIE.9 results; direct domain and receiver acceptance criteria @status:spec/done

#source spec://ai.lev/fpf-eng-sie/source/SIE-10
