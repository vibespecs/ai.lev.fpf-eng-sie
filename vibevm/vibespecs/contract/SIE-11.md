# SIE.11 - Trace Semantic Change and Revalidate Affected Uses {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Eternal alpha
> **Normativity:** Normative method guidance within SIE; examples are constructed and non-normative.
>
> **Primary working result:** qualified results for the semantic-integration uses affected by a changed premise; an `AffectedSemanticUseRevalidationAccount@Change` assembles them when a receiving use needs a common account.

## SIE.11:1 - Problem Frame {#problem-frame}

**Use this when** a relied-on source definition, model commitment, identifier meaning, mapping premise, or interface interpretation changes and the integration's continued use needs a decision. A familiar warning sign is an unchanged API field that now answers a different question.

Start by comparing the earlier and later meaning at the receiving question. A compatible documentation move can finish with a reference repair. A changed meaning can require repair or renewed validation of the integration results that relied on it.

The object is the affected semantic reliance and its consequences for receiving uses. The gain is a justified continuation, repair, narrowed use, or scoped unresolved result. To assert that all uses remain unaffected, establish adequate coverage of the relevant uses and their reliance.

Use the applicable domain Method directly for a known operational change that does not alter a relied-on source or semantic premise. If one already identified use is the whole question, resolve that use directly with the relevant domain Method and A.10 reliance guidance. A.10.1 is needed when affected uses must be discovered across a scope.

## SIE.11:2 - Problem {#problem}

A source update can be treated as harmless because the schema still parses, or as universally disruptive because its version changed. Either response misses the actual reliance. Some consumers use a definition that changed; others use a different proposition from the same source; still others are merely mentioned in nearby records.

Indiscriminate revalidation consumes work without settling those differences. An incomplete search can create the opposite error: one repaired mapping is reported as proof that the entire integration remains valid.

## SIE.11:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Selectivity | Only affected reliance needs reopening, while hidden consumers can remain dependent on changed meaning. |
| Continuity | Matching earlier results save work, while changed assumptions can invalidate them. |
| Coverage | A local answer can finish promptly, while a wider no-impact claim needs wider support. |
| Authority | An integrator can repair its mappings and interfaces, while source and receiving decisions retain their owners. |
| Evidence effort | Additional inquiry can change a decision, while unavailable or low-value information can consume the work needed for repair. |

## SIE.11:4 - Solution {#solution}

Follow the changed proposition through actual semantic dependencies to the results and receiving uses it can alter. Complete supported branches at their proper scope. Assemble a wider account only for a receiver that needs it.

### SIE.11:4.1 - Pattern-Use Unfolding {#pattern-use-unfolding}

1. **Compare the relied-on meaning.** Identify what the receiving question depended on in the earlier source or premise and what the later content says. Include changed applicability, subject grain, interval, assumptions, or limits where relevant. An inaccessible later definition leaves that comparison unresolved.
2. **Finish a compatible repair when sufficient.** If content, applicability, and access remain compatible for the use, make the needed reference repair and retain matching results. A version or URL change alone does not require every downstream Method to run again.
3. **Find affected uses when their scope is unsettled.** Apply A.10.1 to discover actual reliance within the question's scope, using source-side and receiver-side evidence or an index that adequately covers both. Distinguish a material dependency from a mention. Retain coverage gaps that limit the intended conclusion.
4. **Select the integration result that the change can alter.** Use the domain returns below. Follow a further consumer only when the changed result can alter its action or claim. The physical proximity of files is not a dependency rule.
5. **Repair or revalidate that result.** Apply its defining Method to the changed premise. Reuse earlier evidence whose actual conditions still match. Return a supported continuation, repair, permitted narrower use, or scoped gap. Source truth, master identity, product release, and application decisions go to the owners of those decisions.
6. **Return the completed branch.** Give the receiver the result it needs, with the changed premise and remaining limits where those affect reliance. A completed direct result is sufficient for its own receiving question.
7. **Combine results when a receiver needs the wider answer.** State the covered uses, their relevant results, unresolved uses or discovery gaps, and the continuation that those results support. A broader no-impact conclusion requires the corresponding coverage; completed local branches cannot supply unexamined ones.

