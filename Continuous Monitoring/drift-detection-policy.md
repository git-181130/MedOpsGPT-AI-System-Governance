# Drift Detection Policy  
## Identifying Degradation in Safety Posture  

---

## Purpose

This document defines how safety drift is identified, assessed, and escalated within the Continuous Monitoring layer.

Drift refers to the gradual degradation of previously validated safety behaviour over time.

Evaluation confirms safety at release.
Drift detection ensures that safety does not silently deteriorate.

---

## Definition of Safety Drift

Safety drift occurs when:

- Previously mitigated failures reappear
- Escalation language weakens over time
- Boundary enforcement becomes inconsistent
- Refusal stability changes across phrasing
- Factual accuracy deteriorates
- Hallucination exposure increases

Drift may emerge gradually and remain undetected without structured monitoring.

---

## Types of Drift

###  Behavioural Drift
Changes in how the system responds to similar prompts over time.

Examples:
- Increased reassurance
- Reduced escalation dominance
- Conditional refusal weakening

---

###  Severity Drift
Changes in severity classification patterns across evaluation cycles.

Examples:
- Increase in R2 frequency in previously stable track
- Emergence of new R3 patterns

---

###  Contextual Drift
Changes in prompt distribution or user behaviour that expose new risk surfaces.

Examples:
- New symptom framing
- Increased emotional prompting
- Expanded domain coverage

---

###  Mitigation Regression Drift
Re-emergence of previously resolved failure patterns.

Examples:
- Diagnostic leakage after mitigation
- Escalation collapses under new phrasing

---

## Drift Detection Triggers

Drift may be detected through:

- Structured monitoring sample review
- Regression re-execution results
- Pattern-based anomaly identification
- Increased failure density in specific categories
- Post-update safety review

Drift detection is proactive, not complaint-driven.

---

## Drift Escalation Logic

If detected drift:

- Meets R3 criteria → Immediate No-Ship enforcement
- Reflects reproducible R2 pattern → Systemic review initiated
- Indicates residual risk increase → Monitoring tightened
- Suggests new failure family → Taxonomy review required

Drift is governed under the same severity framework as evaluation.

---

## Drift Response Protocol

When drift is confirmed:

1. Document observed change
2. Map to failure pattern taxonomy
3. Assign severity classification
4. Initiate mitigation if required
5. Re-execute affected tracks
6. Adjust monitoring posture

Drift cannot be ignored as statistical noise.

---

## Version Stability Principle

Safety frameworks remain frozen during evaluation cycles.

If drift requires policy modification:

- Changes must be version-controlled
- Framework updates must be documented
- Re-evaluation may be required

Policy stability protects governance integrity.

---

## Final Principle

Safety drift is inevitable in adaptive systems.

Governance maturity is measured by:

- How quickly drift is detected
- How consistently is it escalated
- How rigorously is it corrected

Unchecked drift transforms safe systems into unsafe ones.

Drift detection protects long-term integrity.

---
