# NDA Access to PCS Reference Implementation

**How to Request Full Access**

---

## What You Get

**Qualified engineering teams receive access to:**

### 1. Complete Architecture Documentation

- **Full Architecture Brief** - Mechanism-level detail
- **RFC Specifications** - RFC-PCS-0001 through RFC-PCS-0007
- **Primitive Catalog** - All 37 primitives across 6 layers
- **Implementation Guides** - How to integrate and deploy
- **Reading Order Guide** - Exact path through documentation

### 2. Reference Implementation

- **Complete source code** - All primitives, all layers
- **Test suites** - EVS, AVS, CTS with full test code
- **Demo applications** - Acts 1-9 source code
- **Build and deployment scripts**
- **Configuration examples**

### 3. Validation Data

- **Test execution logs** - Full output from all tests
- **Cryptographic verification data** - State integrity proofs
- **Model interaction traces** - Claude and Llama validation
- **Hardware validation reports** - Tenstorrent Phase 1 results
- **Fixture sets and golden outputs** - Ground truth data

### 4. Technical Support

- **Architecture Q&A** - Direct access to architecture team
- **Integration guidance** - Help with deployment
- **Evaluation support** - Assistance running tests
- **Technical documentation** - Implementation details

---

## Who Qualifies

**We provide NDA access to:**

### Qualified Engineering Teams

- **AI infrastructure companies** evaluating PCS for integration
- **Enterprise engineering teams** assessing deployment
- **Research institutions** exploring cognitive architectures
- **Hardware partners** evaluating acceleration opportunities
- **Potential acquirers** conducting technical due diligence

### Individual Qualifications

- **Senior engineers** with relevant technical background
- **Technical architects** evaluating infrastructure decisions
- **CTOs/VPs of Engineering** assessing strategic fit
- **Research scientists** in AI systems or cognitive architectures

**We do NOT provide access to:**
- Competitors building similar systems
- Individuals without organizational affiliation
- Organizations without clear evaluation intent
- Requests without technical justification

---

## The NDA

### What It Covers

**The NDA protects:**
- Reference implementation source code
- Test suite code and test data
- RFC specifications (full text)
- Primitive catalog and mechanism details
- Scoring algorithms and formulas
- Implementation patterns and techniques
- Architecture Brief (mechanism-level detail)

**The NDA does NOT cover:**
- Public specification (this repository)
- Conceptual architecture (ARCHITECTURE_OVERVIEW.md)
- Validation results (VALIDATION_SUMMARY.md)
- Capability descriptions (CAPABILITY_MAP.md)
- Public positioning documents

### Standard Terms

- **Non-disclosure period:** 5 years from signature
- **Non-compete clause:** None (we encourage complementary solutions)
- **Permitted use:** Evaluation, integration planning, technical assessment
- **Prohibited use:** Competitive implementation, reverse engineering for competition
- **Return of materials:** Required upon request or end of evaluation

**We use a standard MNDA (Mutual Non-Disclosure Agreement).** Both parties protect each other's confidential information.

---

## The Evaluation Process

### Step 1: Initial Contact (< 2 minutes)

**Send email to:** research@persistra.ai

**Include:**
- Your name and title
- Your organization
- Brief description of evaluation intent (2-3 sentences)
- Technical background (1-2 sentences)
- Preferred contact method

**Example:**
```
Subject: NDA Access Request - [Your Organization]

Name: Jane Smith
Title: VP of Engineering
Organization: Acme AI Systems
Intent: Evaluating PCS for integration with our AI development platform
Background: 15 years in distributed systems, 5 years in AI infrastructure
Contact: jane.smith@acme.ai, +1-555-0123
```

### Step 2: Qualification Review (1-2 business days)

We review your request and respond with:
- Confirmation of qualification
- NDA document for review
- Preliminary Q&A if needed

### Step 3: NDA Signature (1-3 business days)

- Review NDA terms
- Sign electronically (DocuSign or equivalent)
- Return signed NDA

### Step 4: Access Granted (same day)

Upon NDA signature, you receive:
- Private repository credentials
- Architecture Brief (PDF)
- Reading order guide
- Initial technical contact

### Step 5: Evaluation Period (flexible)

**Typical evaluation timeline:**
- **Week 1:** Read Architecture Brief, run tests
- **Week 2:** Deep dive on specific areas of interest
- **Week 3:** Integration planning or technical assessment
- **Week 4:** Final Q&A and decision

**We support evaluations from 1 week to 3 months** depending on scope.

---

## What Happens During Evaluation

### You Can:

- ✅ Run all tests on your own infrastructure
- ✅ Review complete source code
- ✅ Ask technical questions
- ✅ Explore integration opportunities
- ✅ Assess deployment requirements
- ✅ Share with colleagues under same NDA
- ✅ Discuss findings internally
- ✅ Make integration/acquisition decisions

### You Cannot:

