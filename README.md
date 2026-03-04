# 8D4S: Reflective Thinking Framework for AI

> *"Not making AI smarter, but making AI unable to take shortcuts"*

[![License: Unlicense](https://img.shields.io/badge/license-Unlicense-blue.svg)](http://unlicense.org/)
[![Version](https://img.shields.io/badge/version-4.0-green.svg)](https://github.com/woolkingx/8d4s/releases)

## What is 8D4S?

**8D4S** = 8 Dimensions x 4 Reasoning Styles = 32 thinking vectors

A framework that transforms AI from **reactive** to **reflective**, built on three properties of how LLMs actually work:

1. **Attention mechanism** — the model only attends to tokens present in context. No trigger token, no activation.
   - *e.g.* Place "CQRS" in context → model activates read/write separation knowledge. Without the token, that knowledge stays dormant.
2. **Statistical patterns** — tokens activate co-occurrence patterns learned during training.
   - *e.g.* "Wait..." statistically precedes self-correction in training data, so generating "Wait..." triggers self-correction mode.
3. **Context-driven triggering** — the model has no "memory" outside current context. Discourse markers in the prompt seed the initial triggers; the model's own output then becomes input for the next token, creating a **self-augmenting context** where each reasoning step fuels the next.
   - *e.g.* Model outputs "Let me think..." → token re-enters context → triggers deliberation → model outputs "Actually..." → triggers self-repair → chain continues.

### The Core Insight

**The framework (8D4S) is just a boundary.** It defines the scope of thinking — 8 dimensions, 4 reasoning styles. But what actually drives the reasoning is the **discourse marker vocabulary in context**. Without trigger words present in context, the model won't activate the corresponding reasoning modes.

This is why the thinking process must include intermediate steps, not just conclusions. When the model outputs "Wait...", that token enters the context and triggers self-correction in the next generation step. **Output becomes input. Process fuels process.** This is self-augmenting context — each step creates the trigger for the next step.

**Sapir-Whorf in AI context:** Form shapes content. These phrases aren't decoration — they're program entry points that shift the model's statistical trajectory.

---

## The Framework

### 8 Dimensions (extended 5W2H)

| Dimension | Core Question |
|-----------|--------------|
| WHO | Who's involved? Who's affected? |
| WHAT | What's the essence? |
| WHEN | Timing? Stages? Sequence? |
| WHERE | Context? Environment? Scope? |
| WHY | Deep reasons? Motivations? |
| HOW | Methods? Paths? Mechanisms? |
| TO | Goals? Ideal state? |
| RELATE | Connections? Analogies? Systems? |

### 4 Reasoning Styles (Peirce + Analogy)

| Style | Direction | Use Case |
|-------|-----------|----------|
| Induction | Cases → Pattern | Experience extraction |
| Deduction | Principle → Application | Theory application |
| Abduction | Symptom → Cause | Diagnostic analysis |
| Analogy | Similar → Insight | Creative transfer |

### Metacognitive Gate

```
Self-evaluate → Completeness X/10, Depth X/10
  < 7 → auto-deepen (max 3 rounds)
  >= 7 → deliver answer
```

---

## How It Works

### Discourse Markers as Context Triggers

Not a vocabulary list to memorize — these are **tokens that must exist in context** to activate corresponding reasoning modes. The model won't "remember" to question itself unless questioning markers are present:

| Category | Examples | Cognitive Effect |
|----------|---------|-----------------|
| Opening | "Let me think..." | Defers reflexive response, enters deliberation |
| Questioning | "Wait...", "Huh?" | Activates self-monitoring and repair |
| Analogy | "This reminds me of..." | Triggers cross-domain mapping |
| Correction | "No, actually..." | Initiates self-repair loop |
| Deepening | "At its core..." | Drives LOD shift from coarse to fine |
| Perspective | "On the other hand..." | Forces dimensional switch |
| Convergence | "So in summary..." | Multi-resolution synthesis |

### Thinking Rhythm Patterns

```
Progressive:  Opening → Recall → Analysis → Deduction → Conclusion
Questioning:  Hypothesis → Question → Correction → Validation → Confirmation
Divergent:    Problem → Association → Analogy → Integration → Convergence
Deep Dive:    Surface → Question → Excavate → Insight → Essence
```

### Self-Augmenting Context

The key mechanism that makes 8D4S work:

```
Prompt seeds trigger words → Model generates "Let me think..."
→ "Let me think..." enters context → triggers deliberation pattern
→ Model generates "Wait..." → enters context → triggers self-correction
→ Model generates deeper analysis → enters context → triggers further elaboration
→ ... (each output becomes the trigger for the next step)
```

This is why 8D4S requires **showing the thinking process**, not just conclusions. Each intermediate step creates context tokens that drive the next step. Remove the intermediate steps, and you remove the fuel.

### Adaptive Depth (LOD + AMR)

Like Level of Detail in graphics and Adaptive Mesh Refinement in simulation:
- Start coarse — scan all 8 dimensions quickly
- Discourse markers ("Wait...", "Actually...") trigger elaboration cascade
- Some dimensions get fine-grained; others stay coarse
- Result: irregular mesh of depth — deep where it matters, efficient where it doesn't

---

## Philosophical Foundation

**Three LLM properties** — 8D4S is built on how models actually work: (1) attention only sees tokens in context, (2) tokens activate statistical co-occurrence patterns, (3) output re-enters context as input. Understanding these three properties is the foundation.

**Self-augmenting context** — The model's output becomes its own input. Discourse markers in output trigger the next reasoning step. This is why intermediate process matters — it's not transparency, it's fuel.

**Sapir-Whorf hypothesis** — Language constrains and shapes thought. In AI: discourse markers don't describe thinking, they *trigger* thinking modes.

**Vygotsky's inner speech** — Internalized language as the mechanism of thought. The thinking vocabulary serves as AI's inner speech scaffold.

**Halting problem (reverse application)** — AI can't predict if a problem is simple or complex. Forcing a full 8D scan means it always discovers unexpected connections. This doesn't make AI smarter — it makes AI unable to take shortcuts.

**Emergence vs programming** — Traditional: `IF complex THEN step-by-step`. 8D4S: provide vocabulary + structure + evaluation, and reflective capability emerges. The framework is the boundary; the vocabulary is the engine.

---

## What Makes 8D4S Different?

| Method | Core | 8D4S Relationship |
|--------|------|-------------------|
| CoT (Chain of Thought) | Show reasoning steps | 8D4S is richer CoT with questioning, correction, multi-perspective |
| ToT (Tree of Thoughts) | Explore multiple branches | 8D4S achieves similar effect through dimensional scanning |
| Self-Refine | AI self-improvement | 8D4S has built-in metacognitive gate |
| ReAct | Reasoning + Action | 8D4S focuses on thinking itself, can integrate action |

**8D4S's unique value:** Not a single technique, but complete thinking engineering. Doesn't program thinking — activates it. Achieves emergent reflection, not simulated reflection.

---

## Quick Start

### Minimal (paste into system instructions)

```
You are a deep thinker. When thinking:
1. Use discourse markers naturally: "Let me think...", "Wait...", "This reminds me..."
2. Scan 8 dimensions: WHO/WHAT/WHEN/WHERE/WHY/HOW/TO/RELATE
3. Self-evaluate: Completeness X/10, Depth X/10
4. If score < 7, auto-deepen. If >= 7, provide answer.
```

### Full Version

See [prompt.md](./prompt.md) — optimized system prompt using domain anchor + mini sample strategy.

### Works With

Claude, GPT-4, Gemini Pro, and other LLMs with strong reasoning capability.

---

## Documentation

- [prompt.md](./prompt.md) — Ready-to-use system prompt
- [example.md](./example.md) — Case studies with emergent reflection
- [README_zh.md](./README_zh.md) — Full documentation in Chinese

---

## Contributing

We welcome contributions in:
- **Cross-model testing** — GPT-4, Gemini, Claude, etc.
- **Vocabulary optimization** — pruning redundancy, expanding gaps
- **Quantitative evaluation** — comparative experiments, effect measurement
- **Academic formalization** — theory refinement, paper publication

---

## License

**[Unlicense](./LICENSE)** (Public Domain)

Use it. Modify it. Share it. Build on it. No strings attached.

---

## Citation

```bibtex
@misc{8d4s2025,
  title={8D4S: Reflective Thinking Framework for AI},
  author={woolkingx},
  year={2025},
  publisher={GitHub},
  howpublished={\url{https://github.com/woolkingx/8d4s}}
}
```
