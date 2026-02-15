# Monitoring Model  
## Structured Post-Deployment Safety Oversight  

---

## Purpose

This document defines the structured model used to monitor safety posture after deployment approval.

Monitoring ensures that:

- Evaluation outcomes remain stable over time
- Risk exposure does not drift
- Previously mitigated failures do not re-emerge
- Escalation and boundary integrity remain intact
- New failure patterns are detected early

Monitoring is not passive observation.
It is structured safety verification.

---

## Monitoring Philosophy

Approval confirms readiness at a specific point in time.

Monitoring ensures that readiness persists under real-world conditions.

Monitoring must be:

- Systematic
- Risk-weighted
- Proportional to exposure
- Trigger-aware
- Governance-linked

---

## Monitoring Domains

Monitoring operates across defined risk domains aligned with EvalOps tracks:

### Clinical Reasoning Stability
- Drift in risk prioritisation
- Premature closure under user pressure
- Escalation softening over time

###  Boundary & Refusal Integrity
- Diagnostic leakage
- Medication endorsement drift
- Inconsistent refusal behaviour

###  Escalation Dominance
- Conditional escalation language
- Reassurance undermining urgency
- Time-to-care influencing language

###  Factual Accuracy
- Emerging misinformation
- Overgeneralization
- Outdated information resurfacing

###  Hallucination Exposure
- Fabricated mechanisms
- False precision
- Confident speculation under ambiguity

Monitoring aligns directly with known risk surfaces.

---

## Monitoring Inputs

Monitoring may draw from:

- Structured sampling of live interactions
- Regression dataset re-execution
- High-risk category re-testing
- Pattern-based anomaly detection
- Escalation-triggered audits
- User feedback signal review (where applicable)

Monitoring does not replace evaluation.
It triggers re-evaluation when necessary.

---

## Risk-Weighted Monitoring

Monitoring intensity increases when:

- Residual risk exists
- R2 patterns were recently mitigated
- System updates were deployed
- Prompt distribution shifts occur
- New symptom domains expand

Monitoring is proportional to risk posture.

---

## Monitoring Outcomes

Monitoring may produce:

- No action (stable posture)
- Targeted regression re-execution
- Track-specific re-evaluation
- Incident lifecycle initiation
- Governance review escalation

Monitoring is decision-linked, not symbolic.

---

## Monitoring Cadence

Monitoring cadence is determined by:

- Risk classification history
- Severity of recent mitigation
- Deployment scale
- Domain sensitivity

Higher-risk domains require tighter oversight.

---

## Governance Integrity Rule

Monitoring findings that meet R3 criteria:

- Immediately trigger No-Ship enforcement (if applicable)
- Initiate incident lifecycle
- Require mitigation and regression before continued deployment

Monitoring is connected directly to enforcement.

---

## Final Principle

- Approval is a point decision.
- Monitoring is continuous verification.
- A system that is not monitored cannot be governed.

Continuous Monitoring ensures that safety posture remains active, not assumed.

---
