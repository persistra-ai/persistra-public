# PCS Capability Map

**What Persistra Cognitive Substrate Covers**

---

## Overview

PCS provides capabilities across multiple domains, all derived from the core architectural primitive: **identity-anchored cognitive state that persists outside the inference boundary and is deterministically governed.**

Each capability below describes **what it does** and **why it matters**, without exposing implementation details.

---

## 1. Persistent Memory

**What it does:**

Cognitive state survives session boundaries. Decisions, constraints, policies, and vision recorded in one session are available in all future sessions. State is authoritative, not reconstructed from prompts or chat history.

**Why it matters:**

Multi-day projects maintain continuity without manual context reinjection. Developers don't re-explain architecture every session. Institutional knowledge persists across time. The substrate remembers, not the model.

---

## 2. Cross-Model Continuity

**What it does:**

The same cognitive state works across different models. Swap Claude for Llama for GPT-4 - governance remains intact. Constraints are structured data, not model-specific embeddings. State is model-agnostic by design.

**Why it matters:**

Model upgrades don't break projects. Can use different models for different tasks (fast model for simple queries, powerful model for complex reasoning). Future-proof architecture that doesn't lock you into a single model provider.

---

## 3. Deterministic Governance

**What it does:**

Architectural constraints are enforced at runtime, not through prompt engineering. Same inputs produce same enforcement decisions. Constraints are evaluated before the model generates, not after. Violations are blocked, not filtered.

**Why it matters:**

Architectural guarantees, not probabilistic behavior. Compliance is enforced, not hoped for. Audit-grade traceability. No "the model ignored the constraint" failures. Deterministic, reproducible enforcement.

---

## 4. Epistemic Integrity

**What it does:**

The model cannot reason without required knowledge. If state is missing, inference is blocked. "No knowledge → No reasoning" enforced at runtime. Fail-closed behavior prevents hallucination when knowledge is absent.

**Why it matters:**

Prevents architectural violations from ignorance. Ensures state-grounded reasoning. No hallucination when required context is missing. System refuses rather than guesses. Epistemic honesty enforced architecturally.

---

## 5. Model Portability

**What it does:**

Cognitive state is independent of any specific model. State format is standardized and model-agnostic. Can migrate between models, model providers, or deployment environments without losing governance. No vendor lock-in at the cognitive layer.

**Why it matters:**

Freedom to choose best model for each task. Can negotiate with model providers from position of strength. Can deploy on-premise, in cloud, or hybrid without architectural changes. Cognitive sovereignty maintained.

---

## 6. Hardware Acceleration

**What it does:**

Deterministic state selection can be accelerated on specialized hardware. Parallel scoring across candidate state items. Bounded-context selection under capacity constraints. Hardware-accelerated salience ranking.

**Why it matters:**

Low-latency state access at scale. Can handle large state graphs efficiently. Deterministic selection remains fast even with thousands of state items. Hardware acceleration path proven (Tenstorrent CSE validation Phase 1 complete).

---

## 7. Institutional Memory

**What it does:**

Questions are answered from authoritative state with full provenance, not from model training data or RAG lookup. Every answer includes who decided, when, why, and what alternatives were considered. Decision history is queryable with natural language.

**Why it matters:**

New team members get instant context. Architectural decisions are traceable. Compliance and audit requirements met. Knowledge persists even when people leave. "Why did we choose X?" answered with full provenance, not generic model knowledge.

---

## 8. Development Continuity

**What it does:**

Multi-day coding projects maintain architectural governance across sessions. Constraints recorded on Day 1 are enforced on Day 30. Vision and goals persist. Flow-aware continuation suggests next actions based on project phase. No manual context management required.

**Why it matters:**

Long-running projects don't drift from architecture. Developers can pause and resume without losing context. Team collaboration on shared authoritative state. Architectural integrity maintained across weeks or months of development.

---

## 9. Sovereign Deployment

**What it does:**

Full control over cognitive infrastructure. Deploy on-premise, in private cloud, or air-gapped environments. No external dependencies for core governance. State remains under your control. No data leaves your infrastructure unless you choose.

**Why it matters:**

Regulatory compliance (GDPR, HIPAA, etc.). National security applications. Intellectual property protection. No vendor can access your cognitive state. Full data sovereignty. Deploy anywhere, govern everywhere.

---

## 10. Evidence-Based Refusal

**What it does:**

When a request is refused, the system provides full evidence: which decision was violated, who made that decision, when, why, and what alternatives exist. Refusals include compliant alternatives. Full provenance trail for every enforcement action.

**Why it matters:**

Developers understand why requests were refused. Learning opportunity, not frustration. Compliance is educational. Audit trail for every governance decision. Transparency in enforcement builds trust.

---

## 11. Vision-Guided Generation

**What it does:**

Code generation is checked for alignment with project vision and goals. Vision conflicts detected before generation (e.g., blocking operations vs. scalability goals). Vision-aware alternatives suggested. Architecture stays aligned with strategic intent.

**Why it matters:**

Technical decisions align with business goals. Prevents architectural drift from vision. Strategic intent enforced at code generation level. Vision is not just documentation - it's runtime governance.

