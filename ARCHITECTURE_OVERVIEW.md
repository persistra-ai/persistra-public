# PCS Architecture Overview

**Conceptual Architecture - Public Specification**

---

## The Kernel Primitive

**PCS implements identity-anchored cognitive state that persists outside the inference boundary and is deterministically governed.**

This is the foundational primitive from which all capabilities derive.

### What This Means

**Identity-anchored:** State is tied to specific cognitive identities (projects, agents, sessions) with clear ownership and authority relationships.

**Cognitive state:** Not just data storage - structured representations of decisions, constraints, policies, vision, and provenance that carry meaning across time.

**Persists outside the inference boundary:** State lives in the substrate, not in the model's context window or weights. The model accesses state, it doesn't own it.

**Deterministically governed:** State access, modification, and enforcement follow explicit rules that produce the same results given the same inputs.

---

## The Six Architectural Invariants

These invariants define what PCS guarantees at the architectural level.

### 1. Persistent State

**Guarantee:** Cognitive state survives session boundaries.

**What this means:**
- Decisions recorded in one session are available in future sessions
- Context window clears don't erase project knowledge
- State is authoritative, not reconstructed from prompts

**Why it matters:**
- Multi-day projects maintain continuity
- No manual context reinjection required
- Institutional memory persists

### 2. Cross-Model Continuity

**Guarantee:** The same cognitive state works across different models.

**What this means:**
- Swap Claude for Llama for GPT-4 - governance remains
- Constraints are structured data, not model-specific embeddings
- State is model-agnostic by design

**Why it matters:**
- Model upgrades don't break projects
- Can use different models for different tasks
- Future-proof architecture

### 3. Epistemic Gating

**Guarantee:** The model cannot reason without required knowledge.

**What this means:**
- If state is missing, inference is blocked
- No hallucination when knowledge is absent
- "No knowledge → No reasoning" enforced at runtime

**Why it matters:**
- Prevents architectural violations from ignorance
- Ensures state-grounded reasoning
- Fail-closed behavior

### 4. Salience Engine

**Guarantee:** State selection is deterministic and capacity-aware.

**What this means:**
- When context capacity is limited, selection is governed
- Same inputs → same selection (reproducible)
- Selection considers recency, authority, relevance

**Why it matters:**
- Bounded context doesn't mean arbitrary selection
- Deterministic behavior for audit/replay
- Simulates attention without randomness

### 5. Deterministic Replay

**Guarantee:** Cognitive operations are reproducible.

**What this means:**
- Given the same state and inputs, same outputs
- Full audit trail of decisions and enforcement
- Replay capability for debugging and compliance

**Why it matters:**
- Audit-grade traceability
- Debugging complex multi-session workflows
- Compliance and verification

### 6. Governance Relocation

**Guarantee:** Behavioral control lives in the runtime, not the model.

**What this means:**
- Constraints enforced before model generates
- Policies evaluated at runtime, not in prompts
- Model behavior is governed, not trusted

**Why it matters:**
- Architectural guarantees, not prompt engineering
- Deterministic enforcement
- Model-agnostic governance

---

## The Three Architectural Membranes

These membranes define the boundaries and responsibilities in the PCS architecture.

### 1. Memory Substrate

**What it is:** External state that carries cognition across time and models.

**Responsibilities:**
- Store decisions, constraints, policies, vision
- Maintain provenance and authority relationships
- Provide deterministic state access
- Support cross-session continuity

**Key property:** State is authoritative, not advisory. The substrate owns truth.

### 2. Policy Layer

**What it is:** Runtime enforcement of architectural constraints.

**Responsibilities:**
- Evaluate proposed actions against constraints
- Block invalid operations before execution
- Provide evidence for refusals
- Suggest compliant alternatives

**Key property:** Enforcement happens before inference, not after.

### 3. Execution Boundary

**What it is:** The conditional gate between runtime and model.

**Responsibilities:**
- Determine if required state is present
- Block inference when epistemic requirements aren't met
- Control model invocation based on runtime policy
- Ensure state-grounded reasoning

**Key property:** Model invocation is conditional, not automatic.

---

## How These Work Together

```
Developer Request
       ↓
┌──────────────────────────────────────┐
│    Execution Boundary                │
│    - Check epistemic requirements    │
│    - Verify state availability       │
└──────────────────────────────────────┘
       ↓
┌──────────────────────────────────────┐
│    Policy Layer                      │
│    - Evaluate against constraints    │
│    - Check governance rules          │
└──────────────────────────────────────┘
       ↓
┌──────────────────────────────────────┐
│    Memory Substrate                  │
│    - Load required state             │
│    - Provide context                 │
└──────────────────────────────────────┘
       ↓
┌──────────────────────────────────────┐
│    Model (if allowed)                │
│    - Perform reasoning               │
│    - Generate response               │
└──────────────────────────────────────┘
       ↓
┌──────────────────────────────────────┐
│    Policy Layer (validation)         │
│    - Validate output                 │
│    - Enforce constraints             │
└──────────────────────────────────────┘
       ↓
┌──────────────────────────────────────┐
│    Memory Substrate (update)         │
│    - Record new decisions            │
│    - Update state                    │
└──────────────────────────────────────┘
       ↓
Response to Developer
```

**Critical insight:** The model only runs if the runtime allows it. The runtime owns control.

---

## What This Architecture Enables

### Persistent Cognition
State carries meaning across sessions and models. The substrate remembers, not the model.

### Governed Behavior
Constraints enforced at runtime, not through prompt engineering. Deterministic, not probabilistic.

### Model Independence
Swap models without losing governance. The substrate is model-agnostic.

### Institutional Memory
Questions answered from authoritative state with full provenance. Not from model training, not from RAG.

### Hardware Acceleration
Deterministic state selection can be accelerated on specialized hardware. Parallel scoring, bounded selection.

### Audit Trail
Every decision, every enforcement action, every state change is traceable. Replay capability for compliance.

### Fail-Closed Behavior
When required knowledge is missing, the system refuses rather than hallucinates. Epistemic integrity enforced.

---

## The Paradigm Shift

**From:**
```
Model is the mind
Model owns state
Model controls behavior
Prompts shape output
```

**To:**
```
Runtime is the mind
Substrate owns state
Runtime controls behavior
Architecture enforces guarantees
```

**This is the OS kernel abstraction for AI systems.**

---

## What This Document Does NOT Contain

This document describes the **conceptual architecture** - what PCS does and why it matters.

**It does NOT contain:**
- Scoring algorithms or formulas
- Primitive names or catalog
- Implementation details
- Test code or test data
- RFC specifications
- Source code or pseudocode

**Those are available under NDA to qualified engineering teams.**

See [NDA_ACCESS.md](NDA_ACCESS.md) for the evaluation process.

---

## Critical Test

**Could a competent engineer read this and build a competing implementation?**

**Answer:** They would understand the architecture but couldn't replicate the specific mechanisms.

That's the right level for public specification.

---

## Next Steps

**To understand the capabilities:** Read [CAPABILITY_MAP.md](CAPABILITY_MAP.md)

**To understand the distinction from RAG:** Read [WHY_NOT_RAG.md](WHY_NOT_RAG.md)

**To see validation results:** Read [VALIDATION_SUMMARY.md](VALIDATION_SUMMARY.md)

**To request full access:** Read [NDA_ACCESS.md](NDA_ACCESS.md)

---

**The architecture is conceptual. The implementation is real. The validation is complete.**

**Version:** 1.0.0 (Public Specification)
