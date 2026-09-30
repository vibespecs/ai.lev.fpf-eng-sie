# SIE.6 - Fuse Source-Qualified Claims without Erasing Conflict: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## SIE.6:5 - Archetypal Grounding - Provider Availability Claims {#archetypal-grounding-provider-availability-claims}

Two providers expose availability for the same buyer-recognized product family. Provider A returns `onHand = 12` at 10:00; Provider B returns `availableToPromise = 9` at 10:02. A purchasing integration initially proposes a single `available = 21` value.

The source inventory shows that `on hand` is current physical stock before reservations, while `available to promise` is a provider-governed commitment quantity after its own reservation and horizon rules. The values are not additive and are not globally equivalent. A product-family correspondence exists, but individual inventory objects are not asserted identical.

| Claim relation question | Constructed result |
| --- | --- |
| Can the two values be summed? | non-comparable for summation because definitions, allocation rules, and authority scopes differ |
| Can both support a “which provider can satisfy quantity 8 now?” query? | conditionally comparable only after the contract accepts Provider A's additional reservation check and Provider B's promise horizon; retain separate rows |
| What if Provider A reports 12 and a later status reports 4? | classify by source occurrence, observation interval, and justified supersession rule; retain both claims and derivation rather than overwriting silently |
| What if product identity is unresolved? | stop that product branch and expose the unresolved `SIE.5` premise |
| What if one API times out? | return available source-qualified rows plus an incomplete-result flag if the contract permits; never substitute zero |

The interface can return two qualified provider rows, explicit non-comparability for arithmetic aggregation, and a missing-source branch. Purchasing owns supplier choice and risk acceptance. SIE.6 supplies no canonical stock fact.

## SIE.6:6 - Bias-Annotation {#bias-annotation}

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Governance | A source priority table silently decides truth or business action. | Name the authority and exact claim scope for every selection or supersession rule. |
| Architecture | The target schema requires one value and erases alternatives. | Change the output shape or expose conflict/non-comparability as first-class branches. |
| Ontology/Epistemology | Data values, claims, facts, and decisions collapse. | Record propositions, scope, uncertainty, derivation, and receiver decision separately. |
| Pragmatics | Every disagreement becomes an elaborate dispute. | Classify only relations that can change the receiving answer; retain independent claims without forced comparison. |
| Didactics | “Fusion” is read as merge or averaging. | Show examples where the correct fusion is a qualified set, conflict, or non-comparability. |

## SIE.6:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| Last write wins | State why time establishes supersession for this claim and interval; otherwise retain both. |
| Trusted source always wins | Name the source's exact authority scope and preserve losing claims and conflict. |
| Average the values | Establish compatible meaning, subject, unit, interval, and aggregation semantics first. |
| Null means zero or absent | Preserve missing, unavailable, unknown, not applicable, and zero as distinct branches. |
| Provenance after fusion | Keep source claims and derivation as inputs to the composition, not decoration on the result. |
| One canonical fact | Return a qualified view only when the use and authority rule warrant it; otherwise return plural claims or conflict. |

## SIE.6:10 - Rationale {#rationale}

Claims are source- and scope-bearing assertions, not free-floating values. Composition is therefore a new derivation whose premises and authority must remain inspectable. Preserving the inputs is what makes conflict, correction, and changed-use replay possible.

## SIE.6:11 - SoTA-Echoing {#sota-echoing}

The best-known line combines claim individuation, provenance, authority-aware data integration, and explicit uncertainty. The serious default is master-record survivorship or source ranking. Those Methods can be valid under an authorized MDM use, but they are defective as a universal semantic-integration default because they hide non-comparability and transfer authority. SIE.6 adapts the line by making the qualified composition or explicit conflict the domain result.

| Source line | Adopt, adapt, or reject | Role and limit |
| --- | --- | --- |
| Current FPF `C.2.1` | adopt | Keeps claims as distinct representational objects; SIE supplies the cross-source use composition. |
| Current FPF `A.10` | adopt | Governs claim-bound evidence and provenance reliance; evidence law does not choose the domain truth or action. |
| [PROV-O](https://www.w3.org/TR/prov-o/) | adapt | Supports derivation, attribution, revision, and invalidation traces; provenance alone establishes no truth, priority, or comparability. |
| MDM survivorship and golden-record practice | adapt only under direct authority | May supply an authoritative-value result for a bounded domain; SIE preserves its source and scope rather than generalizing it. |
| last-write, average, or global source-rank defaults | reject as universal | Each may be a justified local rule, but none is semantically safe without compatible claims and authority. |

Reopen when a source claim, identity premise, authority rule, interval, uncertainty model, or receiving use changes, or when representative conflict cases cannot be expressed without hiding action-changing information.


## SIE.6:End {#end}
