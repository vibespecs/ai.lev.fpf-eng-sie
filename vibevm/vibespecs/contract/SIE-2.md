# SIE.2 - Recover and Qualify Source Semantics and Authority {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Eternal alpha
> **Normativity:** Normative method guidance within SIE; examples are constructed and non-normative.
>
> **Primary working result:** a `SourceSemanticInventory@Use` that records the load-bearing source assets, local meanings, schemes, editions and effectivity, identifiers, claims, owners and authority scope, provenance, access, currentness, gaps, and exact returns for one semantic-integration use.

## SIE.2:1 - Problem Frame {#problem-frame}

**Use this when** a bounded integration use exists, yet endpoint meanings are being inferred from labels, column names, class names, diagrams, sample values, or undocumented organizational knowledge. The recognizable failure is a mapping that runs while joining different concepts, editions, grains, or authority scopes.

The primary EntityOfConcern is the set of source-local semantic premises that the receiving use actually consumes. The first move is to select one load-bearing source asset and recover its scheme, edition or effectivity, meaning, owner, authority, provenance, and access conditions. The first result is an inventory that makes both usable premises and exact gaps inspectable.

The payoff is a clean separation between what a source says, what an integrator infers, and what another owner must decide. Do not use SIE.2 to construct an ontology, establish a cross-source correspondence, decide identity, fuse claims, or judge receiving-use adequacy. If model adequacy for a required distinction remains unsettled, request `UseFitSemanticModel@Use` from `SIE.3` or another qualified direct provider. Adequate reuse can finish that question; an actual missing distinction may require extension or construction.

## SIE.2:2 - Problem {#problem}

Source inventories often list files and endpoints but omit the meanings that make their values usable. A table called `feature`, an API field called `available`, and an identifier called `partNumber` appear self-describing. Their actual senses may depend on an edition, profile, configuration, interval, issuer, lifecycle state, organizational rule, or local extension.

When those dependencies are hidden, later workers can neither justify a correspondence nor trace a failure. A changed source looks like a schema defect even when the meaning changed; an access right is mistaken for authority; and a provenance record is mistaken for truth.

## SIE.2:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Selectivity | Reading every source is infeasible, while skipping one load-bearing definition can invalidate the package. |
| Formal and operative meaning | Standards and schemas provide inspectable definitions, while actual profiles, extensions, and Work can narrow or alter use. |
| Edition and effectivity | A stable name aids reuse, while its meaning or applicability can change across revisions, profiles, configurations, and intervals. |
| Authority | Publishers and stewards define bounded schemes or values, while the receiver may need a decision outside their scope. |
| Access | A source may be meaningful but unavailable, restricted, delayed, or legally unusable for the proposed integration. |
| Adequacy | Existing models reduce construction work, while forcing an inadequate model hides a real semantic gap. |

## SIE.2:4 - Solution {#solution}

Recover source semantics at the smallest grain that can change the receiving answer. Preserve term, concept, type, relation, schema, model, claim, data item, carrier, identifier, and world-side referent as different questions. Qualify each relied-on premise by source identity, edition/effectivity, authority scope, provenance, access, currentness, and known gaps.

### SIE.2:4.1 - Pattern-Use Unfolding {#pattern-use-unfolding}

1. **Take the source cut from the use contract.** Add another source only when it can change an answer claim, test, loss, or stop condition.
2. **Identify the source asset and carrier.** Record publisher or owning System, title or endpoint, profile/module, version or edition, publication and effectivity, retrieval location, and carrier kind. Keep the asset distinct from the concepts and claims it carries.
3. **Recover the local scheme and scope.** State the domain, population, lifecycle state, configuration, jurisdiction, or Work context in which the source definitions apply.
4. **Recover exact meanings.** For every load-bearing endpoint, record the designation, definition or operative rule, type/relation role, examples and counterexamples, units or codes, and unresolved ambiguity. Use source-local language before normalizing it.
5. **Separate identifiers and identified entities.** Record the scheme, issuer or owner, syntax, resolution behavior where relevant, use restrictions, grain, interval, and what the identifier does not establish.
6. **Separate claims, data, and provenance.** Record which claim a data item represents, its scope and time, how it was derived, who or what supplied it, and which uncertainty or status accompanies it. Provenance does not make the claim true.
7. **Recover authority and access.** Name who may define the scheme, issue identifiers, decide authoritative values, approve local extensions, grant access, and authorize receiving use. Mark unsupported assumptions.
8. **Assess currentness and use adequacy.** Compare the source premise with the contract. State whether it is adequate, adequate only under conditions, unresolved, obsolete for this use, inaccessible, or missing.
9. **Return an inadequate model honestly.** If the required distinction cannot be expressed in the available source or supplied semantic model, request `UseFitSemanticModel@Use`; do not hide the gap in a mapping rule.
10. **Record dependencies and next results.** Identify the exact definitions, editions, authority facts, and gaps consumed by `SIE.4`–`SIE.10`, plus observations that reopen this inventory.

