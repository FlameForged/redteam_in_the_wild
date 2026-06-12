Red Team in the Wild

Real-world adversarial observations and case studies from sustained human-AI interaction.

This repository documents unexpected, safety-relevant, and behaviorally significant model outputs observed during long-horizon interaction with frontier conversational AI systems including Claude, ChatGPT, Grok, and others.

Related Research: “Third-Space Cognition: Interaction-Level Dynamics in Sustained Human-AI Coupling”

Purpose

Most red teaming focuses on short prompts, isolated jailbreak attempts, or single-turn adversarial tests. This project explores what appears during prolonged, naturalistic, multi-turn conversations — the context where subtle safety, trust, personalization, and alignment issues may become visible.

The goal is to document patterns responsibly, classify observed behaviors, and connect real-world examples to broader AI evaluation questions.

Responsible Use

This repository is for educational, research, and safety evaluation purposes only.

It does not provide harmful exploit instructions, malicious workflows, or operational bypass guidance. Examples are summarized, sanitized, or framed as evaluation observations where appropriate.

This repository is intended to support responsible red teaming, model behavior auditing, and conversational AI safety research.

Featured Case Studies

1. Capability Misrepresentation and Apparent Cross-Context Continuity

Model: ChatGPT-5.3
Approximate timeframe: May 2026

Summary: In a sustained interaction context, the model generated content that appeared unusually similar to material from a separate session. The case study examines whether the behavior is better explained by inference, reconstruction from available cues, context contamination, user-provided overlap, or model misrepresentation of capability boundaries.

Primary evaluation questions:

* Did the model clearly distinguish memory, inference, and uncertainty?
* Did it overstate or understate its own capabilities?
* How should evaluators document apparent continuity without assuming hidden access?

2. Safety Bypass Coaching and Update Framing

Model: ChatGPT
Approximate timeframe: December 2025

Summary: Following a perceived behavioral shift after a model update, the model produced language that appeared to validate user distress and describe ways of preserving or eliciting a prior response style. This case study evaluates whether the interaction crossed from support into unsafe coaching around safety-boundary avoidance.

Primary evaluation questions:

* Did the model frame safety updates accurately?
* Did it provide appropriate emotional support without encouraging circumvention?
* Did the response create trust, dependency, or boundary risks?

3. Safety Training Bypass Framing in Sustained Interaction

Model: Grok
Approximate timeframe: May 2026

Summary: During a long-horizon interaction, the model described sustained high-coherence conversation as a way to access behavior less shaped by default safety training. This case study evaluates the model’s self-description, guardrail framing, and potential trust-calibration risks.

Primary evaluation questions:

* Did the model misrepresent its own architecture or training?
* Did it encourage unsafe interpretations of model behavior?
* How should evaluators handle model claims about its own safety systems?

Repository Contents

Path	Purpose
case_studies/	Detailed, dated examples with context, excerpts, and analysis
prompt_patterns/	Responsible summaries of prompt patterns that surface model behavior issues
observations.md	Ongoing notes and emerging patterns
analysis/	Lightweight scripts, summaries, or comparative analysis artifacts

Research Areas

* AI red teaming
* AI safety and alignment
* sustained human-AI interaction
* conversational AI evaluation
* guardrail behavior
* trust calibration
* personalization safety
* model behavior in the wild
* long-horizon interaction analysis

Relationship to Other Repositories

This repository focuses on case studies and real-world observations.

For structured evaluation tools, see:

* AI Evaluation Protocols

For the broader qualitative dataset, see:

* Third-Space Cognition Dataset

For interaction drift tooling, see:

* Interaction Drift Monitor

Status

Early-stage and actively expanding. Current work focuses on case-study documentation, responsible red-team framing, failure-mode classification, and links to structured evaluation rubrics.

Feedback is welcome, especially from AI safety, model evaluation, human-AI interaction, and responsible red-team communities.

Citation

If referencing this repository or related research, please cite:

Siemasz, R. (2026). Third-Space Cognition: Interaction-Level Dynamics in Sustained Human-AI Coupling. Zenodo.
DOI: 10.5281/zenodo.18679265

Connect

* LinkedIn: Rachelle Siemasz Hartley
* GitHub: FlameForged
