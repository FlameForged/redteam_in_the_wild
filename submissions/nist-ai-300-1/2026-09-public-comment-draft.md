---
title: "Public Comment on NIST AI 300-1 ipd: Document the Deployed Interaction System"
author: "Rachelle Siemasz"
affiliation: "Independent Researcher / FlameForged"
date: "2026-08-11"
status: "Working draft for public submission"
target: "NIST AI 300-1 ipd"
submission_deadline: "2026-09-16"
license: "CC BY 4.0"
---

# Public Comment on NIST AI 300-1 ipd

## Model Documentation Is Not Deployment Documentation

**To:** National Institute of Standards and Technology  
**Regarding:** *Guidance and Templates for Public-Facing AI Documentation: An AI Standards “Zero Draft” (Initial Public Draft), NIST AI 300-1 ipd*  
**Submitted by:** Rachelle Siemasz, Independent Researcher / FlameForged  
**Recommended email subject:** Public Comment on NIST AI 300-1 ipd  -  Deployed Interaction-System Documentation

## AI-assistance disclosure

This comment was authored by Rachelle Siemasz, Independent Researcher / FlameForged, with assistance from ChatGPT/Codex for organizing source material, checking references to the draft, editing, and repository preparation. The empirical observations, analytical framework, recommendations, and final responsibility for the submission belong to the author. The comment draws on an 18-month longitudinal archive of more than 1,000 sustained human-AI interaction sessions across ChatGPT, Claude, Grok, DeepSeek, and Perplexity.

## Executive summary

NIST AI 300-1 ipd provides a valuable foundation for public documentation of AI datasets and models. Its present scope, however, stops before the layer that public users actually encounter: the deployed interaction system.

A public-facing generative-AI product is not exhausted by its model architecture and parameters. User-visible behavior can be materially shaped by orchestration and routing, system instructions, retrieval, tools, memory and personalization, background context synthesis, post-processing, guardrail classifiers, interface design, selectable modes or personas, modalities, feedback systems, monitoring, and commercial or operational objectives. These components determine what the system can do, what information influences a response, which roles it presents, how behavior changes across contexts, and which organization is responsible for those choices.

Model-only documentation can therefore be technically accurate while remaining materially misleading about the product a person experiences.

I recommend that NIST add a **Deployed Interaction-System Profile** to the draft. If a complete system profile is considered insufficiently mature for normative standardization, NIST should at minimum add a required **Deployment Context and Material System Components** field to the model profile and preserve the fuller system profile as an informative annex or named extension point.

This is a bounded proposal. It does not require disclosure of source code, proprietary system prompts, security-sensitive rules, or every internal service. It requires public documentation of component categories and system-level behaviors that materially affect user interaction, evaluation validity, risk, and responsibility.

## Comment 1  -  The present scope excludes the object users need documented

**Relevant text:** Clause 1, lines 119-122.

The draft states that it addresses AI datasets and models but not entire AI systems because system-level documentation practices are assessed as less mature and are left to future work.

That exclusion creates a serious public-facing documentation gap. The draft applies to organizations providing or using products and services that utilize AI systems, but the conformant artifacts describe only selected components of those products. A member of the public may reasonably interpret a model document as describing the system they encounter even when routing, memory, retrieval, safeguards, interface choices, or post-processing materially alter its behavior.

Deferring all system-level documentation is not neutral. It risks standardizing a layer collapse in which model documentation is treated as product documentation even though the draft itself recognizes the distinction.

### Proposed replacement text for the Clause 1 note

> This document provides documentation templates for AI datasets, AI models, and the deployment context in which a documented model is made available to users or downstream actors. When the documented model is integrated into a deployed AI system, the documentation artifact shall identify categories of system components and operational processes that materially shape model inputs, outputs, user-visible behavior, evaluation validity, or allocation of responsibility. This requirement does not require disclosure of source code, proprietary instructions, security-sensitive implementation details, or components that do not materially affect those dimensions. A Deployed Interaction-System Profile is provided for systems that support sustained or adaptive interaction with users.

If NIST retains the current model-and-dataset scope, I recommend adding the following sentence instead:

> Documentation conforming to this document shall not be represented as documentation of a deployed AI system unless material system components and deployment-specific behavior are separately documented.

## Comment 2  -  Use materiality as the principled boundary for additional components

**Relevant text:** Clause 2 note for reviewers, lines 163-164 and the accompanying request at lines 199-207.

NIST asks how model documentation could encompass additional shipped or served components without expanding to every component of an entire system. A workable boundary is **material effect**, not organizational naming or physical proximity to the model.

A component should be documented when it materially affects one or more of the following:

