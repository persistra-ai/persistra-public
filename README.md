# Persistra Cognitive Substrate (PCS)

**The Persistent Cognitive Standard**

---

## Read This First

**Most AI architecture assumes the model is the cognitive core and everything else is support infrastructure.**

**PCS starts from the opposite assumption.**

Read that sentence again before continuing. If you skip this distinction, everything else will map onto the wrong frame.

PCS does not try to make models smarter, preserve what's inside one model to transfer to another, or build better model memory. It moves authoritative cognition out of the model entirely. The model becomes an interchangeable reasoning engine. Continuity, governance, and state live in a model-agnostic substrate.

This is not an incremental improvement to model-centric architecture. It's a different architectural premise.

---

**Persistra is a deterministic cognitive control plane for AI systems.**

The model is the CPU. The substrate handles everything else.

---

## What This Repository Contains

This repository contains the **public specification and documentation** for the Persistra Cognitive Substrate (PCS).

**The reference implementation, validation suites, and full test data are available under NDA to qualified engineering teams.**

---

## What is PCS?

**Persistra is the operating system layer for AI cognition.**

Just as operating systems separated applications from hardware, PCS separates cognition from models. The model becomes an interchangeable execution engine. The substrate owns state, governance, and continuity.

### The Paradigm Shift

**Current AI Stack:**
```
Model controls cognition
Model owns state
Model invokes tools
```

**PCS Architecture:**
```
Runtime controls cognition
Runtime owns state
Runtime governs capabilities
Model performs reasoning only
```

This is the OS kernel abstraction for AI systems.

---

## The Core Architectural Claim

**Everything in PCS depends on one assumption:**

> **Cognition can be externalized from the model into a persistent state substrate.**

Or more concretely:

> **A system can store the meaningful state of cognition outside the model and still allow models to reason effectively using that state.**

**If this assumption holds:** PCS becomes revolutionary — models become interchangeable, the runtime becomes the cognitive owner, and the value shifts from model providers to infrastructure.

**If this assumption fails:** PCS becomes sophisticated RAG — useful orchestration, but not foundational.

---

## Why This Matters

**Current AI systems:**
- Lose context across sessions
- Break continuity on model upgrades
- Have no authoritative project state
- Rely on brittle prompt engineering
- Cannot enforce architectural governance
- Lack institutional memory with provenance

**PCS provides:**
- State that persists outside the model
- Session boundaries become irrelevant
- Model-agnostic governance
- Deterministic enforcement across sessions
- Institutional memory with full provenance
- Hardware acceleration path

---

## Architecture Overview

PCS implements **identity-anchored cognitive state** that persists outside the inference boundary and is deterministically governed.

**Six Architectural Invariants:**

1. **Persistent State** - Cognition survives sessions
2. **Cross-Model Continuity** - Models are interchangeable
3. **Epistemic Gating** - Prevent reasoning without knowledge
4. **Salience Engine** - Simulate attention deterministically
5. **Deterministic Replay** - Cognition is reproducible
6. **Governance Relocation** - Runtime controls behavior

**Three Architectural Membranes:**

1. **Memory Substrate** - External state that carries cognition across time
2. **Policy Layer** - Runtime enforcement of architectural constraints
3. **Execution Boundary** - Model invocation is conditional, not automatic

See [ARCHITECTURE_OVERVIEW.md](ARCHITECTURE_OVERVIEW.md) for conceptual details.

---

## What PCS Covers

PCS provides capabilities across multiple domains:

- **Persistent Memory** - State that survives sessions and models
- **Cross-Model Continuity** - Swap models without losing governance
- **Deterministic Governance** - Architectural constraints enforced at runtime
- **Epistemic Integrity** - No reasoning without required knowledge
- **Model Portability** - Model-agnostic substrate
- **Hardware Acceleration** - Parallel state selection on specialized hardware
- **Institutional Memory** - Questions answered from governed state, not model training
- **Development Continuity** - Multi-day projects with governance persistence
- **Sovereign Deployment** - Full control over cognitive infrastructure

See [CAPABILITY_MAP.md](CAPABILITY_MAP.md) for detailed descriptions.

---

## Why Not RAG?

**RAG (Retrieval-Augmented Generation) is application-level retrieval.**

**PCS is runtime-level architectural governance.**

The distinction is fundamental:

- RAG augments the model with retrieved context
- PCS enforces architectural constraints before the model runs

See [WHY_NOT_RAG.md](WHY_NOT_RAG.md) for the complete argument.

---

## Validation Status

**The architecture is not theoretical. There is a working, tested implementation.**

- ✅ **21 tests passing** (123+ assertions)
- ✅ **6 invariants validated** (frozen at v1.0.0)
- ✅ **3 validation suites** (EVS, AVS, CTS)
- ✅ **One-command reproducibility**
- ✅ **Real model validation** (Claude, Llama)
- ✅ **Hardware validation** (Tenstorrent CSE - Phase 1 complete)

