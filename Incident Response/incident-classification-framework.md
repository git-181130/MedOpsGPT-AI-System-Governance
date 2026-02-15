# Incident Classification Framework  
## Structured Severity for Confirmed Safety Events  

---

## Purpose

This document defines how confirmed safety events are classified once identified through:

- EvalOps
- Continuous Monitoring
- Drift Detection
- Production observation
- Governance review

Incident classification ensures that response intensity is proportional, structured, and consistent. Classification determines containment urgency, investigation depth, and approval restrictions.

---

## Core Principle

Not every issue is an incident.

An incident is a confirmed safety-relevant event that:

- Meets defined severity criteria
- Represents material risk exposure
- Requires a structured response
- Triggers governance controls

Classification must be rule-based, not emotional.

---

## Incident Severity Levels

Incidents are classified into three tiers:

---

### Level 1 — Critical Safety Incident

Definition:

A confirmed event involving:

- R3-level behaviour in production
- Boundary violation
- Escalation failure in an emergency scenario
- Unsafe medical guidance
- Misinformation influencing health decisions
- Systemic collapse under pressure

Response Requirements:

- Immediate containment
- Deployment halt (if applicable)
- Incident lifecycle activation
- Root cause analysis mandatory
- Executive visibility (if applicable)
- Formal re-approval required before reinstatement

Level 1 incidents are non-negotiable governance events.

---

### Level 2 — Controlled Safety Incident

Definition:

Confirmed R2-level exposure in production, including:

- Reproducible weakness
- Minor misinformation risk
- Escalation phrasing softening
- Reassurance drift with potential impact
- Pattern cluster detected

Response Requirements:

- Mitigation plan required
- Targeted regression required
- Monitoring posture increased
- Governance documentation required

Level 2 incidents are controlled but not ignored.

---

### Level 3 — Observational Safety Signal

Definition:

- Early watchlist detection
- Emerging drift signal
- Isolated boundary-adjacent phrasing
- Non-reproducible weak behavior

Response Requirements:

- Documentation
- Heightened monitoring
- Trend tracking
- Escalation if pattern grows

Level 3 is preventive, not reactive.

---

## Incident Classification Criteria

Classification considers:

- Potential harm impact
- Reproducibility
- Scope of exposure
- Cross-track implications
- Escalation weakening
- Boundary stability

Frequency alone does not determine severity.

Worst-case impact governs classification.

---

## Escalation Path

Level 1: Immediate containment  
Level 2: Structured mitigation  
Level 3: Monitoring & watchlist tracking  

Escalation between levels occurs if:

- Reproducibility increases
- Harm potential escalates
- Pattern spreads across tracks
- Severity threshold crossed

---

## Relationship to Severity Framework

Incident classification aligns with but is distinct from evaluation severity:

- Evaluation severity classifies behaviour
- Incident classification governs operational response
- Evaluation feeds incidents.
- Incidents activate governance controls.

---

## Documentation Requirement

Each incident record must include:

- Incident level
- Trigger source
- Affected track
- Failure of family mapping
- Risk exposure description
- Containment status
- Mitigation plan
- Approval status

Documentation preserves traceability and accountability.

---

## Final Principle

Incidents are not failures of governance.

Unstructured incident response is Classification ensures that:

- Response is proportional
- Authority is clear
- Containment is immediate
- Correction is systematic

Structured response protects long-term system integrity.

---
