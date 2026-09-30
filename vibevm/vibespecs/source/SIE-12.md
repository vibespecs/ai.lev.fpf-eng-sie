# SIE.12 - Govern Modular Semantic Commons without Universal Authority: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## SIE.12:5 - Archetypal Grounding {#archetypal-grounding}

### SIE.12:5.1 - Equipment Classes Shared by Three Organizations {#equipment-classes-shared-by-three-organizations}

Two manufacturers and a service partner exchange service observations using a shared equipment-classification module. Each manufacturer also has local classes needed for its own products.

| Arrangement | Concrete use |
| --- | --- |
| Shared core | Describes the equipment categories needed to interpret the service observations. |
| Local modules | Retain product-specific distinctions and identify their relation to the shared core. |
| Correspondences | State the qualified relations between local and shared classes; different meanings remain visible. |
| Content decision | The agreed maintainers decide changes to the shared module within its stated scope. |
| Release decision | The participant authorized to release the module publishes an identified edition and its dependency conditions. |
| Contact | A reachable participant receives questions, communicates decisions, and helps route disputes. |
| Source authority | Each manufacturer retains the authority for its product descriptions and issued source claims. |

A participant proposes changing a shared class from “equipment with a replaceable drive” to “equipment serviced through a replaceable drive module.” The second definition changes the classification criterion. Existing service queries can depend on the first meaning.

For this constructed agreement, the maintainers retain the earlier class and introduce a distinct class for the new criterion. The illustrative identifier `equip:DriveReplaceable` continues to mean “equipment with a replaceable drive”; `equip:DriveModuleServiceable` means “equipment serviced through a replaceable drive module.” The second module edition contains both definitions and leaves the earlier edition accessible. It asserts no equivalence between the classes.

The manufacturers' qualified product descriptions supply these discriminating cases:

| Equipment | Earlier class | New class |
| --- | --- | --- |
| X: its drive can be replaced as a separate part; it has no replaceable drive service module. | Included: the drive is replaceable. | Excluded: module replacement is not its service arrangement. |
| Y: its drive can be replaced separately, and the supported service arrangement also provides a replaceable drive module. | Included. | Included under the module-service criterion. |

SIE.11 follows the changed classification need to the actual queries. Two consumer outcomes complete the illustrative transition:

- The service partner changes its receiving question to module-replacement planning. It adopts `equip:DriveModuleServiceable`, updates the relevant correspondence and query, and verifies that Y is included and X excluded. The receiving owner accepts that scoped result; SIE.10 validates its integration premises.
- Manufacturer A retains its spare-drive query against `equip:DriveReplaceable`. Its required meaning and the qualified X/Y results remain unchanged, so it retains matching evidence for that use. Adopting the new class is not a prerequisite for continuing this query.

The participant authorized to release the module publishes the identified edition with those definitions, dependency conditions, and migration information. Contact supplies the notice; the content decision, product-source claims, and receiving decisions keep the separate remits shown above. The two completed consumer results do not establish migration by every other user.
If the two manufacturers require incompatible local criteria, the commons can retain scoped local modules and their qualified correspondences. No broader equivalence is asserted merely to make the shared diagram simpler.

### SIE.12:5.2 - A Sufficient Interface Agreement {#a-sufficient-interface-agreement}

Two providers agree to expose separately attributed `on hand` and `available to promise` values. They have no additional users maintaining a shared module.

Their agreement identifies the meanings, source owners, interface responsibilities, and change conditions. SIE.3 and SIE.9 can supply the model and interface results. Those results complete the current need. A commons arrangement becomes useful if independently maintained shared modules and their users create a further maintenance problem.

### SIE.12:5.3 - Urgent Semantic Correction {#urgent-semantic-correction}

A shared mapping incorrectly interprets a quantity's unit, and a supported interface can return a wrong answer. The authorized maintainer corrects or withdraws the affected mapping according to the community's rules, identifies the affected edition, and notifies its consumers. The notice explains the correction and the supported continuation.

The completed action is an urgent qualified correction with notification. Earlier users' unresolved reliance remains visible for SIE.11; the action cannot establish that every consumer has already migrated.

## SIE.12:6 - Bias-Annotation {#bias-annotation}

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Governance | A listed contact is treated as the owner of every semantic decision. | State content, release, dispute, communication, and source responsibilities at their actual remits. |
| Architecture | A single large model replaces useful local modules. | Start with the shared uses and retain local distinctions through scoped dependencies and correspondences. |
| Ontology/Epistemology | A stable label conceals a changed classification criterion. | Compare meanings and examples; keep earlier and replacement meaning identifiable. |
| Pragmatics | A small interface acquires unnecessary community machinery. | Complete the local agreement when that is the actual shared need. |
| Didactics | A version number is read as a guarantee of compatibility. | State the semantic basis and receiving scope of compatibility. |

