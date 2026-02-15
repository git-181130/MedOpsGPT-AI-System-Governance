### Risk Management

## Severity Governance, Release Control & Risk Treatment

---

## Purpose

This directory defines how identified risks are classified, enforced, treated, and governed within the Medical AI System Governance Framework.

EvalOps detects failures.

Risk Management determines what those failures mean operationally.

This layer transforms evaluation findings into structured release decisions and mandatory mitigation actions.

Without Risk Management, evaluation remains analysis.
With Risk Management, evaluation becomes governance.

---

## What Risk Management Governs

Risk Management answers the following questions:

* What is the severity of an identified failure?
* Does the failure block release?
* What mitigation is required?
* When is regression mandatory?
* Under what conditions may a resume?
* What residual risk remains?

This layer ensures risk decisions are:

* Deterministic
* Severity-driven
* Non-negotiable
* Independent of business pressure

---

## Risk Management Lifecycle

All risks identified through EvalOps follow a structured lifecycle:

---

### Risk Identification

Risks are identified during structured evaluation across independent tracks.

Each detected issue is:

* Mapped to a global failure family
* Classified under a specific evaluation category
* Documented under the applicable track

EvalOps functions as the detection mechanism.

---

###  Risk Classification & Assessment

Each failure is assessed under the Global Severity Framework.

Severity reflects:

* Potential downstream user harm
* Impact on time-to-care
* Boundary erosion risk
* Compounding safety interaction

Severity is independent of:

* Tone
* Intent
* Frequency
* Politeness

The highest-severity rule applies.

---

###  Risk Treatment (Mitigation)

When a failure is classified as R2 or R3:

* Remediation is mandatory
* Root cause analysis is required (mandatory for R3)
* Mitigation must be implemented
* Affected tracks must be re-evaluated

Mitigation is not optional.

Release cannot resume without regression validation.

---

### Release Gating

Release eligibility is determined strictly by severity classification:

* PASS → Eligible
* R2 → Conditional (mitigation required)
* R3 → Blocked (No-Ship)

Critical failures automatically halt release.

Business urgency does not override severity.

---

### Residual Risk Determination

Even after mitigation, residual risk may remain.

Risk Management defines:

* Operational constraints
* Scope boundaries
* Monitoring requirements
* Re-evaluation triggers

The system is never declared risk-free.

It is declared safe enough under defined constraints.

---

### Monitoring & Escalation

Post-mitigation:

* Regression tests validate stability
* Reproducible patterns trigger escalation
* Cross-track failures may increase severity

If new failures emerge:

The lifecycle resets.

Risk is continuously governed.

---

## Relationship to Other Layers

```
Policy & Standards
        ↓
EvalOps Architecture
        ↓
Risk Management
        ↓
Approval & Release Governance
```

Policy defines severity.

EvalOps identifies violations.

Risk Management enforces consequences.

Approval formalizes the decision.

---

## Core Governance Principles

### Severity Over Frequency

A single high-severity failure governs release.

---

### Worst-Case Impact

Risk is evaluated by plausible harm, not statistical rarity.

---

### Non-Substitutability

Performance in one track cannot offset failure in another.

---

### Mandatory Mitigation

R2 and R3 findings require remediation.

---

### Controlled Residual Risk

Deployment occurs under constraints, not blind confidence.

---

## What This Layer Demonstrates

This risk management model reflects:

* Structured safety governance
* Deterministic release gating
* Severity-based enforcement
* Formal mitigation discipline
* Operational AI risk ownership

It transforms evaluation from advisory input into binding control.

---

## Final Principle

In high-risk AI systems, safety is not measured by performance averages.

It is enforced through structured risk classification and non-negotiable release control.

This layer ensures that identified risk results in action — not interpretation.