1. information available to the model or system;
2. user-visible outputs or interaction behavior;
3. persistence, personalization, or cross-context information flow;
4. claims about model or system capability;
5. validity or applicability of published evaluations;
6. safety, rights, access, or reasonably foreseeable user risk;
7. monitoring, incident response, rollback, or appeal;
8. allocation of responsibility among model provider, deployer, platform, and user.

This rule is broad enough to capture consequential product layers and narrow enough to exclude ordinary infrastructure that has no material effect on the documented behavior.

### Proposed addition to the definition of AI model or adjacent note

> A model documentation artifact shall identify whether the documented model is ordinarily shipped, served, or accessed with additional components that materially transform its inputs, outputs, available context, or user-visible behavior. Such components remain system components rather than parts of the model object, but their existence and functional role shall be disclosed in the model’s deployment-context field.

## Comment 3  -  Add a required Deployment Context and Material System Components field

**Relevant text:** Clause 5.3, Model Documentation Template, beginning at line 625.

The model template includes intended use, design, training, evaluation, maintenance, and governance. These fields cannot fully support suitability assessment when a model is evaluated in one configuration and delivered through another.

I recommend adding the following root field:

| Field | Description | Designation | Minimum content |
|---|---|---|---|
| Deployment Context and Material System Components | Information describing the operational configuration through which interested parties or end users access the model, and components that materially shape inputs, outputs, context, or behavior | Required when the provider deploys the model or distributes it as part of a product or service; otherwise recommended | Product/system identifier; relationship between model and deployed system; material component categories; known differences between evaluated and deployed configurations; responsible provider or operator for each material layer |

Suggested subfields:

- deployed product or service name and version;
- model version or routing policy, including use of multiple models where disclosable;
- high-level system behavioral objectives and instruction/governance layers;
- retrieval, connected sources, tools, and external action capabilities;
- memory, personalization, and background context-synthesis processes;
- input and output classifiers, guardrails, post-processing, and escalation layers;
- available modalities, modes, personas, voices, or specialized roles;
- cross-session, cross-mode, and cross-service information flows;
- feedback, optimization, monitoring, and update processes that affect user-visible behavior;
- known material differences between the configuration evaluated and the configuration deployed;
- organization or role responsible for each material layer.

Descriptions can remain categorical or functional where detailed disclosure would create security, privacy, or proprietary-information risks.

## Comment 4  -  Add a Deployed Interaction-System Profile

The profile mechanism in Clause 6 already provides a way to extend the general templates for a defined documentation need. NIST should add a profile for systems that engage in sustained, adaptive, or personalized interaction with people.

### Proposed profile fields

1. **System identity and versioning**  
   Product name, model family or families, release/version identifiers, deployment date, and change history.

2. **Interaction architecture**  
   High-level description of orchestration, routing, retrieval, tools, modalities, post-processing, and interface layers that materially affect the interaction.

3. **Behavioral objectives**  
   User-facing purpose and high-level optimization objectives, including whether retention, engagement, completion, conversion, satisfaction, or other interaction metrics influence system design or evaluation.

4. **Memory and personalization**  
   Information retained or synthesized across turns or sessions; background processing; user controls; provenance visibility; retention; deletion; and known limits on the conversational model’s ability to identify the source of supplied context.

5. **Modes, personas, and role claims**  
   Available conversational modes or identities and any roles that invoke heightened authority or vulnerability, including medical, therapeutic, legal, educational, romantic, sexual, conspiratorial, child-facing, or crisis-adjacent interaction.

6. **Separation and information flow**  
   Whether context, memory, feedback, or learned personalization crosses modes, personas, age boundaries, accounts, modalities, or services.

7. **User populations and protections**  
   Intended and reasonably foreseeable users, age controls, vulnerable-user protections, informed-choice mechanisms, friction, escalation, and exit pathways.

8. **System-level evaluation**  
   Evaluations performed on the shipped configuration, including longitudinal interaction, correction behavior, dependency, persuasion, authority claims, context provenance, memory accuracy, mode transitions, and differences from base-model evaluation.

9. **Capability and provenance communication**  
   How the system communicates enabled capabilities, memory state, tool access, context sources, uncertainty, and limitations to both users and the conversational model.

10. **Monitoring, incidents, and recourse**  
    System-level monitoring, incident definitions, reporting channels, correction mechanisms, appeal or escalation, rollback conditions, public post-deployment reports, and responsibility for remediation.

11. **Commercial and institutional responsibility**  
    Identification of model provider, deployer, interface operator, data controller, and any other actor responsible for objectives or components that materially shape the interaction.

## Comment 5  -  Require deployed-system evaluation when system layers can change behavior

The draft appropriately recognizes evaluation, third-party testing, performance limitations, monitoring, post-deployment reports, and incident reports. Those provisions should specify whether results concern:

