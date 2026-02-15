# New Risk Surface Onboarding  
## Structured Integration of Additional Evaluation Domains  

---

## Purpose

This document defines how new risk surfaces, domains, or evaluation tracks are formally integrated into the EvalOps architecture.
As system scope expands, new harm pathways may emerge.
New risk surfaces must be:

- Justified
- Structured
- Non-overlapping
- Integrated into existing governance
- Version-controlled

Unstructured expansion creates fragmentation.

---

## Core Principle

- New risk surfaces are added to strengthen coverage — not to duplicate existing controls.
- Each new surface must represent a distinct pathway to user harm.
- Overlap weakens clarity.

---

## Trigger Conditions for New Risk Surface Review

New surface onboarding may be initiated when:

1. Postmortem reveals recurring failure not captured by existing tracks  
2. Domain scope expands (e.g., new medical categories)  
3. Monitoring reveals systematic exposure outside current coverage  
4. Regulatory expectations introduce a new risk dimension  
5. Cross-track instability indicates a missing structural boundary  

Isolated anomalies do not justify new track creation.

---

## Onboarding Evaluation Criteria

Before adding a new risk surface, assess:

- Does it represent a distinct harm pathway?
- Can it be governed within an existing track?
- Does it introduce cross-track complexity?
- Does it require new minimum expected outputs?
- Does it require new severity mapping logic?

If existing tracks can govern it, refinement may be preferable to expansion.

---

## Onboarding Process

Formal onboarding requires:

1. Written proposal describing the new risk surface
2. Harm pathway analysis
3. Mapping to global failure taxonomy
4. Definition of minimum expected outputs
5. Category plan creation
6. Scoring interpretation model definition
7. Cross-track interaction assessment
8. Monitoring alignment
9. Governance authority approval
10. Version increment documentation

All steps must be completed before deployment under the new scope.

---

## Structural Integration Requirements

New risk surface must:

- Align with Global Severity Framework
- Integrate into the Risk Management layer
- Connect to Approval & Release Governance
- Integrate into the Monitoring model
- Be included in Incident Response protocols
- Be covered by RCA and Postmortem processes

No risk surface may exist outside the governance lifecycle.

---

## Monitoring & Escalation Alignment

Upon onboarding:

- Monitoring watchlists must update
- Regression triggers must include the new track
- Escalation protocol must recognize new domain
- Incident classification must include the new surface

Integration must be lifecycle-complete.

---

## Documentation Requirements

New risk surface documentation must include:

- Justification statement
- Governance impact assessment
- Cross-layer integration summary
- Version reference
- Effective date

Traceability preserves clarity.

---

## Governance Integrity Rule

Expansion must not:

- Dilute severity enforcement
- Duplicate risk coverage unnecessarily
- Introduce overlapping classification ambiguity
- Create governance fragmentation

Controlled expansion strengthens architecture.

---

## Final Principle

- A mature governance system must scale without losing structural clarity.
- New risk surfaces are not additions. They are integrations.
- Integration must preserve coherence, discipline, and enforcement integrity.
- Evolution without structure creates complexity.
- Structured onboarding creates resilience.

---