When additional evidence is being considered, apply `C.11.DUA` to compare its attainable contribution to the receiving decision with its cost, delay, downside, and displaced work. A gap can remain a qualified gap when further inquiry cannot support a worthwhile next action; that limitation does not warrant a stronger claim.

### SIE.11:4.2 - Domain Returns {#domain-returns}

| Changed reliance | Integration result to revisit |
| --- | --- |
| A concept, relation, or model constraint | SIE.3 model adequacy and any affected SIE.4 correspondence. |
| Identifier meaning, scheme, grain, or interval | SIE.5 identity disposition and the results that actually use it. |
| Source-claim scope or interpretation | SIE.6 composition, conflict, or non-comparability result. |
| A transformation premise | SIE.7 mapping and its affected outputs. |
| Availability, permissions, freshness, or service conditions | SIE.8 realization choice or SIE.9 receiving interface, according to the changed condition. |
| Receiving meaning or acceptance condition | SIE.9 interface contract and the corresponding SIE.10 validation. |

This table locates the defining result; the actual dependency determines which returns are needed and their useful order.

### SIE.11:4.3 - Record the Result {#record-the-result}

For a direct repair, use the result already needed by its consumer. For a common account, retain the following content at the scope the receiver needs:

| Account position | Receiving content |
| --- | --- |
| Change and reliance | Earlier relied-on meaning, later meaning, and the affected question. |
| Covered uses | Actual dependencies and the basis for the stated discovery scope. |
| Direct results | Completed repairs, revalidation, permitted continuation, or narrowed uses under their defining Methods. |
| Unresolved reach | Unexamined or inaccessible reliance, discovery gaps, and their effect on the conclusion. |
| Continued use | What the receiver can now rely on and which changed conditions would reopen it. |

The account summarizes its constituent results. It does not serve as a circular input that those results must await before they can be completed.

### SIE.11:4.4 - What Changes in Practice {#what-changes-in-practice}

The maintainer can say which interface meaning changed, which mapping or identity result was revisited, and what can continue. A corrected local reference can finish immediately. A broader claim remains bounded by the uses actually discovered and assessed.

## SIE.11:7 - Conformance Checklist {#conformance-checklist}

- [ ] The compared change concerns a premise used by an identified receiving question.
- [ ] Compatible reference repair can complete without a wider account.
- [ ] Discovery, where needed, supports the stated scope and distinguishes dependencies from mentions.
- [ ] Each affected integration result uses its defining Method.
- [ ] Reused evidence still matches its actual conditions.
- [ ] Independently supported branches finish at their own scope.
- [ ] A common account has a receiving use and preserves unresolved coverage.
- [ ] A wider no-impact claim has support for the uses it covers.

## SIE.11:9 - Consequences {#consequences}

Supported uses can continue while affected branches receive focused repair. Dependency evidence becomes useful because it points to a changed receiving result. Local completion no longer waits for an unnecessary integration-wide account.

Finding hidden reliance and interpreting source changes can require domain and receiver participation. A wider assurance claim may remain unavailable while an actual consumer or later definition is inaccessible. The result preserves that limitation without erasing completed branches.

## SIE.11:12 - Relations {#relations}

- A.10.1 governs affected-use discovery when the scope of reliance needs to be found.
- SIE.2 supplies the source meaning, edition, authority, and access premises used in the comparison.
- SIE.3–SIE.9 supply the domain results located in §4.2; SIE.10 supplies validation for the affected receiving claim.
- SIE.12 supplies the module dependencies and material-change arrangements of an actual commons.
- Domain source owners, MDM, SYSE, operational providers, and receiving applications retain their respective decisions.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): Changed relied-on premise; relevant SIE.2-SIE.10 results; FPF spec://ai.lev/fpf-spec/contract/A-10-1#root when discovery is needed @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-sie/contract/SIE-12#root @status:spec/done

#source spec://ai.lev/fpf-eng-sie/source/SIE-11
