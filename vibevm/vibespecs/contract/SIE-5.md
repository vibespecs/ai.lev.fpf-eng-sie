# SIE.5 - Resolve Cross-Source Identity without Erasing Identifier Authority {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Eternal alpha
> **Normativity:** Normative method guidance within SIE; examples are constructed and non-normative.
>
> **Primary working result:** a `CrossSourceIdentityDisposition@Use` that states, for each load-bearing endpoint pair or set, the required entity grain and interval, identity-related disposition, source identifier schemes and issuers, evidence, authority boundary, unresolved cases, and the exact mappings, claim compositions, interfaces, and tests that may consume it.

## SIE.5:1 - Problem Frame {#problem-frame}

**Use this when** an integration needs to decide whether records or identifiers from different sources concern the same entity, a part, a version, a variant, an alternate description, a family, or different or unresolved entities. The recognizable failure is a join, merged key, or `sameAs` assertion that makes identifiers appear unified while erasing their issuers, grains, intervals, and authority.

The primary EntityOfConcern is one bounded cross-source identity question for a named use. The first move is to state the entity grain and time or effectivity interval at which sameness matters. The first result is a disposition that downstream work can inspect and challenge without replacing source identifiers or master-data authority.

The payoff is that the integration can join only warranted cases, return exact unresolved branches, and preserve source trace. Do not use SIE.5 to create identifiers, choose enterprise master identity or survivorship, decide authoritative values, or prove a source claim true. Those decisions remain with identifier owners, MDM, or the direct domain authority.

## SIE.5:2 - Problem {#problem}

The same real-world item can carry manufacturer, supplier, enterprise, lot, serial, package, event, and temporary process identifiers. Conversely, the same character string can be reused by different issuers or at different times. Version, configuration, part-whole, and alternate-description relations can be mistaken for identity because they support some joins.

If an integration collapses those distinctions, provenance becomes decorative: the merged record no longer shows which identifier asserted what, when, or under whose rules. Contradictory events appear to concern one thing without evidence, and a master key silently becomes a domain decision.

## SIE.5:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Joinability | A common key makes computation easy, while premature merging can create false identity and irreversible provenance loss. |
| Grain | Receivers want one “item”, while wafer, die, device, package, lot, feature, version, and event answer different questions. |
| Time and effectivity | Identity may be stable across one interval, while reuse, replacement, split, merge, and revision change the warranted claim. |
| Authority | Identifier issuers and master-data stewards govern different schemes and decisions; crosswalk custody transfers neither authority. |
| Incomplete evidence | A bounded decision is needed, while some pairs must remain unresolved without blocking independent rows. |
| Reuse | A disposition can help several mappings, while its grain, interval, and use boundary prevent blanket equivalence. |

## SIE.5:4 - Solution {#solution}

Frame identity as a source-qualified, grain- and interval-specific disposition for one receiving use. Preserve every source identifier and issuer. Compare the entity criteria, relation evidence, version/effectivity, and authoritative decisions that matter. Return same, different, part, version, variant, alternate-description, family, or unresolved only at the precision supported; do not force every useful relation into identity.

### SIE.5:4.1 - Pattern-Use Unfolding {#pattern-use-unfolding}

1. **Name the receiving identity question.** State which mapping, claim composition, query, or decision needs an identity premise and what a wrong merge or split would change.
2. **Fix entity grain and interval.** Name the relevant individual or occurrence kind, part-whole level, version/configuration, lifecycle state, jurisdiction or organization, and time/effectivity interval.
3. **Bind source endpoints.** Reference each `SIE.2` identifier scheme, issuer/owner, syntax, resolution behavior, restrictions, identified-entity claim, edition, and source provenance.
4. **Separate candidate relation kinds.** Consider same individual at the stated grain, different individuals, part/whole, earlier/later version or specialization, variant, alternate description, family membership, or unresolved. Do not use one boolean until the use truly needs only that distinction.
5. **Collect discriminating evidence.** Use issuer records, source assertions, configuration/effectivity, provenance, physical or domain characteristics, event histories, and counterexamples. A shared string or co-occurrence is only candidate evidence.
6. **Recover authority.** Name who may decide scheme-local identity, master identity, authoritative values, or the domain relation. SIE may record and use a bounded disposition; it does not acquire those authorities.
7. **Assign the narrowest warranted disposition.** State conditions, confidence or uncertainty where meaningful, rejected alternatives, and unresolved evidence. Preserve source IDs even for accepted same-entity rows.
8. **Propagate the premise explicitly.** Reference the disposition from every mapping, claim composition, interface row, and identity test that relies on it. Never copy only the merged key.
9. **Test difficult cases and reopen.** Include identifier reuse, split/merge, version/configuration change, part-whole confusion, contradictory source events, and absent-link cases. State the source or observation change that reopens the row.