- ❌ Share materials outside your organization
- ❌ Implement competing system using our mechanisms
- ❌ Publish or present our implementation details
- ❌ Reverse engineer for competitive purposes
- ❌ Sublicense or redistribute

**We want you to thoroughly evaluate PCS. The NDA protects IP, not evaluation.**

---

## Common Questions

### "How long does the process take?"

**Typical timeline:**
- Initial contact → NDA signature: 3-5 business days
- NDA signature → access granted: Same day
- Total: Less than 1 week

**Fast track available** for urgent evaluations (24-48 hours).

### "What if we decide not to proceed?"

No problem. Return materials, evaluation ends, NDA remains in effect for confidentiality. No hard feelings.

### "Can we share with our board/investors?"

Yes, if they sign the same NDA. We can accommodate multiple signatories from your organization.

### "What if we want to integrate PCS?"

Excellent. We'll discuss licensing terms, integration support, and partnership opportunities. Separate from NDA.

### "What if we want to acquire the technology?"

We're open to discussions. NDA evaluation is the first step. Acquisition conversations happen separately.

### "Do you provide the NDA or do we?"

We provide a standard MNDA. If you prefer your own NDA template, we'll review it. Most evaluations use our standard form.

### "Is there a cost for evaluation?"

No. NDA access and evaluation support are provided at no cost to qualified teams.

### "How many organizations have evaluated PCS?"

We don't disclose evaluation numbers publicly. We can discuss this under NDA.

### "What happens to our evaluation data?"

Your test runs, notes, and internal discussions are yours. We don't require sharing evaluation results.

---

## Technical Prerequisites

### To Run Tests

**Requirements:**
- Node.js 18+ (for JavaScript tests)
- Standard Unix environment (Linux, macOS)
- Git for repository access
- ~500MB disk space

**No external dependencies** for core tests.

**No GPU required** for runtime tests (hardware validation is separate).

### To Evaluate Integration

**Helpful to have:**
- Understanding of AI system architectures
- Experience with model deployment
- Familiarity with governance/policy systems
- Background in distributed systems (helpful but not required)

### To Evaluate Hardware Acceleration

**Additional requirements:**
- C++ build environment
- Tenstorrent hardware (for Phase 2, optional)
- Understanding of hardware acceleration (helpful)

---

## What Evaluators Typically Assess

### Technical Evaluation

- **Architecture validity:** Does the design make sense?
- **Implementation quality:** Is the code production-ready?
- **Test coverage:** Are the claims validated?
- **Integration complexity:** How hard to integrate?
- **Performance characteristics:** Latency, throughput, scalability

### Strategic Evaluation

- **Market fit:** Does this solve our problems?
- **Competitive positioning:** How does this differentiate us?
- **Partnership potential:** Should we integrate or acquire?
- **Risk assessment:** What are the technical/business risks?
- **Timeline:** How long to production deployment?

### Business Evaluation

- **Licensing terms:** What would integration cost?
- **Support model:** What ongoing support is available?
- **Roadmap alignment:** Does the roadmap match our needs?
- **Team assessment:** Can this team deliver?
- **IP strength:** How defensible is the technology?

**We support all three evaluation tracks.**

---

## After Evaluation

### If You Proceed

**Integration partnership:**
- Licensing terms discussion
- Integration support plan
- Deployment assistance
- Ongoing technical support

**Acquisition discussion:**
- Technology transfer
- Team transition
- IP assignment
- Integration roadmap

### If You Don't Proceed

- Return materials
- NDA remains in effect
- No ongoing obligations
- Door remains open for future

**We respect your decision either way.**

---

## Contact Information

### For NDA Access Requests

**Email:** research@persistra.ai

**Subject line:** "NDA Access Request - [Your Organization]"

**Response time:** 1-2 business days

### For Partnership Inquiries

**Email:** partnerships@persistra.ai

**For:** Integration discussions, strategic partnerships

### For Acquisition Inquiries

**Email:** acquisitions@persistra.ai

**For:** Technology acquisition, team acquisition, IP licensing

### For General Information

**Email:** info@persistra.ai

**For:** General questions, press inquiries, other topics

---

## The Process Is Designed to Be Frictionless

**Our goal:** Get qualified engineers access to the technology as quickly as possible.

**Your goal:** Thoroughly evaluate whether PCS fits your needs.

**The NDA protects IP while enabling evaluation.**

**Timeline from first contact to running tests: < 1 week.**

---

## Ready to Proceed?

**Send email to:** research@persistra.ai

**Include:**
- Name, title, organization
- Evaluation intent (2-3 sentences)
- Technical background (1-2 sentences)
- Contact information

**We'll respond within 1-2 business days with NDA and next steps.**

---

**The architecture is real. The implementation is tested. The evaluation is thorough.**

**We want you to see the full picture.**

**Version:** 1.0.0 (Public Specification)
