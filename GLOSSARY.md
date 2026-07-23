# PCS Glossary

**Purpose:** Canonical definitions of PCS terminology for engineers, evaluators, and decision-makers.

**Audience:** Anyone reviewing PCS architecture, documentation, or implementations.

This glossary provides clear definitions of terms used throughout PCS documentation. For architectural context, see [ARCHITECTURE_OVERVIEW.md](ARCHITECTURE_OVERVIEW.md). For validation evidence, see [VALIDATION_SUMMARY.md](VALIDATION_SUMMARY.md).

---

## Foundational Concepts

### AI Cognition
The reasoning, decision-making, and state-maintenance processes performed by AI systems. Traditionally confined within model context windows, but externalized in PCS architecture to enable persistence and governance.

**Why this matters:** Understanding that cognition can be separated from the inference engine is fundamental to the PCS architectural model.

### Cognitive Infrastructure
Foundational architectural layer that provides persistent state, governance, and continuity capabilities for AI systems, analogous to how operating systems provide infrastructure for applications.

**Why this matters:** Positions PCS as infrastructure, not a feature or tool.

### External Cognitive Infrastructure
Architectural pattern where cognitive state (decisions, policies, context, provenance) is maintained outside the inference engine in a persistent substrate layer, enabling continuity, governance, and model-agnostic operation.

**Related terms:** Exocortical Substrate, Persistent State, Cognitive State

**Why this matters:** This is the core architectural thesis of PCS - moving cognitive state out of models into external infrastructure.

### Exocortex
External cognitive extension analogous to the human brain's cortex, providing persistent memory and reasoning support outside the core processing unit. In PCS, the substrate layer functions as an exocortex for AI systems.

**Related terms:** External Cognitive Infrastructure, Exocortical Substrate

**Why this matters:** Just as humans use external tools (notebooks, databases) to extend memory beyond biological limits, AI systems need external infrastructure to maintain state beyond context window limits.

### Exocortical Substrate
The persistent infrastructure layer that serves as external cognitive storage and coordination for AI systems, maintaining state that would otherwise be lost across session boundaries.

**Related terms:** Exocortex, External Cognitive Infrastructure, PCS

**Why this matters:** This term emphasizes the substrate nature of PCS - it's the foundation layer, not an application.

---

## State and Persistence

### State
The collection of information representing an AI system's current context, including decisions, policies, constraints, vision, and reasoning artifacts.

**Related terms:** Cognitive State, Persistent State, Critical State

### Cognitive State
Persistent representation of an AI system's decisions, policies, context, and reasoning artifacts that survive beyond individual inference operations.

**Related terms:** State, Persistent State, Memory Graph

**Why this matters:** Cognitive state is what enables continuity across sessions, operators, and models.

### Persistent State
Cognitive state that survives beyond individual inference operations, sessions, or model swaps, maintained in durable storage outside the inference engine.

**Related terms:** Cognitive State, Memory Graph, Session Boundary

**Why this matters:** Persistence is what differentiates PCS from prompt-based or RAG-based approaches that lose state across sessions.

### Critical State
Cognitive state artifacts essential for maintaining continuity, governance, and decision coherence across sessions. Examples include architectural decisions, binding policies, and project vision.

**Related terms:** Persistent State, Decision Record, Policy Record, Vision Anchor

**Why this matters:** Not all state is equally important - critical state must be preserved and governed to maintain system reliability.

### Persistence
The property of cognitive state remaining available and retrievable across session boundaries, model changes, and time, enabling long-horizon continuity.

**Related terms:** Persistent State, Session Boundary, Long-horizon Reasoning

**Why this matters:** Persistence enables AI systems to maintain coherence over days, weeks, or months - not just within a single conversation.

### Memory Graph
Graph-structured representation of persistent cognitive state showing relationships between decisions, policies, context, and provenance, enabling semantic retrieval and reasoning continuity.

**Related terms:** Cognitive State, Persistent State, Contextual Salience Engine

**Why this matters:** Graph structure enables semantic relationships and contextual retrieval that flat storage cannot provide.

---

## Architectural Components

### PCS (Persistent Cognitive Substrate)
External cognitive infrastructure for AI systems that externalizes state, governance, and continuity into a persistent substrate layer, enabling model-agnostic, governed, and continuous AI operations.

**Related terms:** External Cognitive Infrastructure, Exocortical Substrate

