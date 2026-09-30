# SIE.8 - Choose Virtual, Materialized, or Hybrid Semantic Realization: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## SIE.8:5 - Archetypal Grounding - Provider Availability without Replication {#archetypal-grounding-provider-availability-without-replication}

Two providers expose current availability through governed APIs. Provider A means “on hand”; Provider B means “available to promise”. `SIE.4` preserves the semantic difference and `SIE.6` permits a qualified side-by-side answer but forbids arithmetic fusion. Neither provider permits replication of its availability state.

If the question is only whether a proposed copied availability store may serve that contract, the completed answer is: “Reject the proposed copied availability store for this purchasing use: the qualified provider conditions prohibit copying the required availability state.” The contract, proposal, and provider conditions identify its scope and grounds. This concludes that question without a latency study, credential design, recovery plan, or alternative selection.

When the receiving question also asks which remaining arrangement to use, continue with the following comparison:

| Candidate | Constructed comparison |
| --- | --- |
| materialized common graph | excluded by the providers' prohibition on copying availability state; that condition is sufficient without developing its implementation, recovery, and exit |
| query-time virtual mapping | retained alternative: preserves source custody and timestamps and can return provider-specific qualified rows; depends on runtime credentials, latency, provider availability, query limits, and explicit timeout/incomplete branches |
| hybrid metadata plus virtual values | selected conditionally: materialize stable product-family correspondences, mapping rules, and source metadata where their copying and maintenance are permitted; retrieve volatile availability values at query time; invalidate metadata when source definitions or product relations change |

The decision selects the hybrid arrangement because stable semantic premises can be inspected and volatile restricted values remain at their sources. It requires Data Engineering and security results for credential handling, concurrent calls, timeout behavior, observability, and recovery. SIE.9 receives separately attributed quantities and timestamps, provider errors, and the permitted incomplete-result and fallback behavior. No running interface or provider reliability is claimed.

## SIE.8:6 - Bias-Annotation {#bias-annotation}

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Governance | Materialization silently transfers custody, authority, or permission. | Record source rights, retention, correction, and use authority for every copied state. |
| Architecture | The incumbent platform determines the answer, or every conceivable alternative requires full design. | Use sufficient exclusions, then compare serious alternatives as complete arrangements on the receiving basis. |
| Ontology/Epistemology | A graph or warehouse is treated as the semantic arrangement itself. | Keep mapping premises, claims, provenance, and validation independent of carrier. |
| Pragmatics | Every unresolved comparison commissions a probe. | Compare obtainable decision benefit with the probe's full burden and displaced work. |
| Didactics | “Virtual is fresh; materialized is fast” becomes a universal rule. | Show source latency, snapshot reproducibility, invalidation, and failure conditions that reverse the slogan. |

## SIE.8:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| “Knowledge graph” as the requirement | Restate the receiving result and compare graph and non-graph realizations. |
| Virtual means no state | Record mappings, caches, credentials, query occurrences, source snapshots, and provenance state actually required. |
| Materialized means reliable | Test refresh, invalidation, correction/deletion, recovery, and source-authority changes. |
| Hybrid means best of both | Expose coherence, invalidation, fallback, and doubled operating responsibilities. |
| Product feature checklist | Compare serious arrangements on use-sensitive criteria, joint resource demand, and relevant failure cases. |
| Decision equals implementation | Name the exact build, provider, security, and operating results still missing. |

## SIE.8:10 - Rationale {#rationale}

Virtual and materialized are not merely deployment choices: they change when and where mappings execute, which state is copied, how provenance and currentness are established, and which failures reach the receiver. Those changes can alter semantic adequacy, so SIE owns the bounded comparison while direct practices own implementation and operation.

## SIE.8:11 - SoTA-Echoing {#sota-echoing}

The best-known line combines declarative mappings, virtual knowledge-graph systems, data federation, materialized integration, and operational data-product practice. The serious default alternatives are “materialize one canonical graph” and “federate everything live”. Each can be correct under conditions; each is defective as a universal answer because it hides a different set of currentness, access, provenance, and recovery obligations. SIE.8 mutates the line into a whole-arrangement choice around one semantic result.

| Source line | Adopt, adapt, or reject | Role and limit |
| --- | --- | --- |
| [Ontop virtual-KG line](https://ontop-vkg.org/research/publications.html) | adapt | Demonstrates query-time virtual realization over mappings; it does not make virtual RDF mandatory or supply source access and receiving acceptance. |
| [R2RML](https://www.w3.org/TR/r2rml/) | adapt | Supplies one declarative mapping form usable in virtual or materialized arrangements; relational/RDF technology is optional. |
| [Data on the Web Best Practices](https://www.w3.org/TR/dwbp/) | adapt | Contributes access, version, provenance, reuse, and persistence questions; Web publication is not required. |
| universal canonical graph | reject as default | Materialization is one candidate and cannot transfer source authority or erase incompatibility. |
| universal live federation | reject as default | Query-time access does not guarantee freshness, availability, permitted disclosure, or reproducibility. |

Reopen when source access or replication rights change, measured latency/availability defeats the use, refresh/invalidation fails, mapping or source semantics change, security/provenance conditions change, or a new candidate materially improves the comparison.


## SIE.8:End {#end}