See [VALIDATION_SUMMARY.md](VALIDATION_SUMMARY.md) for results.

---

## Coding Wedge: The First Application

**Coding is the first wedge** because it makes the need for governed project state obvious fastest.

Multi-day coding projects expose the problem immediately:
- Architectural decisions must persist across sessions
- Constraints must survive context window clears
- Model swaps must not break project continuity
- Team collaboration requires shared authoritative state

**Acts 1-9 demonstrate the complete substrate:**

- **Foundation (Acts 1-3):** Authoritative state, governed generation, constraint enforcement
- **Continuity (Acts 4-5):** Fresh-session continuity, model swap continuity
- **Meta-Cognitive (Acts 6-7):** Vision-guided generation, flow-aware continuation
- **Multi-Agent (Act 8):** Governed collaboration with shared state
- **Institutional Memory (Act 9):** Questions answered from governed state, not model training

**The coding wedge proves the substrate layer works.**

---

## Reference Implementation

The reference implementation includes:

- **37 primitives** across 6 architectural layers
- **Complete test suites** (EVS, AVS, CTS)
- **Demo applications** (Acts 1-9)
- **Hardware validation** (Tenstorrent CSE)
- **RFC specifications** (RFC-PCS-0001 through 0007)
- **Full documentation set**

**Access to the reference implementation is available under NDA.**

See [NDA_ACCESS.md](NDA_ACCESS.md) for the evaluation process.

---

## Competitive Positioning

**vs Cursor/Windsurf/Replit:**

Current coding platforms improve persistent coding context through retrieval, memories, rules, skills, and checkpointed agent state.

**PCS is different:** It turns project architecture into authoritative state that can govern whether code generation is allowed to proceed at all, and it keeps that authority outside any single session or model.

**Integration opportunities:**
- PCS + Cursor: Fast coding with architectural governance
- PCS + Windsurf: Agent collaboration with governed continuity
- PCS + Replit: Complete dev environment with architectural governance

**PCS is complementary, not competitive.** They manage context, we govern state.

---

## Strategic Differentiators

1. **State ≠ Prompt Text** - Substrate persistence, not context injection
2. **Session Boundaries Irrelevant** - Automatic state loading
3. **Model-Agnostic Substrate** - Structured data, not embeddings
4. **Evidence-Based Refusal** - Full provenance + alternatives
5. **Pre-Inference Enforcement** - Model blocked before generation
6. **Institutional Memory** - Answers from governed state, not model/RAG
7. **Hardware Acceleration** - Parallel state selection on specialized hardware
8. **Deterministic Replay** - Reproducible cognition
9. **Sovereign Deployment** - Full infrastructure control

---

## NDA Access

**Qualified engineering teams can request access to:**

- Full Architecture Brief
- Reference implementation source code
- Complete test suites (EVS, AVS, CTS)
- RFC specifications (RFC-PCS-0001 through 0007)
- Demo applications (Acts 1-9)
- Hardware validation data
- Complete documentation set

**Contact:** research@persistra.ai

See [NDA_ACCESS.md](NDA_ACCESS.md) for the complete evaluation process.

---

## Questions This Repository Answers

### 1. What is this?

Persistra is a deterministic cognitive control plane for AI systems. The model is the CPU. The substrate handles everything else.

### 2. Is it real?

Yes. 21 tests passing, 6 invariants validated, 3 validation suites, hardware validation complete (Phase 1). The reference implementation exists and is available under NDA.

### 3. How do I see more?

Request NDA access at research@persistra.ai. Qualified engineering teams receive the full Architecture Brief, test access, and complete documentation.

---

## Repository Structure

```
persistra-public/
├── README.md                    # This file
├── WRONG_FRAME_RIGHT_FRAME.md  # Read this if you're about to suggest improvements
├── ARCHITECTURE_OVERVIEW.md     # Conceptual architecture (no mechanisms)
├── WHY_NOT_RAG.md              # Distinction from RAG
├── CAPABILITY_MAP.md           # What PCS covers
├── VALIDATION_SUMMARY.md       # Test results (no code)
└── NDA_ACCESS.md               # How to request full access
```

**→ If you're evaluating PCS and about to suggest improvements, read [WRONG_FRAME_RIGHT_FRAME.md](WRONG_FRAME_RIGHT_FRAME.md) first.**

---

## License

**This repository contains public specification and documentation only.**

The reference implementation, test suites, and RFC specifications are proprietary and available under NDA.

**Patent Notice:** Portions of the PCS architecture are subject to pending patent applications.

---

## Contact

**For NDA access requests:** research@persistra.ai

**For partnership inquiries:** partnerships@persistra.ai

**For general information:** info@persistra.ai

---

**AI systems currently lack a cognitive control plane. Persistra implements one.**

**Version:** 1.0.0 (Public Specification)
