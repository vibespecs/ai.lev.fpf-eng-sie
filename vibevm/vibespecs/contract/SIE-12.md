# SIE.12 - Govern Modular Semantic Commons without Universal Authority {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Eternal alpha
> **Normativity:** Normative method guidance within SIE; examples are constructed and non-normative.
>
> **Primary working result:** a `ModularSemanticCommonsAccount@Community` describing how actual users maintain and rely on shared semantic modules, their dependencies, decisions, and releases.

## SIE.12:1 - Problem Frame {#problem-frame}

**Use this when** independently governed participants depend on shared semantic modules and need an arrangement for maintaining them. A typical failure is a changed shared term whose consumers cannot determine who could approve the change, which meaning their interface uses, or how to migrate.

Start with one module and the uses that actually depend on it. Establish its scope, who can decide its content and release, and how its users can obtain an identifiable maintained edition. The first useful result is an agreement through which those participants can make and use a concrete module change.

The object is the shared maintenance and reliance arrangement for semantic modules. The gain is continued reuse with explicit local commitments, contribution rights, dependencies, and change consequences. A compatibility claim covering additional users needs support for those users' relevant reliance.

A team or a pair maintaining one interface can use its ordinary model and interface agreement when that suffices. A repeated file or shared repository alone does not establish a commons that needs this Method.

## SIE.12:2 - Problem {#problem}

Reusable semantic assets acquire users outside their original project. A term, class, relation, or mapping then carries assumptions into interfaces maintained by other participants. Changes can break those assumptions even when the shared file remains available.

One response is to require every participant to adopt one centrally controlled model. Another is to allow local changes without a recoverable relation to the shared meaning. Both can defeat useful reuse: the first can suppress necessary domain distinctions, while the second makes compatibility impossible to assess.

## SIE.12:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Shared meaning | Common modules reduce repeated work, while participants retain distinct purposes and source authority. |
| Local development | Extensions can answer local questions, while consumers need to know which shared commitments still hold. |
| Decision rights | Maintainers need power to release a module, while contact or repository access alone cannot establish that remit. |
| Stability | Identifiable meanings support reliance, while mistakes and changed requirements need correction. |
| Participation | Open contribution can improve coverage, while unresolved proposals still need a usable decision path. |

## SIE.12:4 - Solution {#solution}

Define the smallest shared module arrangement that serves the actual users. Make its semantic scope, decisions, dependencies, and releases usable in their integration work. Preserve local modules and disagreement where convergence is unnecessary or unsupported.

### SIE.12:4.1 - Pattern-Use Unfolding {#pattern-use-unfolding}

1. **Identify the shared use.** Name the users and questions that depend on the module. Locate the semantic content they share and the local distinctions they still need. If the actual need is only one interface agreement, complete that agreement through the relevant SIE Methods.
2. **Set module boundaries.** State the module's domain, concepts and relations, intended uses, material exclusions, and relation to local extensions. Use SIE.3 for content that needs model development and SIE.4 for qualified correspondences between different module meanings.
3. **Establish identification and dependencies.** Choose namespaces or identification practices that let consumers recover the intended term or module meaning. Identify editions and the dependencies each supported use needs. A permitted version range must have a semantic compatibility basis for its claimed use.
4. **Assign the decisions and communication.** State who may propose changes, decide module content, release an edition, resolve a disagreement under the community's rules, and communicate with users. Record the actual remit of each responsibility. A source owner retains its source meaning and issuance authority.
5. **Make contribution workable.** Give a proposer enough guidance to supply the changed meaning, rationale, examples, affected modules, and known consumer consequences. Route the proposal to the people authorized to decide it. Keep an unresolved disagreement explicit and permit a scoped local extension or alternative module when it can serve its users honestly.
6. **Prepare the release for its consumers.** Identify material semantic changes and use SIE.11 for affected reliance. Provide the edition, access, dependency conditions, and migration or deprecation information needed by those users. Distinguish a clarification from a changed meaning; preserve a way to identify the earlier meaning when consumers still rely on it.
7. **Notify and maintain at the agreed scope.** Give affected users notice that permits the action required by their dependency and the community agreement. Maintain a responsive contact and a workable path for corrections. An urgent correction may require immediate qualified publication and notification; describe the resulting limits honestly.
8. **Return the usable arrangement.** Show how the named participants can obtain a module, propose a change, decide and release it, and interpret the effect on their supported uses. An unresolved decision right or dependency limits the part of the commons that can be claimed as governed.

These responsibilities can fit a small agreement for a small commons. Broader participation adds work only where additional semantic dependence or decision needs arise.

### SIE.12:4.2 - Record the Result {#record-the-result}

| Arrangement position | Content used by participants |
| --- | --- |
| Shared module and users | Semantic scope, supported uses, and the participants who depend on it. |
| Local relationship | Extensions, maintained correspondences, disagreements, and the commitments claimed across module boundaries. |
| Identification and dependencies | Namespaces or equivalent identifiers, recoverable editions, access, and dependency or compatibility conditions. |
| Decisions and communication | Proposal, content, release, dispute, and contact responsibilities at their actual remit. |
| Change and continued use | Material-change assessment, notices, correction, migration, deprecation, and maintained access needed by consumers. |

Refer to existing module definitions and working agreements when they supply this content. The account makes the arrangement recoverable; it need not reproduce every module or introduce a separate record for each responsibility.

### SIE.12:4.3 - What Changes in Practice {#what-changes-in-practice}

A user can identify the meaning and edition its interface consumes and find the decision needed for a proposed change. Maintainers can release a scoped improvement while preserving the commitments they claim to retain. Participants can keep different local meanings through explicit module boundaries and correspondences.

## SIE.12:7 - Conformance Checklist {#conformance-checklist}

- [ ] Actual users and their shared-module reliance justify the arrangement.
- [ ] The shared scope and local extensions preserve the commitments they claim to use.
- [ ] Consumers can identify the model meaning, edition, access, and applicable dependencies.
- [ ] Proposal, content, release, dispute, contact, and source responsibilities are distinguishable where they matter.
- [ ] A material change has a usable decision and affected-consumer path.
- [ ] Identification, notice, migration, and deprecation follow the chosen rules and actual use consequences.
- [ ] A local interface can finish without creating an unnecessary commons.
- [ ] Unresolved rights or reliance limit the corresponding claimed arrangement.

## SIE.12:9 - Consequences {#consequences}

Shared modules can evolve while their users retain identifiable meanings and workable returns. Local development remains possible, and a community can decide changes without claiming authority outside its remit.

The arrangement costs maintenance, communication, and change assessment. Those costs increase with real dependency and participation. Some proposals remain local or unresolved when shared convergence cannot be justified.

## SIE.12:12 - Relations {#relations}

- SIE.3 develops or qualifies module content; SIE.4 establishes correspondences between different meanings.
- SIE.5 retains identifier authority and grain when identity is actually a premise.
- SIE.9 supplies the receiving interfaces that consume shared modules.
- SIE.11 follows material semantic change to affected results and users; SIE.10 supplies their integration validation.
- Domain authorities retain source meanings and claims. ME contributes Method introduction or revision when the community is changing how it works.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): Actual shared-module uses; spec://ai.lev/fpf-eng-sie/contract/SIE-3#root, spec://ai.lev/fpf-eng-sie/contract/SIE-4#root, and spec://ai.lev/fpf-eng-sie/contract/SIE-11#root when their results are needed @status:spec/done

#source spec://ai.lev/fpf-eng-sie/source/SIE-12