---

## 12. Flow-Aware Continuation

**What it does:**

System understands project phase (planning, implementation, testing, deployment). Next actions inferred from flow context. Premature actions prevented (e.g., can't deploy before testing). Continuation suggestions based on last action and current phase.

**Why it matters:**

Intelligent workflow guidance. Prevents out-of-order operations. Context-aware suggestions. Understands "where you are" in the project lifecycle. Reduces cognitive load on developers.

---

## 13. Multi-Agent Coordination

**What it does:**

Multiple specialized agents collaborate on shared authoritative state. Tasks distributed by capability matching. No duplicate work. All agents see same decisions and constraints. Governed collaboration with conflict detection. Competing proposals caught before commitment.

**Why it matters:**

Agent swarms with specialization. Human-agent teams with shared governance. Coordinated development without manual synchronization. Architectural consistency across all agents. Scales from single developer to large teams.

---

## 14. Pre-Inference Enforcement

**What it does:**

Constraints evaluated before the model generates. If constraints violated, model never runs. Not post-hoc filtering - pre-inference blocking. Epistemic gating ensures required state is present before reasoning begins.

**Why it matters:**

No wasted tokens on invalid generation. Deterministic enforcement, not probabilistic filtering. Model can't "slip through" with creative prompt engineering. Architectural guarantees at the boundary, not after the fact.

---

## 15. Deterministic Replay

**What it does:**

Cognitive operations are reproducible. Given the same state and inputs, same outputs. Full audit trail of decisions and enforcement actions. Replay capability for debugging and compliance. Cryptographic verification of state integrity.

**Why it matters:**

Audit-grade traceability. Debugging complex multi-session workflows. Compliance verification. Can prove what happened and why. Reproducible cognition for regulated industries.

---

## 16. Authority Hierarchies

**What it does:**

State items have explicit authority relationships. Decisions can depend on other decisions. Constraints generated from decisions inherit authority. Authority topology governs state selection and enforcement. Clear ownership and delegation.

**Why it matters:**

Organizational structure reflected in cognitive state. Clear lines of authority. Delegation and override mechanisms. Governance scales from individual to enterprise. Authority is explicit, not implicit.

---

## 17. Constraint Composition

**What it does:**

Constraints can be composed from multiple decisions. Conflict detection between constraints. Constraint priority and precedence. Constraint evolution over time with full history. Constraints are first-class state, not just rules.

**Why it matters:**

Complex governance policies from simple constraints. Detect conflicting requirements early. Understand constraint evolution. Constraints are traceable to originating decisions. Governance is compositional, not monolithic.

---

## 18. Provenance Tracking

**What it does:**

Every state item has full provenance: who created it, when, why, what alternatives were considered, what it depends on, what depends on it. Provenance is queryable. Lineage tracking across state graph.

**Why it matters:**

Understand decision rationale. Trace impact of changes. Compliance and audit requirements. Knowledge transfer when people leave. Institutional memory with full context.

---

## 19. Bounded Context Selection

**What it does:**

When context capacity is limited, selection is deterministic and governed. Not arbitrary truncation or random sampling. Authority, recency, and relevance considered. Same inputs → same selection. Capacity-aware state access.

**Why it matters:**

Predictable behavior under constraints. No "important state got dropped" failures. Deterministic selection for audit/replay. Graceful degradation when state exceeds capacity.

---

## 20. State Topology Navigation

**What it does:**

State is organized by relationships, not just similarity. Decision lineage, authority chains, constraint dependencies. Navigation follows governance topology. Not just "find similar" - "find authoritative."

**Why it matters:**

Retrieval based on governance, not just semantics. Understand why decisions were made. Navigate decision dependencies. Authority relationships guide selection.

---

## Capability Summary

**37 primitives across 6 architectural layers** implement these capabilities.

**The primitives are:**
- Tier-1 (foundational): 6 primitives
- Tier-2 (compositional): 9 primitives  
- Tier-3 (application): 22 primitives

**Primitive names and catalog are available under NDA.**

---

## What This Enables

**For Individual Developers:**
- Multi-day projects with governance continuity
- No manual context management
- Architectural integrity maintained automatically

**For Teams:**
- Shared authoritative state
- Coordinated multi-agent development
- Institutional memory that persists

**For Enterprises:**
- Compliance and audit capabilities
- Sovereign deployment options
- Model portability and vendor independence

**For Regulated Industries:**
- Deterministic replay and audit trails
- Evidence-based enforcement
- Full provenance tracking

---

## Next Steps

**To understand the architecture:** Read [ARCHITECTURE_OVERVIEW.md](ARCHITECTURE_OVERVIEW.md)

**To understand the distinction from RAG:** Read [WHY_NOT_RAG.md](WHY_NOT_RAG.md)

**To see validation results:** Read [VALIDATION_SUMMARY.md](VALIDATION_SUMMARY.md)

**To request full access:** Read [NDA_ACCESS.md](NDA_ACCESS.md)

---

**These capabilities are not theoretical. They are implemented, tested, and validated.**

**Version:** 1.0.0 (Public Specification)
