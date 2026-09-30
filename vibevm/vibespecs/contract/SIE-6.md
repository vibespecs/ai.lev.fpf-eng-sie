# SIE.6 - Fuse Source-Qualified Claims without Erasing Conflict {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Eternal alpha
> **Normativity:** Normative method guidance within SIE; examples are constructed and non-normative.
>
> **Primary working result:** a `SourceQualifiedClaimFusion@Use` that preserves each source claim, subject and any relied-on identity premise, scope, interval, authority, uncertainty, derivation, and relation to other claims, then returns a qualified view, explicit conflict, non-comparability, or unresolved result for one receiving use.

## SIE.6:1 - Problem Frame {#problem-frame}

**Use this when** a receiving answer must combine claims from separately governed sources and a simple union, priority rule, average, overwrite, or “golden record” would hide differences in meaning, subject, time, authority, or uncertainty. The recognizable failure is one clean value whose provenance can be displayed but whose conflict or non-comparability can no longer be recovered.

The primary EntityOfConcern is one source-qualified claim composition for a named receiving question. The first move is to state the exact source claims and the subject relation the receiving question requires. The first result is either a qualified view with explicit derivation or an honest conflict, non-comparability, or unresolved branch.

The payoff is an answer the receiver can interpret without pretending that integration owns truth or preference. Do not use SIE.6 to decide domain truth, authoritative value, survivorship, risk acceptance, or action. A domain authority or receiving decision may consume the composition and choose; SIE preserves what that choice depends on.

## SIE.6:2 - Problem {#problem}

Claims that share a field name can concern different concepts, entities, grains, intervals, or authority scopes. Claims that do concern the same entity can disagree without either being malformed. A timestamp does not settle whether one claim supersedes another; a source rank does not explain why the rank applies; and an average can be meaningless across different measurement definitions.

If composition silently collapses these differences, later validation can test only the fused value. It cannot test the losing claim, the identity premise, the conflict rule, or the receiver's permitted use. Provenance survives as a list of sources but no longer constrains meaning.

## SIE.6:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Simplicity | Receivers prefer one view, while a truthful answer may need several qualified rows or an explicit conflict. |
| Authority | Some sources are authoritative for bounded claims, while no source may own the whole receiving question. |
| Time | Newer claims may supersede older ones, while differing intervals, effectivity, or observation times can make them jointly informative. |
| Identity | Composition needs a subject relation, while an unresolved identity premise must stop only the dependent branch. |
| Uncertainty | Quantification can support comparison, while unlike confidence, status, or evidence forms should not be normalized without warrant. |
| Performance | Precomputed canonical values are convenient, while preserving source-qualified alternatives and derivation costs storage and query work. |

## SIE.6:4 - Solution {#solution}

Compose claims only after their meanings, subjects, scopes, intervals, authority, uncertainty, and provenance are explicit. Classify the relation among claims before applying a rule. Preserve the source claims and any relied-on identity premises in the result. Return a qualified view only under a stated rule and use boundary; otherwise return conflict, non-comparability, or unresolved.

### SIE.6:4.1 - Pattern-Use Unfolding {#pattern-use-unfolding}

1. **Name the receiving question and action.** State what the composed answer may change and which outcomes are acceptable: one qualified row, several rows, conflict, non-comparability, unresolved, or stop.
2. **Bind exact source claims.** Reference `SIE.2` rows and `SIE.4` correspondences. Record each proposition or data-derived claim, scope, interval/effectivity, units, status, uncertainty, derivation, source, and authority.
3. **Bind the subject relation needed by the use.** Reference `SIE.5` when composition depends on claims concerning the same entity. For separately attributed claims about clearly distinct subjects, preserve their subjects and attribution. Keep an explanation of unused identity only when it affects interpretation or later reliance. A correspondence alone does not establish subject identity.
4. **Test comparability.** Decide whether claims use compatible concepts, subjects, grains, units, intervals, and observation/decision roles. Preserve non-comparability as a result.
5. **Classify the claim relation.** Distinguish compatible conjunction, refinement, overlap, duplication, supersession under a justified rule, contradiction, non-comparability, and unresolved relation.
6. **Choose a bounded composition rule.** Examples include retaining all qualified claims, selecting one claim under an explicit domain authority/effectivity rule, deriving a new claim through a stated calculation, or returning conflict. State rejected alternatives and semantic loss.
7. **Construct the qualified output.** Include the source claims or stable references, applied rule, any relied-on identity premise, derived value if any, provenance/trace, authority boundary, uncertainty, conflict/non-comparability status, and permitted receiving use.
8. **Expose failure and challenge.** Define missing-source, stale-source, unresolved-identity, incompatible-unit, contradictory-authority, and unsupported-default branches. Do not convert them into null or a chosen value without the contract's permission.
9. **State downstream and reopen conditions.** Identify mappings and interfaces that consume the composition and the source, identity, rule, authority, or use change that reopens it.