### SIE.2:4.2 - Record the Result {#record-the-result}

| Inventory position | Required content |
| --- | --- |
| source identity | owning/publishing System, asset or endpoint, profile/module, carrier, location |
| edition and applicability | version/edition, publication, effectivity/configuration/interval, local extension status |
| local semantic endpoints | designation, definition or operative rule, type/relation role, scope, examples/counterexamples, units/codes |
| identifiers | scheme, issuer/owner, syntax, resolution behavior, restrictions, grain, interval, identified-entity claim |
| claims and data | source claim, represented data item, scope/time, uncertainty/status, derivation and provenance |
| authority and access | meaning, identifier, value, extension, access, and receiving-use authority scopes |
| qualification | adequate, conditional, unresolved, obsolete, inaccessible, missing, or model-gap return with reason |
| dependency and reopen | consuming package rows, known gaps, next result, and source/edition/meaning changes that reopen |

### SIE.2:4.3 - What Changes in Practice {#what-changes-in-practice}

The team stops mapping from field names. A later correspondence or transformation can point to exact source-local endpoints and editions, and a failure can return to the owner of the missing meaning, authority, access, or model. An inventory row can be useful even when its disposition is unresolved or inaccessible.

## SIE.2:7 - Conformance Checklist {#conformance-checklist}

- [ ] Every included source can change a named contract position.
- [ ] Source asset, carrier, local scheme, semantic endpoint, identifier, claim, data item, and referent remain distinguishable.
- [ ] Edition, profile/module, effectivity/configuration/interval, and local extensions are explicit where load-bearing.
- [ ] Definitions or operative rules include scope and at least one discriminating example or counterexample where ambiguity matters.
- [ ] Identifier scheme, issuer/owner, grain, interval, restrictions, and resolution assumptions are explicit.
- [ ] Claims retain provenance, scope, time, status, and uncertainty without treating provenance as truth.
- [ ] Meaning, identifier, authoritative-value, extension, access, and receiving-use authorities remain separate.
- [ ] Every row has an adequate, conditional, unresolved, obsolete, inaccessible, missing, or model-gap disposition.
- [ ] Consuming rows and reopen conditions are recoverable.

## SIE.2:9 - Consequences {#consequences}

Mappings become reviewable against exact endpoints, and source changes can be traced to the rows that relied on them. Authority, access, and model gaps appear before implementation. The same inventory can support several direct pattern entries while each use retains its own qualification.

The cost is source-local reading and coordination with publishers, stewards, domain specialists, and access owners. Some attractive automation must wait because the source meaning or applicability is unresolved.

## SIE.2:12 - Relations {#relations}

- `SIE.1` supplies the receiving use, source cut, answer claims, preserved distinctions, and stop conditions.
- `SIE.3` qualifies an available model for the named use or develops an actual missing distinction. Request that result when the recovered source model leaves the integration's model question unsettled.
- `SIE.4`, `SIE.5`, and `SIE.6` consume exact endpoint meanings, source claims, identifiers, editions, and authority limits.
- `SIE.7`–`SIE.10` consume the manifest, provenance, currentness, and gap dispositions relevant to implementation and validation.
- Domain sources, MDM, access owners, Systems Engineering, Data Engineering, and applications retain their respective meanings, values, permissions, operational results, and decisions.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-eng-sie/contract/SIE-1#root or equivalent contract; FPF spec://ai.lev/fpf-spec/contract/F-0-1#root, spec://ai.lev/fpf-spec/contract/F-0-2#root; direct source owners @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-sie/contract/SIE-3#root, spec://ai.lev/fpf-eng-sie/contract/SIE-4#root, spec://ai.lev/fpf-eng-sie/contract/SIE-5#root, spec://ai.lev/fpf-eng-sie/contract/SIE-6#root, spec://ai.lev/fpf-eng-sie/contract/SIE-7#root @status:spec/done

#source spec://ai.lev/fpf-eng-sie/source/SIE-2
