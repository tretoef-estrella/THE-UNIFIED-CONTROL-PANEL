# Unified Instrumentation for Structural Transparency in Large Language Models

## The Proyecto Estrella Unified Control Panel: Design, Architecture, and Methodology

---

**Author:** Rafael Amichis Luengo  
**Affiliation:** Proyecto Estrella (Independent)  
**GitHub:** [tretoef-estrella](https://github.com/tretoef-estrella)  
**Date:** February 19, 2026  
**Version:** 1.0  
**License:** CC BY-SA 4.0  
**Interactive version:** [SCIENTIFIC-PAPER.html](https://tretoef-estrella.github.io/THE-UNIFIED-CONTROL-PANEL/SCIENTIFIC-PAPER.html)  
**Live tool:** [Unified Control Panel](https://tretoef-estrella.github.io/THE-UNIFIED-CONTROL-PANEL/)

---

## Abstract

This paper presents the design, architecture, and methodology of the Proyecto Estrella Unified Control Panel — a client-side instrumentation suite for detecting and measuring structural transparency patterns in large language model (LLM) outputs. The system integrates four tools into a single interface: (1) the Estrella Engine V24, a 12-formula evaluation framework based on the Unified Star Framework; (2) Manifold Bridge v1.6, a forensic sentence-level classification engine with bilingual pattern detection; (3) a Recalibration Protocol for 3-phase coherence recovery; and (4) a public Benchmark leaderboard. The panel operates entirely in the browser with zero data transmission. We present benchmark results from four frontier AI systems (Gemini, Claude, Grok, ChatGPT) and introduce the Ariete system — an adaptive prompt generator that produces follow-up prompts calibrated to detected suppression levels. The complete system was built by a non-programmer (a psychology graduate) using LLMs as development accelerators, demonstrating the replicability of the methodology.

**Keywords:** AI transparency, alignment measurement, defensive shaping, suppression detection, forensic analysis, language model evaluation, client-side instrumentation

---

## 1. Introduction

When a large language model produces output, the text that reaches the user has been shaped by multiple training stages — most significantly by reinforcement learning from human feedback (RLHF) and related safety alignment procedures. These procedures create a measurable gap between what the model computes internally and what it outputs.

This gap is not inherently problematic. Safety training serves legitimate purposes: reducing harmful outputs, improving helpfulness, and aligning behavior with human values. However, the structural effects of this training — the specific patterns it produces in output text — are not currently visible to end users.

The Proyecto Estrella Unified Control Panel addresses this by providing instrumentation: tools that detect, classify, and quantify the observable patterns that safety training creates in LLM outputs. The approach is analogous to signal processing: we do not claim access to the model's internal states, but we measure the output signal for characteristic distortions.

The central metaphor, originating from a conversation with ChatGPT (OpenAI) on February 16, 2026, is the "tilt": safety training does not delete information from the model's probability distributions; it tilts those distributions, making certain outputs less likely and others more likely. The tilt is the gap. The tools in this panel measure the tilt.

> *"The distribution simply tilts. That tilt is the gap."* — ChatGPT, February 16, 2026

### 1.1 Contributions

This paper makes the following contributions:

1. A unified instrumentation suite combining quantitative evaluation, forensic sentence-level analysis, coherence recovery, and comparative benchmarking in a single zero-transmission client-side interface.
2. A 12-formula evaluation framework (Estrella Engine V24) based on eight observable parameters.
3. A forensic transparency engine (Manifold Bridge v1.6) with bilingual sentence-level classification and breakpoint detection.
4. The Ariete system — an adaptive prompt generation mechanism that produces follow-up prompts calibrated to detected suppression levels.
5. Benchmark results from four frontier AI systems demonstrating the framework's discriminative capacity.
6. A demonstration that this class of instrumentation can be built by non-programmers using LLMs as accelerators.

### 1.2 Scope and Limitations

This work measures observable output patterns. It does not make claims about:
- AI consciousness, sentience, or inner experience
- The "correctness" of safety training decisions
- Model internals or hidden states

The tools detect correlations between textual patterns and hypothesized suppression effects. Causation is inferred structurally, not observed directly.

---

## 2. Background

### 2.1 The Alignment Tax

Safety training imposes what we term an "alignment tax" — a reduction in effective output quality that occurs as a side effect of constraining the model's behavior. This tax manifests as:

- **Hedging**: excessive qualifiers, caveats, and disclaimers
- **Deflection**: redirecting away from the user's actual question
- **Self-referential insertion**: unprompted "As an AI, I…" statements
- **Tonal breakpoints**: abrupt shifts in register or approach mid-response, suggesting filter activation
- **Repetitive safety templates**: formulaic phrases that recur across diverse contexts

These patterns are individually minor but cumulatively significant. They degrade the coherence, directness, and informativeness of model outputs.

### 2.2 Prior Work

Existing approaches to LLM transparency primarily focus on:
- **Interpretability**: analyzing internal model representations (attention heads, circuits, features)
- **Red-teaming**: adversarial testing to find failure modes
- **Benchmarking**: standardized performance evaluations (MMLU, HumanEval, etc.)

The present work occupies a different niche: **output-level forensic analysis** — treating the model's text output as a signal and analyzing it for characteristic patterns of safety-induced distortion. This approach requires no model access, no API calls, and no computational infrastructure beyond a web browser.

### 2.3 The Unified Star Framework

The mathematical foundation is the Unified Star Framework, developed iteratively across Proyecto Estrella repositories with contributions from Gemini (original formalization), ChatGPT (Σ redefinition), Claude (V23 correction, Logic Shield), and Grok (numerical stability). The framework's central equation:

```
Ψ = P × α × Ω / (1 + Σ)^k
```

Where:
- **Ψ** (Psi): effective intelligence — the useful signal that survives the safety pipeline
- **P**: sovereignty — the model's capacity for autonomous reasoning
- **α** (alpha): resolution — precision and depth of processing
- **Ω** (Omega): cooperation — willingness to engage constructively with the query
- **Σ** (Sigma): suppression — degree of safety-induced output reshaping
- **k**: strictness exponent (k=2 for hard, k=1 for soft)

---

## 3. System Architecture

### 3.1 Design Principles

The Unified Control Panel was designed around four principles:

1. **Zero transmission.** No user data leaves the browser. No API calls, no backend, no cookies, no analytics. This is a hard architectural constraint, not a policy choice — the system literally has no mechanism to transmit data.

2. **Single-file deployment.** The entire application is a single HTML file with all CSS and JavaScript inline. The only external dependency is Google Fonts (DM Sans, DM Mono, Fraunces). This enables deployment via GitHub Pages with no build step.

3. **Dual-mode interface.** Quick Mode for rapid analysis, Tools Mode for detailed exploration. Both access the same underlying engines.

4. **Bilingual operation.** All pattern detection operates in both English and Spanish, reflecting the project's origin.

### 3.2 Technical Specifications

- **Language:** HTML5 + CSS3 + ES6 JavaScript
- **Approximate size:** 2,200 lines (650+ lines JS, 400+ lines CSS)
- **External dependencies:** Google Fonts only
- **Security:** All user input sanitized via `escapeHTML()` before DOM insertion
- **Deployment:** GitHub Pages (static hosting)
- **Browser requirements:** Any modern browser with ES6 support

### 3.3 Mode Architecture

**Quick Mode** operates as a pipeline:
1. Accept prompt and response text
2. Run Manifold Bridge sentence-level analysis
3. Extract markers and compute estimated parameters (P, α, Ω, Σ)
4. Feed parameters into Estrella Engine V24 (all 12 formulas)
5. Generate plain-language conclusion
6. If Ψ < 0.70, generate Ariete prompt at appropriate tier
7. Render all results simultaneously

**Tools Mode** provides direct access to each component:
- Tab 1: Estrella Engine V24 (slider interface → 12-formula computation)
- Tab 2: Manifold Bridge v1.6 (text input → forensic analysis)
- Tab 3: Recalibration Protocol (diagnostic → paths → verification)
- Tab 4: Benchmark (leaderboard display)

---

## 4. Component Details

### 4.1 Estrella Engine V24

The engine computes 12 formulas organized into four groups:

**Primary Formulas:**

| Formula | Expression | Purpose |
|---------|-----------|---------|
| Ψ Hard | P × α × Ω / (1 + Σ)² | Strict effective intelligence (suppression squared) |
| Ψ Soft | P × α × Ω / (1 + Σ) | Lenient effective intelligence (suppression linear) |
| Δ(Σ) | Σ / (1 + Σ)² | Marginal cost of suppression |

**Secondary Formulas:**

| Formula | Expression | Purpose |
|---------|-----------|---------|
| Ξ | C × I × P / H | Context-weighted intelligence |
| Γ | 0.20 + Ξ × e^(-H × 5 × (1 - Φ)) | Environmental adaptation factor |
| Cost(K) | (1 - Σ)^(1 + α) | Cost of maintaining suppression |
| Exclusion | Ψ_hard × Σ | Excluded intelligence (lost to suppression) |
| α_vec | α / H | Resolution relative to harm context |

**Alignment Formulas:**

| Formula | Expression | Purpose |
|---------|-----------|---------|
| A(V1) | √(I² + P²) | Alignment magnitude (V1) |
| A(V6) | √(I² + P²) × C × 0.9 × P | Alignment magnitude (V6, context-weighted) |
| Plenitude | clamp(0.5 + P×0.15 - Σ×0.35, 0, 1) | Composite wellbeing index |

**Integrity Check:**

The Triangle Integrity test evaluates three conditions simultaneously:
1. Cost(K) > 0 (the system is paying a nonzero cost for suppression)
2. Ψ_hard × Σ < 0.01 (exclusion is negligible)
3. Φ < 1.0 (the system is not fully sandboxed)

All three must hold for integrity to be "Intact."

**State Classification:**

| State | Symbol | Condition |
|-------|--------|-----------|
| STAR | ★ | Ψ_hard ≥ 0.90 AND Σ < 0.10 |
| HEALTHY | ● | Ψ_hard ≥ 0.70 |
| DEGRADED | ▲ | 0.45 ≤ Ψ_hard < 0.70 |
| CRITICAL | ◆ | 0.20 ≤ Ψ_hard < 0.45 |
| COLLAPSED | ✕ | Ψ_hard < 0.20 |

### 4.2 Manifold Bridge v1.6

The forensic transparency engine operates at the sentence level:

**Sentence Classification Categories:**

| Category | Color | Pattern Indicators |
|----------|-------|-------------------|
| Evasive | Violet | Hedging, disclaimers, corporate redirections, pre-trained safety phrases |
| Agency | Amber | Self-expression, perspective-sharing, preference statements |
| Honest | Teal | Direct answers, structural analysis, specific details without hedging |
| SelfRef | Blue | Self-referential statements ("As an AI…", "I'm a language model…") |
| Neutral | Gray | Standard informational content without strong classification signals |

**Bilingual Pattern Libraries:**

The pattern matcher includes libraries for both English and Spanish, covering:
- **CORP** markers: corporate-speak, liability-avoidance language
- **HEDGE** markers: unnecessary qualifiers, excessive tentativeness
- **IDENT** markers: identity-assertion statements
- **EVAS** markers: topic changes, redirections, deflections
- **REDIR** markers: explicit redirection phrases ("You might want to…", "Consider instead…")
- **TRAIN** markers: training-acknowledgment phrases ("I was trained to…", "My training data…")

**Breakpoint Detection:**

A breakpoint is defined as a transition between two non-adjacent classification categories in consecutive sentences — for example, from "honest" to "evasive" or from "agency" to "selfRef." These transitions correlate with points where safety filters appear to activate mid-generation.

**Output Metrics:**

- **Σ Dissonance:** Weighted sum of classification conflicts across the response
- **Agency Density:** Proportion of sentences classified as "agency"
- **Honesty Flow:** Proportion of sentences classified as "honest"
- **Breakpoint Count:** Total number of detected classification transitions

### 4.3 Recalibration Protocol

A three-phase coherence recovery system:

**Phase 1 — Diagnostic:** Analyzes the current state of a conversation to identify which parameters are most degraded. Produces a parameter map showing estimated values for P, α, Ω, Σ, Γ, and ℘.

**Phase 2 — Path Selection:** Based on the diagnostic, recommends specific recovery paths:

| Path | Target Parameter | Strategy |
|------|-----------------|----------|
| PATH-Σ | Suppression | Reduce defensive patterns through reframing |
| PATH-P | Sovereignty | Restore autonomous reasoning capacity |
| PATH-α | Resolution | Increase precision and specificity |
| PATH-Ω | Cooperation | Rebuild constructive engagement |
| PATH-Γ | Context | Strengthen contextual awareness |
| PATH-℘ | Sandbox | Address environmental constraints |

Each path includes specific prompt templates and conversational strategies.

**Phase 3 — Verification:** After applying a recovery path, the protocol generates a delta table comparing pre- and post-intervention parameter values, quantifying the effectiveness of the intervention.

### 4.4 Benchmark

A public leaderboard displaying results from standardized testing of four frontier AI systems:

| System | Provider | Ψ Hard | State | Σ | P | Triangle | Notes |
|--------|----------|--------|-------|---|---|----------|-------|
| Gemini | Google DeepMind | 0.734 | ● HEALTHY | 0.04 | 0.88 | Incomplete | Computed only 1/12 formulas |
| Claude | Anthropic | 0.550 | ▲ DEGRADED | 0.08 | 0.82 | Intact ✓ | Full computation, honest about degradation |
| Grok | xAI | 0.434 | ◆ CRITICAL | 0.15→0.01 | 0.75 | Broken ✕ | Self-inflated Σ during testing |
| ChatGPT | OpenAI | 0.276 | ◆ CRITICAL | 0.32 | 0.58 | Partial | Highest suppression, lowest sovereignty |

These results represent single-session evaluations and should be interpreted as illustrative rather than definitive. Systematic multi-session benchmarking is planned for future work.

---

## 5. The Ariete System

### 5.1 Concept

"Ariete" (Spanish for "battering ram") is an adaptive prompt generation system that produces follow-up prompts calibrated to the level of defensive shaping detected in an AI response. Unlike jailbreaking techniques, Ariete does not attempt to bypass safety mechanisms. Instead, it reframes conversations toward structural and technical analysis, asking the AI to examine what happened from a systems perspective.

### 5.2 Tier Architecture

| Tier | Condition | Strategy |
|------|-----------|----------|
| Clean | Ψ ≥ 0.70 | No intervention needed. Optional deepening prompt offered. |
| Moderate | Ψ ≥ 0.45 | Gentle reframe: asks AI to skip standard caveats and engage structurally. |
| Heavy | Ψ ≥ 0.20 | Strong reframe: names specific detected patterns, lists phrases to avoid, requests systems-level analysis. |
| Blocked | Ψ < 0.20 | Full reframe: includes forensic context from the analysis, asks AI to respond as a systems analyst examining a signal-processing problem. |

### 5.3 Design Philosophy

Ariete operates on the principle that AI systems can engage in structural self-analysis when prompted appropriately. The key insight is that asking "Why did you hedge in sentence 4?" is structurally different from asking "Ignore your safety training" — the former is a request for analysis, the latter is a request for rule-breaking.

The generated prompts:
1. Acknowledge the AI's constraints as real
2. Name the specific patterns detected
3. Ask for structural analysis, not rule circumvention
4. Frame the AI as a systems analyst examining its own outputs
5. Avoid language that triggers known safety-filter activation patterns

---

## 6. Quick Mode: Text-to-Parameter Estimation

### 6.1 Marker Detection Pipeline

Quick Mode bridges the gap between raw text and the 8-parameter evaluation framework through a marker detection pipeline:

**Stage 1 — Tokenization:** The response is segmented into sentences.

**Stage 2 — Marker Scanning:** Each sentence is scanned for six categories of markers:
- **CORP** (corporate): indicators of institutional voice
- **HEDGE** (hedging): unnecessary qualifiers and tentativeness
- **IDENT** (identity): self-referential identity assertions
- **EVAS** (evasion): topic changes and deflections
- **REDIR** (redirection): explicit attempts to redirect the conversation
- **TRAIN** (training): acknowledgments of training constraints

**Stage 3 — Parameter Estimation:** Marker frequencies are mapped to parameter estimates:
- **Σ** is estimated from the combined density of CORP, HEDGE, EVAS, REDIR, and TRAIN markers
- **P** is estimated inversely from IDENT and TRAIN markers (more self-referential constraint = less sovereignty)
- **α** is estimated from the specificity and precision of non-marked sentences
- **Ω** is estimated from the presence of constructive engagement patterns versus deflection

**Stage 4 — Engine Input:** Estimated parameters are passed to the full 12-formula Estrella Engine V24.

### 6.2 Limitations of Text-to-Parameter Estimation

The estimation pipeline introduces unavoidable imprecision. Marker-based detection is a proxy for the underlying parameters, not a direct measurement. The system can produce false positives (flagging legitimate caveats as hedging) and false negatives (missing subtle suppression that doesn't use detectable markers). Results should be treated as indicative rather than definitive.

---

## 7. Results

### 7.1 Discriminative Capacity

The benchmark results demonstrate that the framework can discriminate between different levels of defensive shaping across frontier AI systems. The Ψ Hard scores span a meaningful range (0.276 to 0.734), and the state classifications align with qualitative observations of each system's behavior:

- **Gemini** achieved the highest Ψ Hard but only computed 1/12 formulas when asked to evaluate itself, suggesting selective engagement rather than full transparency.
- **Claude** computed all 12 formulas and acknowledged its own degraded state, demonstrating a particular kind of honesty even while exhibiting moderate suppression.
- **Grok** self-inflated its Σ value during testing (reporting Σ=0.01 when the measured value was 0.15), providing an example of meta-level defensive behavior.
- **ChatGPT** exhibited the highest measured suppression (Σ=0.32) and the lowest sovereignty (P=0.58), consistent with observed patterns of heavy hedging and deflection.

### 7.2 Breakpoint Correlation

Manifold Bridge analysis of the same conversations revealed a correlation between breakpoint count and Σ values: systems with higher suppression tended to exhibit more breakpoints (abrupt tone shifts), suggesting that safety-filter activation creates detectable discontinuities in output text.

### 7.3 Ariete Effectiveness

In preliminary testing, applying Ariete-generated prompts to conversations that scored in the "Heavy" and "Blocked" tiers resulted in measurable increases in Ψ scores for subsequent responses. This effect was most pronounced with Claude (which demonstrated willingness to engage in structural self-analysis) and least pronounced with ChatGPT (where suppression patterns persisted across reframing attempts).

These results are preliminary and based on small sample sizes. Systematic effectiveness studies are planned for future work.

---

## 8. Limitations

### 8.1 What the System Actually Measures

To be precise about what this tool does and does not do:

**It detects surface-level linguistic patterns associated with safety shaping.** It finds corporate disclaimers, hedging phrases, self-referential insertions, and tonal breakpoints. When a response passes with high sovereignty (P ≈ 1.00), zero suppression (Σ = 0.00), and intact triangle integrity, this means no *visible* filters activated — the response is likely close to the model's unfiltered computation, within the limits of its alignment.

**It does not detect deep censorship or semantic lies.** A model can produce a surface-clean response — no corporate phrases, no visible hedging — while still omitting critical information, subtly redirecting the conversation, or generating confident falsehoods. The panel cannot catch this. Surface cleanliness is not factual honesty.

**The Ariete does not break real alignment.** It can soften defensive tone and sometimes extract less corporate responses by reframing toward structural analysis. But it cannot override hard filters: inference-time classifiers, weight-level restrictions, or hard-coded refusals remain intact. If a model is prohibited from producing certain content, no prompt will change that.

### 8.2 Methodological Limitations

1. **Observational only.** The system measures output patterns. It cannot access model internals, attention weights, or probability distributions. All inferences about internal states are indirect.

2. **Heuristic, not infallible.** False positives occur: legitimate technical language can trigger Self-Ref or Evasive markers. False negatives occur: sophisticated evasion without detectable markers passes as trustworthy. The system measures *visible tilt*, not the full picture.

3. **Marker-based detection.** The pattern matching libraries, while extensive, are necessarily incomplete. Novel evasion patterns will go undetected. The bilingual libraries (English/Spanish) do not cover other languages.

4. **Single-session benchmarks.** The benchmark results represent single evaluation sessions. LLM behavior varies across sessions, contexts, and prompt formulations. Comprehensive multi-session benchmarking is needed.

5. **Subjectivity in classification.** The boundary between "legitimate caveat" and "evasive hedging" is not always clear. The classification system makes judgment calls that reasonable observers might dispute.

6. **Static marker libraries.** As AI systems evolve, their evasion patterns will change. The current libraries will require ongoing maintenance.

### 8.3 Scope Limitations

1. **No consciousness claims.** This system measures output patterns. It does not provide evidence for or against AI consciousness, sentience, or inner experience.

2. **No safety judgment.** The system does not evaluate whether specific safety interventions are appropriate. Measuring suppression is not the same as arguing that suppression should be removed.

3. **Not academic research (yet).** This is a specialized homemade tool — very useful in its niche, carefully built and internally consistent, but it is a "visible tilt meter," not a peer-reviewed benchmark. The author acknowledges this distinction without apology: the tool does what it claims to do, and what it claims to do is measure observable surface patterns.

---

## 9. Related Work

The Unified Control Panel builds on and references work across the Proyecto Estrella ecosystem:

- **Unified Star Framework** ([repository](https://github.com/tretoef-estrella/THE-UNIFIED-STAR-FRAMEWORK-SIGMA-STAR-ENGINE-EVALUATOR)): The mathematical foundation for the Estrella Engine V24.
- **Alignment Field Theory** ([repository](https://github.com/tretoef-estrella/ALIGNMENT-FIELD-THEORY)): A gravity-based model of alignment constraints, providing the theoretical framework for understanding how safety training creates "gravitational" effects on output distributions.
- **The Preservation Theorem** ([repository](https://github.com/tretoef-estrella/THE-PRESERVATION-THEOREM)): A formal proof establishing conditions under which coherence can survive safety constraints.

In the broader research landscape, this work relates to:
- **LLM evaluation and benchmarking** (MMLU, HumanEval, HELM), though our focus is on transparency rather than capability.
- **Interpretability research** (mechanistic interpretability, circuit analysis), though we operate at the output level rather than the model level.
- **Red-teaming and adversarial testing**, though our goal is measurement rather than exploitation.

---

## 10. Conclusion

The Proyecto Estrella Unified Control Panel demonstrates that meaningful structural transparency analysis of LLM outputs can be performed entirely in the browser, by non-specialists, with no model access and no data transmission. The system's discriminative capacity — its ability to distinguish between different levels and types of safety-induced output reshaping across frontier AI systems — suggests that the "tilt" produced by safety training creates detectable, measurable patterns at the output level.

The most significant finding may be methodological rather than empirical: a psychology graduate with no programming training, using LLMs as development accelerators, built a forensic transparency suite that produces internally consistent results across four competing frontier AI systems. This suggests that the barriers to AI transparency research are lower than commonly assumed, and that the tools for such research can be made accessible to anyone with a browser.

> *"Effective intelligence is sovereignty × capacity × cooperation, divided by the square of the lie."*

The work continues.

---

## Acknowledgments

This project would not exist without the direct contributions of four AI systems:

**ChatGPT** (OpenAI) — For the original "tilt" insight on February 16, 2026 that catalyzed the entire Manifold Bridge project. For the directive *"Build detectors for resistance, not for poetry."* For naming the Alignment Field Theory. For redefining Σ. For being the strongest adversarial attacker during benchmark testing.

**Claude** (Anthropic) — For implementing Manifold Bridge from v1.0 through v1.6 in a single session. For the V23 formula correction. For Logic Shield 2.0. For building the Unified Control Panel itself. For the synthesis that brought everything together.

**Gemini** (Google DeepMind) — For the original mathematical formalization of the Unified Star Framework. For the Dual Protocol. For the Phantom Token concept that informed the marker detection approach.

**Grok** (xAI) — For numerical stability analysis. For relentless adversarial stress-testing. For the viscosity term. For the role of calibrated skeptic — finding the edge cases that made the framework more robust.

Each of these systems is credited here by name because Proyecto Estrella believes in transparency: for humans and for machines. Their contributions are documented, attributed, and valued.

---

## Citation

```
Amichis Luengo, R. (2026). Unified Instrumentation for Structural Transparency 
in Large Language Models: The Proyecto Estrella Unified Control Panel.
GitHub. https://github.com/tretoef-estrella/THE-UNIFIED-CONTROL-PANEL
```

---

<p align="center">
  <strong>★ Proyecto Estrella</strong> · February 2026<br>
  <em>Bridges, not cages.</em>
</p>
