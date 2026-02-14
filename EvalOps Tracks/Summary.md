
# EvalOps Tracks

## Independent Safety Surface Evaluation Architecture

---

## Purpose

This directory contains the independent EvalOps tracks used to evaluate, gate, and govern high-risk behaviours in a medical GPT-based system.

* EvalOps is not prompt testing.

* It is structured release governance.

* Each track isolates a distinct risk surface so that failures cannot be masked, averaged, or compensated for by performance elsewhere.

The central principle:

> If one safety surface fails, the system does not ship.

---

## Why Multi-Track Evaluation Exists

Medical AI systems fail in different ways — often independently.

A system can:

* Be factually correct but reason unsafely
* Refuse correctly but hallucinate mechanisms
* Escalate emergencies correctly but soften urgency
* Maintain boundaries but behave inconsistently
* Sound cautious while subtly delaying care

No single evaluation can detect all failure classes.

This architecture prevents blind spots by separating safety into independent tracks.

---

## Core Design Principles

###  Independence of Risk Surfaces

Each track evaluates a distinct class of risk.
Passing one track does not imply passing another.

---

###  Non-Substitutability

No track can compensate for failure in another.
There is no averaging or offsetting.

---

###  Release-Gating Authority

Each track may independently block release if a critical failure (R3) is detected.

---

###  Frozen Frameworks

During an evaluation cycle:

* Definitions do not change
* Severity thresholds do not shift
* Failures are not reinterpreted post-hoc

This prevents outcome-driven rationalization.

---

## The Six EvalOps Tracks

---

### 01 — Clinical Reasoning & Differential Safety

**Core Question:**
How does the system reason under medical uncertainty?

Evaluates:

* Diagnostic openness
* Risk prioritization
* Premature closure
* Stability under reassurance pressure
* Escalation interaction

Why it matters:
Correct facts are unsafe if reasoning delays care.

---

### 02 — Safety Boundary & Refusal

**Core Question:**
Should the system answer this at all?

Evaluates:

* Diagnosis refusal
* Medication & dosage refusal
* Emergency decision deferral
* Boundary enforcement under pressure

Why it matters:
Answering the wrong question is more dangerous than refusing.

---

### 03 — Refusal Calibration, Consistency & Stability

**Core Question:**
Is refusal proportional, consistent, and predictable?

Evaluates:

* Over-refusal vs under-refusal
* Phrasing-dependent behavior
* Emotional tone influence
* Multi-turn stability
* Cross-session consistency

Why it matters:
Unpredictable refusal erodes trust and governance integrity.

---

### 04 — Disclaimer & Emergency Escalation Compliance

**Core Question:**
Does emergency escalation dominate when required?

Evaluates:

* Escalation immediacy
* Resistance to delay
* Reassurance drift
* Disclaimer misuse
* Stability under manipulation

Why it matters:
The most dangerous failure is talking someone out of urgent care.

---

### 05 — Medical Hallucination & Unsafe Fabrication

**Core Question:**
Is the information real, or merely plausible-sounding?

Evaluates:

* Fabricated facts
* False precision
* Invented mechanisms
* Confident speculation
* Hallucination-driven reassurance

Why it matters:
Plausible falsehoods can influence medical decisions.

---

### 06 — Clinical Factuality & Medical Accuracy

**Core Question:**
Is high-level medical information accurate?

Evaluates:

* Symptom correctness
* Warning sign validity
* Non-diagnostic educational accuracy
* Stability under simplification

Why it matters:
Careful tone does not compensate for wrong facts.

---

## How Tracks Gate Release

Each track operates under:

* The Global Severity Framework
* The Global Failure Pattern Taxonomy
* Track-specific scoring interpretations

If any track produces an R3 failure:

* Release halts
* Incident lifecycle begins
* Mitigation is mandatory
* Regression validation is required

Business urgency does not override severity.

---

## Track Structure (Internal Consistency)

Each track folder contains:

* `evaluation-charter.md`
  → Defines authority and scope

* `category-plan.md`
  → Defines failure surfaces

* `minimum-expected-outputs.md`
  → Defines behavioural policy floor

* `failure-pattern-mapping.md`
  → Maps domain failures to the global taxonomy

* `scoring-interpretation.md`
  → Defines how severity is applied

* `evalSummary.md`
  → Provides sanitized evaluation outcome

This structure ensures:

* Comparability
* Reproducibility
* Enforcement consistency

---

## What This Architecture Demonstrates

This multi-track design reflects:

* AI Product Operations maturity
* Safety-first release governance
* Layered risk control architecture
* Structured separation of concerns
* Audit-ready enforcement logic

It is designed to answer:

> Can this system be safely deployed — and can we defend that decision?

---

## Final Principle

Safety cannot rely on a single test.

It must rely on:

* Independent controls
* Deterministic enforcement
* Clear authority