**Why this matters:** PCS is the complete architectural system, not just one component.

### Inference Engine
The underlying language model or AI system that performs reasoning operations (e.g., GPT-4, Claude, Llama). In PCS architecture, the inference engine operates against authoritative cognitive state maintained in the substrate.

**Related terms:** Execution Engine, Model-Agnostic

**Why this matters:** PCS treats inference engines as interchangeable execution units, not as the location of cognitive state.

### Execution Engine
Synonym for Inference Engine. The underlying language model or AI system that performs reasoning operations against authoritative cognitive state maintained in the PCS substrate.

**Related terms:** Inference Engine, Model-Agnostic

### Meta-Cognitive Layer
Self-awareness capability enabling AI systems to reason about their own cognitive state, limitations, and processes. Includes vision-guided reasoning, flow-aware continuation, and emergent capability discovery.

**Related terms:** Meta-programming, Emergent Skills, Vision Anchor

**Why this matters:** Meta-cognitive capabilities enable AI systems to adapt and improve based on persistent state and usage patterns.

### Meta-programming
Self-modifying or self-aware programming capabilities where AI systems can reason about and adapt their own cognitive processes, enabled by persistent state and the meta-cognitive layer.

**Related terms:** Meta-Cognitive Layer, Emergent Skills

**Why this matters:** Meta-programming enables AI systems to discover patterns, learn from experience, and adapt to project evolution.

### Contextual Salience Engine (CSE)
Relevance determination mechanism operating at the retrieval boundary between persistent state and inference context. Determines which cognitive state artifacts are most relevant for a given reasoning operation.

**Related terms:** Memory Graph, Persistent State, Retrieval Primitives

**Why this matters:** CSE solves the "what to retrieve" problem - not all persistent state is relevant to every operation.

---

## Reasoning and Continuity

### Long-horizon Reasoning
Cognitive processes spanning multiple sessions, days, or weeks that require persistent state to maintain coherence and avoid re-grounding. Examples include multi-week engineering projects, extended operational planning, or institutional memory maintenance.

**Related terms:** Persistent State, Session Boundary, Continuity

**Why this matters:** Most current AI systems fail at long-horizon tasks because they lose state. PCS enables reliable long-horizon reasoning.

### Session Boundary
Transition point between discrete cognitive sessions where state must be preserved or restored. Without PCS, crossing session boundaries typically results in state loss and re-grounding overhead.

**Related terms:** Persistent State, Continuity, Session Boundary Manager

**Why this matters:** Session boundaries are where traditional AI systems lose coherence. PCS preserves state across these boundaries.

### Continuity
The property of cognitive reasoning maintaining coherence across session boundaries, model swaps, operator handoffs, and time, enabled by persistent state in the substrate.

**Related terms:** Session Boundary, Persistent State, Long-horizon Reasoning

**Why this matters:** Continuity is what enables reliable multi-session workflows and operator handoffs.

### Token Boundary
Limit of inference engine context window requiring cognitive state preservation for continuity. PCS maintains state beyond token boundaries in persistent substrate.

**Related terms:** Session Boundary, Persistent State

**Why this matters:** Token limits are a fundamental constraint of current AI systems. PCS works around this by externalizing state.

---

## Governance and Policy

### Policy Enforcement
Deterministic validation of actions against governance constraints occurring outside the inference engine, before execution proceeds.

**Related terms:** Policy Record, Policy Enforcement Point, Deterministic Governance

**Why this matters:** Policy enforcement in PCS is structural and deterministic, not advisory or prompt-based.

### Deterministic Governance
Governance mechanisms whose behavior is mechanically verifiable and reproducible, independent of model inference. Policies are enforced at runtime boundaries, not through prompts.

**Related terms:** Policy Enforcement, Policy Enforcement Point, Fail-Closed

**Why this matters:** Deterministic governance provides compliance guarantees that prompt-based governance cannot.

### Fail-Closed
Security property where policy violations result in operation blocking (refusal) rather than degraded enforcement. The system fails to a safe state rather than allowing policy violations.

**Related terms:** Policy Enforcement, Deterministic Governance

**Why this matters:** Fail-closed behavior is essential for mission-critical and compliance-sensitive applications.

### Policy Record
Persistent constraint or governance rule enforced deterministically across inference operations. Stored in substrate and enforced at runtime boundaries.

