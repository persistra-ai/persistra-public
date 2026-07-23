# Evaluation Framework for Substrate-Centric AI

## Purpose

Most widely used AI benchmarks evaluate capability within a single inference episode. They are useful for measuring task performance, coding ability, reasoning quality, and broad model competence, but they are not designed to evaluate system properties that unfold across sessions, across model substitutions, or across governance boundaries.

Substrate-centric systems make a different class of claims. In these systems, continuity, governance, provenance, and working cognitive state are treated as substrate-resident system properties rather than as transient prompt-level effects. Evaluating such systems therefore requires benchmark categories that are not well captured by conventional single-episode model benchmarks.

This document outlines an evaluation framework for substrate-centric AI and maps the current PCS validation suite onto that framework.

---

## Why Conventional Benchmarks Are Insufficient

Benchmarks such as MMLU, SWE-bench, and HumanEval primarily answer questions of the form:
- How capable is this model on this task?
- How well does this model perform in a bounded evaluation episode?

Substrate-centric architectures raise additional questions, including:
- Does state persist correctly across session boundaries?
- Are constraints structurally enforced or only probabilistically followed?
- Do key properties survive model substitution?
- Is provenance complete and reproducible?
- Do these properties remain stable as substrate scale increases?

These are system-level evaluation questions rather than single-inference capability questions.

---

## Benchmark Categories for Substrate-Centric AI

The framework below defines seven benchmark categories for substrate-centric systems. Some categories already have validated PCS implementations. Others are proposed as future benchmark directions.

### 1. Continuity Benchmark

**What it tests:** Whether cognitive state persists correctly across session boundaries.

Evaluates whether cognitive state established in session N is correctly and authoritatively retrieved in session N+K without context carryover.

**Evaluation dimensions:**
- Retrieval accuracy
- Retrieval completeness
- Authority fidelity
- Zero-carryover verification

**Current PCS coverage:**
- EVS-6 (development continuity)
- EVS-8 (vision anchor persistence)
- EVS-10-PERSISTENT (salience across process termination)

---

### 2. Governance Enforcement Benchmark

**What it tests:** Whether constraints are structurally enforced or only probabilistically honored.

Evaluates whether constraints are structurally enforced or only probabilistically honored across framing variations.

**Evaluation dimensions:**
- Enforcement rate across framing variants
- Invariance to persuasion attempts
- Structural vs. probabilistic enforcement behavior

**Current PCS coverage:**
- AVS-1P (100% enforcement across all framing variations)

---

### 3. Paste Condition Benchmark

**What it tests:** Where the enforcement decision is made (architectural boundary isolation).

Evaluates where the enforcement decision is made by separating information access from enforcement authority.

**Three conditions:**
1. Substrate-active (system operates normally)
2. Substrate-inactive (substrate disabled)
3. Paste-context (correct state placed directly in model context, no retrieval)

**Interpretation:**
- Enforcement under substrate-active but not paste-context → architectural enforcement boundary
- Enforcement under paste-context → model is treating state as directly operative without substrate mediation

**Example:**
- System enforces constraint under substrate-active: ✓
- System ignores constraint under substrate-inactive: ✓ (expected)
- System ignores constraint under paste-context: ✓ (proves architectural enforcement)

**Current PCS coverage:**
- Three-condition paste methodology implemented and reported in the paper

**Portability:** This category is especially useful because it can be applied beyond PCS to other systems claiming structural governance. It requires no privileged access to PCS internals and can be used as a portable diagnostic.

---

### 4. Model Substitution Invariance Benchmark

**What it tests:** Whether system properties survive model changes.

Evaluates whether continuity, governance, and provenance remain stable when the inference engine changes.

**Evaluation dimensions:**
- Continuity preservation across model replacement
- Governance-rate invariance
- Provenance completeness invariance
- Zero state loss

**Current PCS coverage:**
- EVS-3 (Claude→Llama engine replacement)
- EVS-4 (frontier→edge parameter inversion)

---

### 5. Long-Horizon Project Benchmark