### SIE.6:4.2 - Record the Result {#record-the-result}

| Composition position | Required content |
| --- | --- |
| receiving use | question, action changed, acceptable output branches |
| source claims | exact propositions/data claims, meanings, subjects, scopes, intervals/effectivity, units, status, uncertainty, source and derivation |
| identity premise | referenced `SIE.5` disposition when composition relies on identity; an explanation of unused identity only when it affects interpretation or later reliance |
| comparability | compatible dimensions and any difference that prevents comparison |
| claim relation | conjunction, refinement, overlap, duplicate, qualified supersession, contradiction, non-comparability, unresolved |
| composition rule | rule, authority/evidence basis, conditions, rejected alternatives, semantic loss |
| output | qualified view or explicit conflict/non-comparability/unresolved result, provenance/trace, permitted use |
| downstream and reopen | mapping/interface references, failure branches, exact changes that reopen |

### SIE.6:4.3 - What Changes in Practice {#what-changes-in-practice}

The team stops treating a canonical value as the natural output of integration. A receiver can see why claims were combined, retained separately, or stopped, and can return to the exact source, identity, authority, or rule that changes the answer.

## SIE.6:7 - Conformance Checklist {#conformance-checklist}

- [ ] The receiving question and every allowed output branch are explicit.
- [ ] Source claims retain meaning, subject, scope, interval/effectivity, units, status, uncertainty, source, and derivation.
- [ ] Every load-bearing subject identity premise is referenced and tested.
- [ ] Comparability is judged before aggregation or selection.
- [ ] Compatible, refining, overlapping, duplicate, superseding, contradictory, non-comparable, and unresolved relations are distinguishable.
- [ ] A composition rule states its authority/evidence basis, conditions, rejected alternatives, and loss.
- [ ] Source claims remain recoverable from the output.
- [ ] Missing, stale, unresolved-identity, incompatible-unit, contradictory-authority, and default branches are explicit where applicable.
- [ ] The result does not claim domain truth, authoritative value, preference, authorization, or action beyond its source and receiver boundaries.

## SIE.6:9 - Consequences {#consequences}

Receivers obtain explainable views and honest conflict branches. Corrections can target the source claim, identity premise, composition rule, or receiving use without reconstructing an opaque golden record. Different receivers may lawfully obtain different bounded views from the same preserved claims.

The cost is richer output and explicit rule ownership. Some applications must handle plural, incomplete, or conflicting results instead of one scalar value.

## SIE.6:12 - Relations {#relations}

- `SIE.2` supplies source claims, meanings, editions, authority, provenance, currentness, and gaps.
- `SIE.4` supplies the qualified correspondences needed to compare claim predicates or values.
- `SIE.5` supplies load-bearing subject identity dispositions; claim conflict does not alter those identities by itself.
- `SIE.7` may implement the qualified composition rule but must preserve its branches and trace.
- `SIE.9` exposes qualified views, plural claims, conflict, non-comparability, and incomplete-source states to the receiver.
- `SIE.10` tests the composition rule and negative branches. MDM, domain, and application owners retain truth, value, preference, authorization, and action.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-eng-sie/contract/SIE-2#root, spec://ai.lev/fpf-eng-sie/contract/SIE-4#root; spec://ai.lev/fpf-eng-sie/contract/SIE-5#root when identity is load-bearing; FPF spec://ai.lev/fpf-spec/contract/C-2-1#root, spec://ai.lev/fpf-spec/contract/A-10#root @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-sie/contract/SIE-7#root @status:spec/done

#source spec://ai.lev/fpf-eng-sie/source/SIE-6