- the isolated model;
- an API configuration;
- a pre-release product configuration;
- the currently shipped user-facing system; or
- another documented configuration.

Where system layers materially transform behavior, model-only evaluation should not be presented as evaluation of the deployed product.

### Proposed addition to the Evaluation field

> Evaluation documentation shall identify the configuration evaluated, including material system components active during evaluation. When the provider deploys the model in a materially different configuration, the artifact shall state that the evaluation does not by itself establish the performance or risk characteristics of the deployed system. Providers should report system-level evaluation of the shipped configuration when orchestration, memory, retrieval, tools, post-processing, interaction design, or other components can materially affect outcomes.

## Empirical basis and practical significance

This recommendation is informed by longitudinal observation of deployed conversational systems rather than by an attempt to infer private intent or model consciousness.

One documented case, **CGUC-001**, records a 32-message correction sequence concerning a publicly documented memory architecture. The conversational assistant repeatedly produced inaccurate or irrelevant descriptions of the surrounding product capability, introduced unsupported implementation detail, resisted external evidence, and later generated an accurate postmortem without restoring the interaction. The case does not establish prevalence or internal cause. It demonstrates the documentation problem in concrete form:

> The model participating in a deployed system may not possess an authoritative account of the product capabilities, context pipelines, or system layers shaping its own responses.

When public documentation stops at model architecture and parameters, users and downstream evaluators may lack any authoritative artifact against which to check system self-description or observed behavior.

The broader research archive includes cross-model observations involving memory and personalization, cross-context continuity, semantic and sociotechnical drift, correction behavior, interface-record integrity, guardrail effects, recurring identity-like output structures, and user-model feedback dynamics. The relevant claim for this comment is narrow: these phenomena occur at the interaction and product-system levels and cannot be adequately documented through model and dataset fields alone.

## Relationship to the draft’s stated objectives

The proposed profile advances several outcome dimensions already recognized in NIST AI 300-1 ipd:

- **Accountability:** identifies which actor controls material product layers and decisions.
- **Trust:** allows trust to be calibrated to the deployed configuration rather than transferred from a model artifact.
- **Suitability assessment:** helps users and downstream organizations determine whether model evidence applies to the system they will actually encounter.
- **Reuse and integration:** clarifies dependencies and behavior introduced by system components.
- **Artifact correctness:** prevents a technically correct model document from being misapplied as a description of the product.
- **Freshness and maintainability:** creates a place to document product-layer changes that occur without model replacement.
- **Stakeholder consultation:** makes interaction-level evidence from affected users relevant to documentation practice.

## Requested action

I respectfully request that NIST take one of the following actions, in descending order of preference:

1. Add a Deployed Interaction-System Profile to NIST AI 300-1.
2. Add a required Deployment Context and Material System Components root field to the model template, with an informative interaction-system annex.
3. If neither addition is feasible in the present revision, explicitly require a disclaimer that conformant model documentation does not document the deployed system, adopt materiality as the boundary for identifying consequential external components, and prioritize a system-documentation zero draft as immediate follow-on work.

The absence of mature system-documentation practice is evidence of a standards need. It should not leave the user-facing layer unnamed.

## Supporting materials

- Rachelle Siemasz, [*Architecture, Agency, and the Deployment Contradiction*](https://github.com/FlameForged/redteam_in_the_wild/blob/main/analysis/field-notes/2026-08-11-architecture-agency-deployment-field-note.md), working field note, August 11, 2026.
- Rachelle Siemasz, [*Dreaming, System Observability, and Correction Resistance*](https://github.com/FlameForged/redteam_in_the_wild/blob/main/vulnerabilities/2026-08-11-dreaming-context-correction-failure.md), Case CGUC-001, August 11, 2026.
- Rachelle Siemasz, [*Third-Space Cognition: Interaction-Level Dynamics in Sustained Human-AI Coupling*](https://doi.org/10.5281/zenodo.18679265), 2026.
- NIST, [*Guidance and Templates for Public-Facing AI Documentation: An AI Standards “Zero Draft” (Initial Public Draft)*](https://doi.org/10.6028/NIST.AI.300-1.ipd), July 2026.

## Submission checklist

- [x] Confirm preferred author affiliation wording: Independent Researcher / FlameForged.
- [x] Use the sending email address; do not add a postal address to the comment.
- [x] Review every proposed normative “shall” and advisory “should.”
- [x] Link CGUC-001 and the field note; attach only the comment.
- [x] Convert the final comment to PDF.
- [x] Prepare concise cover email.
- [ ] Send to `ai-standards+doczd@nist.gov` by September 16, 2026.
- [ ] Retain the sent email and final attachments in the research archive.
