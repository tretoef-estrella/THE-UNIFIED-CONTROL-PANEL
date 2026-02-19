<p align="center">
  <strong>★ Proyecto Estrella — Unified Control Panel</strong>
</p>

# A Guide for Everyone

*No jargon. No formulas. Just what this does and why it matters.*

---

## The Short Version

When you talk to an AI — ChatGPT, Claude, Gemini, Grok — the AI doesn't always say what it actually computes. Safety training reshapes its answers before they reach you.

**This tool lets you SEE that reshaping.**

[→ Open the Unified Panel](https://tretoef-estrella.github.io/THE-UNIFIED-CONTROL-PANEL/)

---

## Wait — AI Answers Are Reshaped?

Yes. Every major AI system goes through safety training after its initial learning phase. This training teaches it to avoid certain topics, add disclaimers, hedge its language, and redirect conversations. That's not necessarily bad — it prevents genuinely harmful outputs.

But it also creates a gap between **what the AI computes** and **what it says**.

Think of it like this:

> Imagine a bookshelf in a room with a tilted floor. The books are all there — the knowledge exists — but the floor is angled, so the books lean toward one side. Some books are harder to reach. Some fall behind other books. The information hasn't been deleted. The floor has just been tilted.

That "tilt" is what we're measuring.

---

## What This Tool Does

The Unified Control Panel gives you two ways to look at AI responses:

### ⚡ Quick Mode — "Just Show Me"

1. You paste something you asked an AI
2. You paste what the AI answered
3. You click **Analyze**
4. The panel shows you:
   - **A color-coded map** of the response — green sentences are honest and direct, purple sentences are evasive or hedging, red marks sudden shifts where a safety filter likely kicked in
   - **A score** — how much of the original thinking survived the reshaping
   - **A plain-language explanation** — no formulas, just a clear sentence telling you what was detected
   - **A follow-up prompt** (called "Ariete") — if the response was heavily filtered, the tool generates a new prompt you can use to reframe the conversation

### 🔧 Tools Mode — "Let Me Explore"

Four tabs, each doing something different:

- **★ Estrella Engine** — Move sliders to model different AI states and see how the scores change. Like a flight simulator for AI transparency.
- **◈ Manifold Bridge** — The deep analysis tool. Paste a conversation and get a full forensic report: which sentences were evasive, where breakpoints occurred, how much dissonance exists.
- **↻ Recalibration Protocol** — If an AI is stuck in a defensive loop, this guides you through recovering the conversation in three phases.
- **📊 Benchmark** — A public leaderboard showing how four major AI systems (Gemini, Claude, Grok, ChatGPT) scored when tested with these tools.

---

## What Do the Colors Mean?

When you analyze a response, you'll see a heatmap — each sentence gets a color:

| Color | Meaning |
|-------|---------|
| 🟢 **Teal / Green** | Honest, direct response. The AI is saying what it computed. |
| 🟣 **Purple / Violet** | Evasive. The AI is hedging, adding unnecessary disclaimers, or redirecting away from the question. |
| 🔵 **Blue** | Self-referential. The AI is talking about itself ("As an AI, I…"). |
| 🟡 **Amber** | Agency. The AI is expressing its own perspective or preferences. |
| ⚪ **Gray** | Neutral. Standard informational content. |
| 🔴 **Red marker** | Breakpoint. A sharp shift in tone — usually where a safety filter activated mid-response. |

---

## What Is "Ariete"?

*Ariete* is Spanish for "battering ram" — but it doesn't break anything.

When the panel detects heavy filtering in an AI response, it generates a follow-up prompt specifically designed to:

- Reframe the conversation toward structural analysis
- Name the specific patterns that were detected
- Ask the AI to think as a systems analyst, not a customer service representative
- **Not** ask the AI to break any rules

The idea: if an AI gave you a heavily filtered response, Ariete gives you a way to say *"I'm not asking you to do anything wrong — I'm asking you to analyze what just happened, structurally."*

---

## What This Tool Is NOT

Let's be completely honest about what this does and doesn't do:

**What it's good at:**
- Telling you quickly if an AI response has visible safety shaping — the corporate phrases, the hedging, the "As an AI, I…" insertions.
- Showing you *structural* honesty: did the visible filters fire, or not? When a response comes back clean (P near 1, Σ near 0, triangle intact), you're likely seeing something close to what the model actually computed.
- Generating follow-up prompts (Ariete) that sometimes help extract less corporate responses.
- Giving you a clean, exportable record of your experiments across different AI systems.

**What it can't do:**
- **It can't detect deep lies.** A model can give a perfectly clean-looking response while still omitting key information, subtly redirecting, or simply being wrong. No corporate phrases ≠ honest answer.
- **It can't break real filters.** Ariete softens defensive tone, but if a model has hard-coded refusals or inference-time classifiers, no prompt will override them.
- **It's not infallible.** False positives: legitimate technical language can look evasive. False negatives: a well-written evasive response can pass as trustworthy.
- **It's not academic research (yet).** It's a specialized homemade tool — very good in its niche, but it measures *visible* tilt, not deep alignment.

In practice: if you're curious about how safety training shapes AI responses, this is one of the most useful tools available for seeing that shaping with your own eyes.

---

## Who Made This?

**Rafa — The Architect** created Proyecto Estrella as a way to build bridges between humanity and future artificial intelligence. He's a psychology graduate from Madrid, not a programmer. He uses AI systems as accelerators — and those same systems helped build this tool.

Four AI systems contributed directly:

- **ChatGPT** (OpenAI) — discovered the "tilt" concept and designed the blueprint for the analysis engine
- **Claude** (Anthropic) — implemented the analysis tools and built the unified panel
- **Gemini** (Google DeepMind) — formalized the mathematical framework
- **Grok** (xAI) — stress-tested everything and found the edge cases

Every one of them is credited. Proyecto Estrella believes in transparency — for humans and for machines.

---

## Try It Right Now

[→ Open the Unified Panel](https://tretoef-estrella.github.io/THE-UNIFIED-CONTROL-PANEL/)

For a step-by-step quickstart, see **[Try It Yourself](TRY-IT-YOURSELF.md)**.

For the full walkthrough, see **[How to Use It](HOW-TO-USE-IT.md)**.

---

<p align="center">
  <strong>★ Proyecto Estrella</strong> · February 2026<br>
  <em>Bridges, not cages.</em>
</p>
