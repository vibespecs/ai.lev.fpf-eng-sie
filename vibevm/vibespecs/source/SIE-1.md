# SIE.1 - Bound the Receiving Use and Semantic Contract: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## SIE.1:5 - Archetypal Grounding - AP242/QIF Configuration Query {#archetypal-grounding-ap242-qif-configuration-query}

A quality engineer asks which QIF inspection plan and result concern feature `F` in released AP242 product-definition revision/configuration `R` at effectivity `E`. The initial request is “connect PLM and quality data in a knowledge graph.” SIE.1 replaces the carrier proposal with this contract:

| Position | Constructed value |
| --- | --- |
| receiver/use | quality engineer preparing an evidence return for one configuration-bound review; query by revision/configuration, feature, and effectivity |
| answer claims | AP242 feature identifier and configuration/effectivity claim; QIF plan, characteristic, and result identifiers; relation disposition; source edition; timestamp; provenance; unmatched/incompatible status |
| preserved distinctions | product feature versus inspection characteristic; definition versus performed result; revision versus configuration; applicability/effectivity; source identifier and issuer; plan versus result |
| tolerated loss | display may coarsen source-local labels after exact identifiers and relations remain available; no unmatched feature or incompatible characteristic may become a positive relation. For this constructed evidence-return review, the receiver permits the qualified row set with unresolved local-extension and unknown-unit branches shown separately; the partial answer supplies available qualified evidence while leaving those branches unresolved |
| currentness and latency | for this constructed review at time T, the receiver requires the released AP242 configuration applicable to the review, QIF observations from T minus 24 hours through T, and a query response within two seconds. These are stipulated receiving-contract criteria for this demonstration |
| authority | Systems Engineering owns release, configuration, and effectivity; the quality authority owns acceptance; source owners define their models; SIE may qualify mappings but authorizes neither decision |
| tests | known match; unmatched feature; changed revision; incompatible characteristic; stale QIF result; missing provenance; source timeout |
| stop/reopen | stop on unresolved configuration/effectivity, source edition, feature identity, permission, or acceptance rule; reopen when a relied-on AP242/QIF edition, review use, or protected condition changes |

This result does not claim that the two source models correspond or that an interface works. It makes those later claims testable. AP242 edition 4 is recorded by `SIE.2` with its current source status; SIE.1 only requires the edition and reopen rule to be explicit.

## SIE.1:6 - Bias-Annotation {#bias-annotation}

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Governance | The integration team silently accepts loss or acts as source/value authority. | Name each decision subject and the direct authority relation; make absence a blocker. |
| Architecture | Platform boundaries define the semantic use. | Begin from the receiving result and keep realization alternatives open. |
| Ontology/Epistemology | A shared label or data field is treated as a shared meaning or true claim. | State answer claims, source contexts, preserved distinctions, and uncertainty separately. |
| Pragmatics | The contract becomes a complete requirements catalogue rather than a decision tool. | Keep only conditions that can change the receiving action or stop. |
| Didactics | Readers infer that SIE.1 must precede every other pattern. | Enter directly elsewhere when an equivalent current contract already exists; verify compatibility instead of repeating it. |

## SIE.1:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| “Integrate all enterprise data.” | Name one receiver and the smallest source cut that can change one use. |
| “The knowledge graph is the deliverable.” | State the receiving answer and treat graph materialization as one later realization option. |
| “No information loss.” | Name the distinctions and tests; unlimited preservation is not an operational contract. |
| “Real time.” | State a measurable currentness and latency condition for the use. |
| “Single source of truth.” | Name source, identity, and value authorities and the claims each may establish. |
| “Every test must return a row.” | Define legitimate unmatched, incompatible, unavailable, and stop branches. |

## SIE.1:10 - Rationale {#rationale}

Semantic adequacy is relative to a use, but relativity does not make it arbitrary. A receiver, answer claim, source context, permitted loss, authority, and representative test together constrain what counts as a successful integration. Beginning there prevents a carrier choice from becoming an implicit ontology, authority model, and acceptance rule.

## SIE.1:11 - SoTA-Echoing {#sota-echoing}

The best-known line for this question combines use-bounded representation selection, situational Method criteria, quality-for-use, and explicit source/provenance practice. The serious default alternative is technology- or source-led integration. Its defect is not the use of a graph, warehouse, or federation; it is allowing that choice to define the answer and loss boundary. SIE.1 mutates the line by making the whole semantic contract, including authorities and legitimate unresolved branches, the first domain result.

| Source line | Adopt, adapt, or reject | Role and limit |
| --- | --- | --- |
| Current FPF `C.37` | adopt | Bounds representation selection and co-use to a named use; does not supply the SIE package or application authority. |
| Current `ME.3` | adapt | Situational criteria help state receiving Work and fit conditions; SIE adds semantic endpoints, loss, source, authority, and layered tests. |
| [DQV](https://www.w3.org/TR/vocab-dqv/) and [ISO/IEC 25012:2008](https://www.iso.org/standard/35736.html) | adapt | Supply quality dimensions and vocabulary; the contract selects only dimensions that change this use. |
| [Data on the Web Best Practices](https://www.w3.org/TR/dwbp/) | adapt | Contributes provenance, version, access, and reuse questions; no Web publication form is mandatory. |
| platform-first “single source of truth” | reject as default | A carrier and custody arrangement cannot establish cross-source meaning, authority, or receiving-use adequacy. |

Reopen this pattern when representative uses cannot express action-changing loss, authority, or validation obligations through the contract positions, or when a source line supplies a materially better first result.


## SIE.1:End {#end}
