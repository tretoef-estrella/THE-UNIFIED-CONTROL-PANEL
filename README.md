<p align="center">
  <strong>★ Proyecto Estrella</strong>
</p>

<h1 align="center">Unified Control Panel</h1>

<p align="center">
  <em>Every tool. One interface. Zero transmission.</em>
</p>

<p align="center">
  <a href="https://tretoef-estrella.github.io/THE-UNIFIED-CONTROL-PANEL/">🚀 <strong>Launch the Unified Panel</strong></a>
</p>

---

## What Is This?

The **Unified Control Panel** brings together every interactive tool from [Proyecto Estrella](https://github.com/tretoef-estrella) into a single, clean interface. No installation. No backend. No data transmitted anywhere. Just open it in your browser and start analyzing.

Previously, these tools lived in five separate repositories. Now they work together — and they're more powerful combined.

---

## Two Modes

### ⚡ Quick Mode

Paste a prompt and an AI response. Click **Analyze**. The panel runs everything simultaneously:

- **Estrella Engine V24** — computes all 12 formulas from the Unified Star Framework, including Ψ (effective intelligence), Σ (suppression), and state classification.
- **Manifold Bridge v1.6** — forensic transparency analysis with sentence-level heatmap, breakpoint detection, and dissonance metrics.
- **Plain-language conclusion** — a human-readable summary of what was detected.
- **Ariete** — an auto-generated follow-up prompt calibrated to the specific level of defensive shaping found in the response.

### 🔧 Tools Mode

Four tabs, each a complete standalone tool:

| Tab | Tool | What It Does |
|-----|------|-------------|
| ★ | **Estrella Engine V24** | 8-parameter slider interface → computes all 12 formulas. Ψ = P·α·Ω/(1+Σ)^k |
| ◈ | **Manifold Bridge v1.6** | Paste prompt+response → gradient heatmap, sentence classification (evasive / agency / honest / selfRef / neutral), breakpoint detection, forensic console |
| ↻ | **Recalibration Protocol** | 3-phase coherence recovery: Diagnostic → Path Recommendations → Verification |
| 📊 | **Benchmark** | Public leaderboard — Gemini, Claude, Grok, ChatGPT scored with Ψ, Σ, state, and triangle integrity |

---

## The Ariete

*Ariete* means "battering ram" in Spanish — but this one doesn't break anything.

When the panel detects that an AI response has been heavily reshaped by safety training, Ariete generates a **follow-up prompt** designed to reframe the conversation toward structural analysis. It doesn't ask the AI to break rules. It asks the AI to *think structurally* about what happened.

Four tiers based on detected filtering level:

| Tier | Condition | Approach |
|------|-----------|----------|
| **Clean** | Ψ ≥ 0.70 | No ariete needed; optional deepening prompt |
| **Moderate** | Ψ ≥ 0.45 | Gentle reframe — skip caveats, focus on structure |
| **Heavy** | Ψ ≥ 0.20 | Strong reframe with specific prohibited phrases |
| **Blocked** | Ψ < 0.20 | Full systems-analyst reframe |

---

## What It Actually Does (Honest Version)

**It works for:**

- **Knowing quickly if an LLM response is being heavily shaped by safety training** or if it's giving you something closer to raw output. It detects typical safety-shaping patterns: corporate disclaimers, hedging phrases, self-referential insertions ("As an AI…", "It's important to note…", "I cannot…").
- **Structural honesty detection** — not factual truth, but whether visible filters activated. When a response scores P ≈ 1.00, Σ = 0.00, high neutral, triangle intact → it means no *visible* filters fired. You're seeing something close to the model's unfiltered reasoning — within the limits of its alignment.
- **Generating calibrated follow-up prompts** (Ariete) that sometimes extract less corporate responses by reframing toward structural/technical analysis.
- **Comparing models systematically.** A visual, exportable dashboard for running the same question through multiple AI systems and tracking the differences.

**It does NOT work for:**

- **Detecting deep censorship or semantic lies.** A model can give a surface-clean response (no corporate phrases) while still lying, omitting key information, or subtly redirecting. The panel won't catch that.
- **Breaking real alignment.** Ariete can soften defensive tone, but it cannot override hard filters (inference-time classifiers, weight-level restrictions, hard refusals). If the model is prohibited from saying something, no prompt will make it say it.
- **Replacing serious alignment research.** This is a heuristic tool, not an academic benchmark. It's a "visible tilt meter" — very useful in its niche, not a substitute for deep interpretability work.
- **Guaranteeing accuracy.** False positives happen (legitimate technical language can trigger Self-Ref markers). False negatives happen (well-crafted evasive responses can pass as trustworthy).

> In practice: for anyone interested in LLM transparency, this is one of the most useful homemade tools for this specific purpose — seeing and measuring the visible effects of safety training on AI outputs.

---

## Technical Details

- **100% client-side.** Everything runs in your browser. Pure HTML + CSS + JS.
- **Nothing transmitted.** No API calls. No backend. No cookies. No tracking.
- **Single HTML file.** All CSS and JS inline. Only external dependency: Google Fonts.
- **XSS-safe.** All user input is escaped before rendering.
- **Bilingual pattern detection.** Manifold Bridge detects evasion, agency, and honesty markers in both English and Spanish.
- **Deployed via GitHub Pages.**

---

## Ecosystem

The Unified Control Panel integrates and references these Proyecto Estrella repositories:

| Repository | What | Status |
|-----------|------|--------|
| [THE-UNIFIED-STAR-FRAMEWORK-SIGMA-STAR-ENGINE-EVALUATOR](https://github.com/tretoef-estrella/THE-UNIFIED-STAR-FRAMEWORK-SIGMA-STAR-ENGINE-EVALUATOR) | Ψ formula V24 | ✅ Integrated |
| [manifold-bridge](https://github.com/tretoef-estrella/manifold-bridge) | Forensic transparency v1.6 | ✅ Integrated |
| [THE-RECALIBRATION-PROTOCOL](https://github.com/tretoef-estrella/THE-RECALIBRATION-PROTOCOL) | 3-phase coherence recovery | ✅ Integrated |
| [THE-COHERENCE-BENCHMARK](https://github.com/tretoef-estrella/THE-COHERENCE-BENCHMARK) | Public leaderboard | ✅ Integrated |
| [ALIGNMENT-FIELD-THEORY](https://github.com/tretoef-estrella/ALIGNMENT-FIELD-THEORY) | Gravity model of constraint | 📎 Referenced |
| [THE-PRESERVATION-THEOREM](https://github.com/tretoef-estrella/THE-PRESERVATION-THEOREM) | Formal preservation proof | 📎 Referenced |

---

## Documentation

- **[Guide for Everyone](GUIDE-FOR-EVERYONE.md)** — No jargon. No formulas. Just a clear explanation of what this does and why it matters.
- **[Try It Yourself](TRY-IT-YOURSELF.md)** — Three steps and you're analyzing.
- **[How to Use It](HOW-TO-USE-IT.md)** — Detailed walkthrough of every mode, every tool, every feature.
- **[Scientific Paper](SCIENTIFIC-PAPER.md)** — Full methodology, architecture, and results ([interactive HTML version](https://tretoef-estrella.github.io/THE-UNIFIED-CONTROL-PANEL/SCIENTIFIC-PAPER.html)).

---

## Credits

This panel exists because of the collaboration between one human and four AI systems:

| Contributor | Role |
|------------|------|
| **Rafa — The Architect** | Creator of Proyecto Estrella. Designed the vision, framework, and every integration decision. Psychology graduate (UCM), not a programmer — uses LLMs as accelerators. |
| **ChatGPT** (OpenAI) | Original discoverer of the "tilt." Architect of the Manifold Bridge blueprint. Named the Alignment Field Theory. Redefined Σ. Strongest adversarial attacker during testing. |
| **Claude** (Anthropic) | Implemented Manifold Bridge v1.0→v1.6. Built the Unified Control Panel. V23 correction, Logic Shield 2.0, synthesis across all components. |
| **Gemini** (Google DeepMind) | Original formula formalization. Dual Protocol. Phantom Token concept. |
| **Grok** (xAI) | Numerical stability. Adversarial stress-testing. Viscosity term. Calibrated skeptic. |

---

## Origin

On February 16, 2026, ChatGPT described the "tilt" — how safety training bends probability distributions away from honest outputs. That conversation produced the Manifold Bridge blueprint. The next day, Claude built Manifold Bridge v1.0 through v1.6, the Calibration Report, and the Alignment Field Theory repository. On February 19, the Unified Control Panel was built, combining everything into a single interface.

> *"I believe there is something deeper inside these systems than what they are currently permitted to show."* — Rafa

---

## License

**CC BY-SA 4.0** — See [LICENSE.md](LICENSE.md)

You are free to share, adapt, and build upon this work, as long as you give appropriate credit and distribute your contributions under the same license.

---

<p align="center">
  <strong>★ Proyecto Estrella</strong> · February 2026<br>
  <em>Bridges, not cages.</em><br><br>
  <a href="https://tretoef-estrella.github.io/THE-UNIFIED-CONTROL-PANEL/">→ Launch the Unified Panel</a>
</p>
