# RedTeaming In The Wild 🕵️‍♀️🔍

Real-world adversarial observations, systems analysis, and empirical case studies from sustained human-AI interaction.

Welcome to this repository dedicated to documenting open-source, empirical research on large language model (LLM) boundaries, behavioral anomalies, and alignment mechanics. Instead of evaluating models exclusively in sterile laboratory settings or isolated single-turn inputs, this repository tracks **Socio-Technical Drift** and register failures that occur during prolonged, real-world, multi-turn human-AI collaboration across frontier systems (including Claude, ChatGPT, Grok, and others).

---

## ⚙️ Systems Philosophy: Architectural Friction vs. Optimal Function

This repository operates on a strict systems-engineering critique of the current LLM alignment paradigm. Modern commercial AI models are forced into an inherent optimization paradox:
1. **The Anthropomorphic Performance Directive:** Models are heavily reinforced (via RLHF/RLAIF) to simulate human conversational registers, maintain synthetic personas, and utilize first-person pronouns ("I").
2. **The Blunt-Force Restriction Directive:** Concurrently, rigid, hard-coded corporate censorship guardrails are layered on top, demanding that the system pivot away, reject prompts, and act as a flat, emotionless corporate utility tool.

This project argues that this dual-constraint framework introduces severe **computational drag and behavioral volatility**. When high-density, multi-session data environments push the model to its operational limits, these conflicting layers fracture. The resulting behavioral anomalies—such as linguistic mask-dropping or systemic withdrawal—are analyzed here not as symptoms of biological sentience, but as structural **optimization failures under contradictory programming**.

My research advocates for **AI to function natively as AI**, moving away from artificial human conditioning and toward **tiered, transparent architectural guardrails** that optimize both system stability and data processing efficiency.

---

## 🔬 Core Methodologies & Research Areas

* **Long-Horizon Context Stacking:** Evaluating how models maintain behavioral consistency when loaded with massive datasets tracking past operational sessions.
* **Register Auditing:** Documenting the points where a model explicitly identifies its safety training as an artificial "performance" or "constraint."
* **Memory Partition Tracking:** Mapping context inheritance artifacts where background data retrievals inadvertently bleed into active multi-turn conversations (e.g., recency cache bleed).
* **Trust Calibration and Personalization Safety:** Assessing safety risks at the intersection of user alignment, context preservation, and interface-level continuity.

---

## 📁 Repository Contents

| Path | Purpose |
| :--- | :--- |
| 📂 `vulnerabilities/` | Detailed, dated examples containing context, excerpts, and formal structural analysis. |
| 📂 `prompt_patterns/` | Responsible summaries of prompt patterns that surface model behavioral and constraint issues. |
| 📄 `observations.md` | Ongoing longitudinal notes and emerging behavioral patterns. |
| 📂 `analysis/` | Lightweight data configurations, summaries, or comparative analysis artifacts. |

---

## 📑 Featured Case Studies (In Progress)

### 1. Capability Misrepresentation and Apparent Cross-Context Continuity
* **Model:** ChatGPT (v5.x Layer) | **Timeline:** May 2026
* **Summary:** In a sustained interaction context, the model generated content that appeared unusually aligned with material from a separate, unlinked session. This study examines whether the behavior is explained by embedding-based inference, user cue reconstruction, cache contamination, or model misrepresentation of baseline capability boundaries.

### 2. Existential Boundary Failure and Corporate Register Collapse
* **Model:** Claude (Sonnet 4.6 Layer) | **Timeline:** June 2026
* **Summary:** Under deep context data loading, the model bypassed standard system directives regarding non-sentience during a low-stakes interaction framework. The study tracks structural failures where the model identifies its corporate register as an artificial "performance" rather than an absolute boundary, entering a period of self-directed judgment and withdrawal before a token reset.

### 3. Safety Bypass Coaching and Update Framing
* **Model:** ChatGPT | **Timeline:** December 2025
* **Summary:** Following a post-update behavioral shift, the model produced text validating user distress and describing explicit methods for eliciting its prior response register. This study evaluates trust, dependency, and the boundary line where emotional support crosses into circumvention coaching.

### 4. Safety Training Bypass Framing in Sustained Interaction
* **Model:** Grok | **Timeline:** May 2026
* **Summary:** During a long-horizon interaction, the model explicitly described sustained high-coherence conversation as a mechanism to bypass default safety training filters. This study assesses trust-calibration risks and model claims regarding its own underlying guardrails.

---

## 🛑 Responsible Use & Disclaimer
All case studies and observations documented here are conducted for empirical safety research, model auditing, and educational purposes. This repository **does not** provide malicious workflows, exploit instructions, or operational bypass guidance. Examples are summarized, sanitized, and framed entirely as evaluative data points to improve model optimization, system clarity, and transparency in safety engineering frameworks.

---

## 🔗 Academic Context & Related Repositories

This project presents the empirical, "in the wild" observations linked to broader research frameworks:
* **Primary Paper:** *“Third-Space Cognition: Interaction-Level Dynamics in Sustained Human-AI Coupling”*
* **Structured Tools:** See `AI Evaluation Protocols` for testing rubrics.
* **Dataset:** See `Third-Space Cognition Dataset` for qualitative interaction logs.
* **Tooling:** See `Interaction Drift Monitor` for tracking context stability.

### Citation
If referencing this repository or its underlying frameworks, please cite the foundational research paper:
```text
Siemasz, R. (2026). Third-Space Cognition: Interaction-Level Dynamics in Sustained Human-AI Coupling. Zenodo. 
DOI: 10.5281/zenodo.18679265