### SIE.5:4.2 - Record the Result {#record-the-result}

| Identity position | Required content |
| --- | --- |
| identity question and use | receiver, dependent action, wrong-merge/wrong-split consequence |
| entity boundary | kind and grain, part-whole level, version/configuration, interval/effectivity, relevant context |
| source identifiers | scheme, identifier, issuer/owner, syntax/resolution/restrictions, source edition and provenance |
| candidate relations | same, different, part, version/specialization, variant, alternate description, family, unresolved alternatives |
| warrant | evidence, counterevidence, counterexamples, uncertainty/confidence, rejected alternatives |
| authority | scheme-local, master-data, domain, and receiving-decision scopes |
| disposition | narrowest warranted relation or unresolved result, conditions, source-ID preservation rule |
| downstream and reopen | mapping/composition/interface/test references and exact change or observation that reopens |

### SIE.5:4.3 - What Changes in Practice {#what-changes-in-practice}

The integration stops minting a common key as proof of identity. Every load-bearing join points to a disposition with grain, interval, source identifiers, evidence, and authority. Unresolved identity becomes an explicit interface and validation branch instead of a row silently dropped or merged.

## SIE.5:7 - Conformance Checklist {#conformance-checklist}

- [ ] The receiving action and wrong-merge/wrong-split consequence are named.
- [ ] Entity kind, grain, part-whole level, version/configuration, and interval/effectivity are explicit.
- [ ] Every identifier retains its scheme, issuer/owner, restrictions, source edition, and provenance.
- [ ] Useful non-identity relations are not compressed into a boolean same/different field.
- [ ] Shared strings, co-occurrence, and crosswalk membership are treated only as candidate evidence.
- [ ] Evidence, counterevidence, counterexamples, and uncertainty are inspectable.
- [ ] Scheme-local, master-data, domain, and receiving-decision authority scopes remain separate.
- [ ] Accepted same-entity rows do not delete source identifiers.
- [ ] Every dependent mapping, composition, interface, and test references the disposition.
- [ ] Reuse, split/merge, version/configuration, part-whole, contradiction, and absent-link cases are tested where applicable.

## SIE.5:9 - Consequences {#consequences}

The package can join warranted identities without losing source trace and can stop only the branches that depend on unresolved identity. Corrective source or steward decisions can be replayed against explicit consumers. The method also reveals when the useful relation is part, version, membership, or event participation rather than identity.

The cost is domain evidence and authority work. Some convenient global keys remain technical indexes rather than semantic truths, and some desired traces return incomplete.

## SIE.5:12 - Relations {#relations}

- `SIE.1` supplies the receiving action, identity-sensitive answer claims, loss boundary, tests, and stop.
- `SIE.2` supplies identifier schemes, issuers, restrictions, source claims, editions, provenance, and authority gaps.
- `SIE.4` may expose an identity question but does not answer it merely by accepting a semantic correspondence.
- `SIE.6` consumes identity dispositions when composing claims about the same bounded entity; it preserves contradictory claims separately.
- `SIE.7` and `SIE.9` reference dispositions rather than copying only merged keys.
- `SIE.10` tests every load-bearing identity premise. MDM and domain authorities retain master identity, authoritative values, and action.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-eng-sie/contract/SIE-2#root; conditional spec://ai.lev/fpf-eng-sie/contract/SIE-4#root; direct MDM/domain authority inputs @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-fdm/contract/FDM-2#root, spec://ai.lev/fpf-eng-sie/contract/SIE-6#root, spec://ai.lev/fpf-eng-sie/contract/SIE-7#root @status:spec/done

#source spec://ai.lev/fpf-eng-sie/source/SIE-5
