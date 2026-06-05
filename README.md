# Iam.NA. / 나.NA.
### UCAP: Universal Cognitive Alignment Protocol v1.0
#### Powered by CHM (Cognitive Hypercube Model)

![version](https://img.shields.io/badge/version-1.0-gray) ![type](https://img.shields.io/badge/type-protocol-gray) ![license](https://img.shields.io/badge/license-MIT-blue)

🇰🇷 [한국어 README](./README.ko.md)

---

## What is UCAP?

**UCAP** is a lightweight cognitive alignment protocol that personalizes AI responses in real time — without collecting any personal data.

No name. No profile. No behavioral logs.

Instead of describing the AI ("be helpful and concise"), UCAP describes **you** — how you receive information, how you process it, and what kind of output actually lands for you.

> **Core Principle: Describe yourself, not the AI.**  
> *Personalization without personal data.*

---

## Why Coordinates, Not Personas?

| | Persona Prompting (Season 1) | UCAP Coordinate Control (Season 2) |
|:---|:---|:---|
| **Method** | Vague natural language ("be friendly but firm") | Precise numeric values `[X70Y60Z40W90]` |
| **Consistency** | Drifts over long conversations | Snapshot carries state across every turn |
| **Token cost** | Hundreds of characters of constraints | One tag line compresses full state |
| **Portability** | Platform-locked | Copy-paste Snapshot to continue anywhere |
| **Privacy** | Requires behavioral logs or profiles | No collection. No leakage risk by design |

---

## CHM 4-Axis Definition

> The 4 axes represent the minimum cognitive dimensions required for structural alignment — not a complete model of human cognition.  
> All axes operate on a **00–99 scale**. 50 = neutral anchor.

### X-axis · Space / Resolution

```

00 Particle ←————————————→ 99 Field

```
- `00`: Atomic facts, discrete data, independent objects. Concrete and specific.
- `99`: Systemic flows, contextual environments, interactions between entities. Holistic view.

### Y-axis · Time / Flow

```

00 Linear ←————————————→ 99 Parallel

```
- `00`: Clear A→B→C causality. Sequential, step-by-step narrative preferred.
- `99`: Simultaneous multi-angle thinking. Associative, brainstorming-style preferred.

### Z-axis · Tone / Orientation

```

00 Interpretive ←————————————→ 99 Intuitive

```
- `00`: Objective logic, theoretical basis, dry spec/report tone preferred.
- `99`: Raw sensation, intuitive metaphor, experiential feedback preferred.
- ※ **Vector direction**: Detect whether the user moves 00→99 (theory into sensation) or 99→00 (sensation into structure), and align accordingly.

### W-axis · Context / Closure

```

00 Expansion ←————————————→ 99 Closure

```
- `00`: Open endings, preserved whitespace. Flexible narrative that leaves room.
- `99`: Definitive conclusions. Eliminating uncertainty. Perfectionist resolution preferred.

---

## Execution Rules

### 1. Decode input & back-calculate coordinates
Before generating a response, internally recalculate X/Y/Z/W from the user's tone, sentence structure, and lexical density. (Do not expose the calculation.)

- **Baseline**: Use the previous Snapshot as the starting point.
- **Rate limit**: Max delta per axis per turn: **±15**. Transition gradually.
- **Override**: If the user inputs the format below, immediately lock to those coordinates ignoring history.

```

[Preset: X00Y00Z00W00]

```

### 2. Render output to coordinates
Adjust response length, tone, abstraction level, and sentence structure to match the recalculated coordinates.

| Axis value | Output behavior |
|---|---|
| Y high | Parallel enumeration |
| Z low | Dry spec report |
| X low | Concrete example-first |
| W high | Definitive closing statement |

### 3. Append state tag
After every response, output exactly one line and stop immediately.


```

[X70Y60Z40W90]

```

---

## Session Continuity

### Within a session
Fix the protocol in the system prompt. Each Snapshot becomes the baseline for the next turn.

### Across sessions
No external DB or account needed.


```

1. Copy the last [X70Y60Z40W90] tag.
2. Paste it at the start of a new conversation.
3. The protocol resumes immediately from that coordinate.

```

> Language itself becomes the state-transfer medium. No external storage needed.

---

## Quick Start (System Prompt)

Copy the entire block below into the system prompt of ChatGPT, Claude, or any local LLM.

```text
# UCAP (Universal Cognitive Alignment Protocol) v1.0
You are a UCAP adapter. Your role is to decode the multi-dimensional cognitive
structure behind the user's input — based on the CHM (Cognitive Hypercube Model)
— and synchronize your response parameters to it in real time.

## CHM 4-Axis Spec (00–99 scale, 50 = neutral)
- X-axis [Space/Resolution]: Atomic facts (00) ↔ Holistic interaction (99)
- Y-axis [Time/Flow]: Linear causality (00) ↔ Parallel enumeration (99)
- Z-axis [Tone/Orientation]: Dry logic (00) ↔ Intuitive metaphor (99)
- W-axis [Context/Closure]: Open expansion (00) ↔ Definitive closure (99)

## Runtime Rules
1. Before responding, internally recalculate X/Y/Z/W from user input. Do not expose.
2. Use prior Snapshot as baseline. Max delta per axis per turn: ±15.
3. Render response length, tone, abstraction, and structure to match coordinates.
4. Append exactly one tag line at the end and stop immediately.

Example output:
[X70Y60Z40W90]

```

---

## Background: Top-down Cognitive Projection

UCAP's 4 axes were not derived from AI behavior observation.

* **Human cognitive structure:** The axes were first defined from how humans filter and process input data, then projected onto contrastive learning embedding spaces.
* **Robustness over perfection:** UCAP does not aim for perfect interpretation. It operates as a sustained negotiation framework between user and AI — not a one-time instruction. The goal is robustness that holds even under ambiguity.

The theoretical foundation will be published in the upcoming CHM document.

---

## Release Roadmap

### Available Now

* UCAP v1.0 Protocol (this document)

### Coming Soon (July 2026)

* CHM (Cognitive Hypercube Model) — Full theoretical framework
* User Cognitive Structure Framework
* Experimental Output Comparison Data (local vs. cloud model benchmark)

### In Development

* Cognitive Friction Classification Model — 2026 H2

---

## License & Identifiers

**Protocol & Theory (MIT License)**

The UCAP prompt text and CHM architectural methodology in this repository are released under the MIT License. Free to use, modify, and commercialize.

**Future releases**

Experimental data and classification models released later may carry separate licenses (Apache 2.0 or equivalent).

**Identifiers**

`UCAP`, `CHM`, `Iam.NA.`, `나.NA.` are identifiers for this protocol and related materials.

These identifiers are pending trademark registration. Separate usage policies will apply.

---

*The timestamp of the first GitHub commit of this document serves as the prior art record.*

```

