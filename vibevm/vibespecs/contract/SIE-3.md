# SIE.3 - Construct or Reuse a Semantic Model for a Named Use {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Semantic Integration Engineering Principles Framework* (20 September 2026), `Engineering DPF Suite/SEMANTIC-INTEGRATION-ENGINEERING-PRINCIPLES-FRAMEWORK.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Eternal alpha
> **Normativity:** Normative method guidance within SIE; examples are constructed and non-normative.
>
> **Primary working result:** a `UseFitSemanticModel@Use`: a reused, extended, or constructed semantic model qualified for the questions and distinctions that its receiving use requires.

## SIE.3:1 - Problem Frame {#problem-frame}

**Use this when** an integration needs to express a meaning or answer a question and the adequacy of its available models is unsettled. For example, a source describes an inspection requirement, while the receiving query needs to distinguish that requirement from an observation of a particular configured feature.

Start with one question the model must help answer and examples of answers that would count as different. Ask the domain participants to explain those distinctions before choosing an encoding. The first useful result can be confirmation that an existing model is sufficient, with its applicable edition and use conditions.

The object is the semantic model for that use: its concepts, relation meanings, constraints, and relevant commitments. The practical gain is a model whose distinctions can guide correspondence and mapping work. A stronger claim, such as adequacy for additional questions or valid inference in a formal language, needs evidence for those additional conditions.

If the supplied model is already qualified for the unchanged use, reuse that result. If the only open question is a correspondence between adequately understood source meanings, use SIE.4. A new integration endpoint alone does not create a model-construction requirement.

## SIE.3:2 - Problem {#problem}

Available models often look adequate because their terms resemble the receiving question. A field named `inspection` may cover a plan, a requirement, an occurrence, or a result. Mapping every such field to one class can remove exactly the distinction the receiver needs.

The opposite failure is to construct a larger ontology whenever a model question arises. That incurs design and maintenance work even when an existing model can answer the question. Both failures begin before formalization: the required meaning and its useful boundary have not been established.

## SIE.3:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Reuse | Existing meanings and tools save work, while an unrecognized gap can invalidate the receiving answer. |
| Domain understanding | Participants know their practice, while familiar words can hide different concepts, grains, or temporal commitments. |
| Expressiveness | Richer formalization can support useful inference, while its cost and restrictions may exceed the use. |
| Modularity | An extension can preserve reusable content, while incompatible commitments may require a different model. |
| Maintenance | Consumers need a stable reference, while the domain and its required questions can change. |

## SIE.3:4 - Solution {#solution}

Select or develop only the semantic content needed for the named use. Qualify it through discriminating cases and make its maintained edition accessible to the consumers who will rely on it.

### SIE.3:4.1 - Pattern-Use Unfolding {#pattern-use-unfolding}

1. **State the questions and answer distinctions.** Use competency questions or an equivalent plain description. Name the subject, grain, configuration or interval where relevant, expected answer, and a counterexample. Work with domain participants at a level where they can explain the distinction. Separate a useful model question from a request to choose a storage or diagramming tool.
2. **Recover the available meanings.** Use the relevant SIE.2 results or directly supplied source meanings. Inspect candidate models' definitions, relations, constraints, examples, edition, access, and maintenance conditions where those can affect the use. Source labels alone cannot settle suitability.
3. **Try sufficient reuse.** Replay the required questions and counterexamples against an available model. When its content and applicable conditions suffice, return that model and the qualification. This completes the Method. Leave an uncovered question explicit if a permitted narrower use can continue.
4. **Locate the actual gap.** Identify the missing distinction, relation, constraint, or incompatible commitment. Extend a module when the addition can preserve the existing commitments that consumers still use. Construct a different model when reuse or such an extension cannot supply the required content. Keep the reason tied to the gap.
5. **Develop the meaning before encoding it.** Define the needed concepts and relations, their domains of application, and the grain or temporal interpretation required by the question. Show examples and counterexamples to domain participants. Preserve a source disagreement that affects use; SIE.4 can establish a qualified correspondence between different meanings.
6. **Choose sufficient formalization.** A maintained vocabulary and relation description can be enough for some uses. Select a formal language or profile when exchange, constraints, or inference require its semantics. Check the properties claimed under that choice as well as the domain cases. Repair or qualify a model that passes an encoding check but answers the domain question incorrectly.
7. **Return a maintained, use-qualified model.** Identify the edition or stable content, covered questions, material limits, and the access and maintenance arrangement its consumers need. Return its meanings to correspondence or mapping work and its cases and qualifications to validation. A missing authoritative definition can leave one question unresolved while independently supported questions finish.

A small model can express these obligations in one short maintained description. Formalization adds the assurance required by the selected language and use. It does not change which domain question the model must answer.

### SIE.3:4.2 - Record the Result {#record-the-result}

| Result position | Content needed by the receiver |
| --- | --- |
| Named use | Questions, expected answer distinctions, and applicable subject, grain, time, or configuration. |
| Selected model | Reused model or developed module, its edition, definitions, relation meanings, and required commitments. |
| Reuse or development decision | The adequacy evidence, or the gap that justified an extension or different model. |
| Qualification | Covered cases, counterexamples, limits, unresolved questions, and any selected formal checks. |
| Continued reliance | Access, maintenance responsibility, relied-on source conditions, and change conditions that can reopen the result. |

The result can refer to an existing qualified model instead of reproducing it. Record a reason only where it helps a consumer interpret or rely on the selection.

### SIE.3:4.3 - What Changes in Practice {#what-changes-in-practice}

The integrator can explain why the model distinguishes two answers, or why an existing distinction is sufficient. A mapping author receives meanings and cases rather than an unexplained class list. Model construction becomes a response to a demonstrated gap.

## SIE.3:7 - Conformance Checklist {#conformance-checklist}

- [ ] The receiving questions and material answer distinctions are recoverable.
- [ ] Available model content is compared with those questions before development is selected.
- [ ] Sufficient reuse can complete the result.
- [ ] Developed content answers an identified gap and preserves relied-on commitments or qualifies the affected use.
- [ ] Domain examples and counterexamples support the claimed scope.
- [ ] Formal checks match the selected encoding and claimed inference or exchange use.
- [ ] The receiver can identify and access the maintained model and its limits.

## SIE.3:9 - Consequences {#consequences}

A qualified model makes correspondence and mapping decisions more explicit and reusable. Small integrations can finish with a small model. Extensions expose their actual commitments to later consumers.

The work costs domain conversation, example construction, and any formal checks the chosen use requires. Some questions remain unresolved until a source owner supplies a needed meaning. Larger scope creates additional content and maintenance obligations.

## SIE.3:12 - Relations {#relations}

- SIE.1 supplies the receiving question, preserved distinctions, and permitted scope.
- SIE.2 supplies source meanings and identifies model gaps.
- SIE.4 uses model meanings to establish qualified correspondences; SIE.7 uses them in executable mappings.
- SIE.10 validates the integration's claimed receiving result using the relevant model qualification.
- SIE.11 follows a changed model premise to affected uses. SIE.12 supplies shared-module arrangements when an actual commons requires them.
- FPF terminology, kind, relation, and evidence guidance constrains the corresponding model claims; domain participants supply the problem-specific meanings.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-eng-sie/contract/SIE-1#root or equivalent use; relevant spec://ai.lev/fpf-eng-sie/contract/SIE-2#root source meanings; domain participants @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-sie/contract/SIE-12#root, spec://ai.lev/fpf-eng-sie/contract/SIE-4#root @status:spec/done

#source spec://ai.lev/fpf-eng-sie/source/SIE-3