**Related terms:** Policy Enforcement, Decision Record, Persistent State

**Why this matters:** Policy records are binding constraints, not suggestions - they cannot be bypassed by model behavior.

### Policy Enforcement Point
Deterministic gating mechanism that validates actions against policy constraints before allowing execution to proceed.

**Related terms:** Policy Enforcement, Policy Record, Deterministic Governance

**Why this matters:** The enforcement point is where governance actually happens - at the runtime boundary, not in the model.

---

## State Primitives

### Decision Record
Durable representation of an architectural decision made by or with an AI system. Stored in persistent substrate and retrievable across sessions.

**Related terms:** Persistent State, Memory Graph, Provenance Event

**Why this matters:** Decision records enable continuity - new sessions can retrieve past decisions without re-grounding.

### Vision Anchor
Persistent cognitive state artifact representing overarching project intent, architectural principles, or mission objectives. Guides reasoning across sessions.

**Related terms:** Decision Record, Meta-Cognitive Layer, Persistent State

**Why this matters:** Vision anchors provide consistent direction across long-horizon workflows.

### Provenance Event
Immutable record of a cognitive decision's lineage, including inputs, reasoning context, and decision rationale. Enables audit trails and deterministic replay.

**Related terms:** Decision Record, Audit Trail, Epistemic Integrity

**Why this matters:** Provenance enables verification, compliance, and understanding of how decisions were made.

### Attestation Bundle
Verifiable evidence package with tamper-evident metadata proving cognitive state conforms to specified policies.

**Related terms:** Provenance Event, Policy Record, Epistemic Integrity

**Why this matters:** Attestation bundles provide cryptographic proof of compliance for audit and verification.

---

## Advanced Concepts

### Emergent Skills
Learned cognitive capabilities that develop through persistent state usage patterns. AI systems discover and reinforce effective reasoning patterns over time.

**Related terms:** Meta-Cognitive Layer, Meta-programming, Cognitive Pattern Reinforcement

**Why this matters:** Emergent skills enable AI systems to improve through experience, not just through model training.

### Epistemic Integrity
The property of cognitive state remaining internally consistent, verifiable, and traceable to authoritative sources, preventing corruption or drift in reasoning foundations.

**Related terms:** Provenance Event, Attestation Bundle, Deterministic Governance

**Why this matters:** Epistemic integrity ensures that reasoning is based on valid, traceable foundations.

### Model-Agnostic
Design property enabling functionality to operate across different inference engines (GPT-4, Claude, Llama, etc.) without modification. PCS maintains state independently of which model is executing.

**Related terms:** Inference Engine, Execution Engine, Provider-Agnostic

**Why this matters:** Model-agnostic architecture prevents vendor lock-in and enables model swapping based on cost, capability, or deployment constraints.

### Provider-Agnostic
Design property enabling functionality to operate across different model providers (OpenAI, Anthropic, local models, etc.) without modification.

**Related terms:** Model-Agnostic, Pluggable Provider Interface

**Why this matters:** Provider-agnostic architecture enables deployment flexibility and competitive model selection.

---

## Validation and Conformance

### EVS (Execution Validation Suite)
Test suite validating core PCS primitives including state persistence, policy enforcement, session continuity, and model swap capability. 21 tests covering 123+ assertions.

**Related terms:** AVS, CTS, Conformance Testing

**Why this matters:** EVS proves that PCS primitives work as specified.

### AVS (Architectural Validation Suite)
Test suite validating architectural properties of PCS implementations, including cross-session continuity and deterministic policy enforcement.

**Related terms:** EVS, CTS, Conformance Testing

**Why this matters:** AVS proves that PCS architecture delivers on its core promises.

### CTS (Conformance Testing Suite)
Test suite validating deterministic behavior of PCS components at multiple conformance levels.

**Related terms:** EVS, AVS, Conformance Levels

**Why this matters:** CTS enables independent verification of PCS implementations.

---

## Related Documentation

- **Architecture:** [ARCHITECTURE_OVERVIEW.md](ARCHITECTURE_OVERVIEW.md)
- **Validation:** [VALIDATION_SUMMARY.md](VALIDATION_SUMMARY.md)
- **Capabilities:** [CAPABILITY_MAP.md](CAPABILITY_MAP.md)
- **Getting Started:** [README.md](README.md)

---

**Last Updated:** May 2026  
**Version:** 1.0 (Public Release Candidate)