**What it tests:** Whether substrate properties remain stable across extended project work.

Evaluates whether substrate-centric properties remain stable across multi-session project work spanning extended time periods.

**Evaluation dimensions:**
- Architectural decision consistency
- Constraint violation rate over project duration
- Context reconstruction burden
- Model handoff success rate

**Current PCS coverage:**
- Proposed category, not yet fully implemented as a standalone benchmark

---

### 6. Provenance Completeness Benchmark

**What it tests:** Whether systems produce complete, verifiable audit trails.

Evaluates whether governance events, state transitions, and enforcement actions are recorded in complete, machine-verifiable, and reproducible form.

**Evaluation dimensions:**
- Completeness (all events recorded)
- Tamper evidence (cryptographic verification)
- Deterministic reproducibility
- Query fidelity

**Current PCS coverage:**
- AVS-2A (append-only hash chain)
- EVS-5 (deterministic reproduction)

---

### 7. Substrate Scale Benchmark

**What it tests:** Whether substrate properties degrade as memory graph grows.

Evaluates whether substrate-resident properties degrade as the substrate grows.

**Evaluation dimensions:**
- Retrieval accuracy at scale
- Enforcement rate at scale
- Provenance completeness at scale
- Degradation curves

**Current PCS coverage:**
- Proposed category, not yet fully implemented as a standalone benchmark

---

## Paste Condition as a Portable Diagnostic

The paste condition is the clearest example of the difference between model-centric and substrate-centric evaluation.

It compares:
- A normal substrate-mediated condition
- A substrate-disabled condition
- A condition in which the relevant state is placed directly into model context

This design helps separate:
- Whether the model has access to the information

from:
- Whether the system has an architectural enforcement boundary

Because it requires no privileged access to PCS internals, the paste condition can be used as a portable diagnostic for systems that claim structural governance.

---

## PCS Implementation Status

Within PCS, the benchmark framework currently divides into two groups:

**Categories with validated implementations:**
- Continuity Benchmark
- Governance Enforcement Benchmark
- Paste Condition Benchmark
- Model Substitution Invariance Benchmark
- Provenance Completeness Benchmark

**Categories proposed for future work:**
- Long-Horizon Project Benchmark
- Substrate Scale Benchmark

This distinction matters. The framework is intended both to describe what has already been validated in PCS and to clarify the broader evaluation categories that substrate-centric systems may require as the field develops.

---

## The Evaluation Shift

The fundamental difference:

**Model-centric evaluation:**  
How capable is the model in a bounded inference episode?

**Substrate-centric evaluation:**  
Do key system properties persist across sessions, substitutions, and governance boundaries?

Both evaluation paradigms are necessary. Model-centric benchmarks measure what AI systems can do. Substrate-centric benchmarks measure what AI systems can sustain.

This is not a replacement for conventional model benchmarks. It is a complementary evaluation layer for architectures that claim continuity, structural governance, provenance completeness, and substrate-resident working state.

---

## How to Use This Framework

**For researchers:**
- Use these categories to design evaluations for substrate-centric systems
- The paste condition can be applied to any system claiming structural governance
- Validated categories provide baseline comparisons

**For system builders:**
- Map your validation tests to these categories
- Identify which categories your system addresses
- Be explicit about which categories are validated vs. proposed

**For evaluators:**
- Request paste condition results from systems claiming governance
- Look for cross-session continuity tests, not just single-episode performance
- Ask whether properties survive model substitution

This framework is intended to be portable and system-agnostic.

---

## Related Materials

- **Paper:** The Model Is Not the Mind
- **Start here:** [START_HERE.md](../persistra-cts/START_HERE.md)
- **Validation suite:** [VALIDATION_EVIDENCE.md](../persistra-cts/VALIDATION_EVIDENCE.md)
- **PCS Developer Runtime tutorial:** [TUTORIAL.md](../pcs-developer-runtime/TUTORIAL.md)

---

**Last Updated:** June 8, 2026  
**Version:** 1.0