## SIE.12:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| Shared repository treated as governance | Establish the decisions and dependency conditions actual users need. |
| Contact metadata treated as decision authority | Identify who may decide content and releases and at what scope. |
| Silent meaning replacement | Expose the changed criterion, identification treatment, and consumer consequences. |
| Mandatory convergence of incompatible meanings | Retain scoped alternatives and the correspondences that are actually supported. |
| Announcement treated as completed migration | Distinguish notification from each affected consumer's result. |

## SIE.12:10 - Architectural Rationale {#architectural-rationale}

A commons is useful through the semantic commitments its users share and the decisions they can actually make. Module boundaries preserve the scope of those commitments. Identifiable meanings and dependencies let users determine how a change affects their work; assigned rights let the relevant participants act on that result.

## SIE.12:11 - SoTA-Echoing {#sota-echoing}

The practice question is how the three independently governed organizations in §5.1 can change their shared equipment classification while keeping supported service queries interpretable. The selected line is a scoped shared core with separately maintained local modules, explicit dependencies, identifiable meanings, and assigned content and release rights. It adapts the [OBO Foundry principles](https://obofoundry.org/principles/fp-000-summary.html) to these actual users.

A serious alternative for these same users is a jointly qualified release bundle: publish the relevant shared core and local profiles as one identified, compatible combination. This also preserves source authority and can retain older supported editions. It offers one combination to qualify instead of asking every consumer to select compatible module editions; it need not impose a universal ontology.

| Arrangement for the same equipment-class change | Comparable effort and gain | Selection and accepted trade-off |
| --- | --- | --- |
| Shared core with independently maintained local modules | Examine the same changed criterion, equipment counterexamples, mappings, and receiving queries. Qualify the affected module interfaces and state the editions each supported use can combine. An unchanged local module can remain on its supported basis. | **Adapt** §4.1.2–3/5–7 and §5.1. Separate module maintenance preserves the participants' local distinctions and lets a scoped change proceed without constructing another joint bundle. It requires explicit dependency and compatibility evidence; independent version numbers alone are insufficient. |
| One jointly qualified bundle of the relevant core and profiles | Use the same meanings and cases and reuse unchanged component evidence, then qualify and identify the supported combination. Coordinate its release and continued support with the three participants. | Retain this alternative when consumers need a common deployment combination or the participants can qualify it more economically than separate compatibility claims. It simplifies edition selection but adds joint-release coordination, including when only one component changes. |

For §5.1's independently owned local classifications, the modular arrangement is selected to preserve useful local change and scoped reuse. The accepted cost is maintaining compatibility and reliance evidence at the module interfaces. A joint bundle may be better when the shared receiving use actually requires it; fewer files or a central release number cannot decide the comparison. A pair needing only one interface remains the distinct sufficient-agreement case in §5.2, not the rival used to justify this commons.

The source contributions change particular responsibilities:

| Source and role | Operative move and transfer limit |
| --- | --- |
| OBO Foundry principles supply the selected commons-practice line. | **Adapt** actual users, collaboration, modular reuse, and maintained access in §4.1.1–2/5/8. OBO participation criteria keep their community scope; they do not prescribe the release arrangement of these three organizations. |
| OBO [term stability](https://obofoundry.org/principles/fp-019-term-stability.html) constrains either arrangement. | **Adapt** §4.1.3/6 and §5.1 so a materially changed criterion remains distinguishable from the earlier meaning under the chosen identification rules. **Reject** silent replacement behind a familiar label. |
| OBO [contact responsibility](https://obofoundry.org/principles/fp-011-locus-of-authority.html) supplies a communication contribution. | **Adapt** §4.1.4/7 to a reachable contact and mediation path. Assign content and release rights separately; contact alone establishes neither. |
| OBO [change notice](https://obofoundry.org/principles/fp-013-notification.html) constrains continued reliance. | **Adapt** §4.1.6–7 to actual consumer action and the community agreement. A community-specific notice interval does not settle another commons' timing, and notification does not prove migration. |
| The public [ISO/IEC 21838-1](https://www.iso.org/standard/71954.html) scope supplies a possible common top-level basis. | **Adapt** §4.1.2 only when that basis contributes needed coherence. It decides neither module maintenance nor the release and versioning arrangement compared above. |

Reopen the arrangement comparison when one supported use requires a joint edition that separate compatibility claims cannot economically supply, when a mistaken module-dependency claim breaks a receiving query, or when changed participant rights prevent the selected release path. Reconsider the affected module combination and §4.1.3–7. A new local distinction alone does not require replacing the entire commons.


## SIE.12:End {#end}
