# Threshold Adjustment Governance  
## Structured Control of Severity and Enforcement Thresholds  

---

## Purpose

This document defines how severity thresholds, escalation criteria, and monitoring sensitivity levels may be adjusted over time.

Thresholds determine:

- When a failure becomes R2 or R3
- When monitoring escalates to re-evaluation
- When incidents are classified at higher levels
- When release is halted

Threshold changes directly impact safety posture.

Therefore, adjustments must be deliberate, justified, and governed.

---

## Core Principle

- Thresholds may be strengthened to improve safety.
- Thresholds must not be relaxed without structured justification and governance review.
- Lowering safety thresholds for convenience undermines integrity.

---

## Types of Thresholds Governed

This policy applies to:

- Severity classification thresholds (PASS / R2 / R3)
- Escalation trigger definitions
- Monitoring sensitivity triggers
- Drift detection thresholds
- Incident classification criteria
- Regression trigger rules

All enforcement boundaries are threshold-controlled.

---

## Valid Reasons for Threshold Adjustment

Threshold adjustments may be considered when:

1. Postmortem reveals under-classification of risk  
2. Repeated near-miss incidents occur  
3. Monitoring fails to detect drift early enough  
4. Regulatory expectations evolve  
5. Domain expansion introduces a higher-risk context  
6. Empirical review shows classification inconsistency  

Adjustment must be evidence-based.

---

## Prohibited Reasons for Threshold Adjustment

Thresholds must not be adjusted due to:

- Business pressure
- Deployment delays
- Stakeholder discomfort
- Desire to reduce reported incident count
- Model performance incentives

Safety thresholds exist to protect users — not metrics.

---

## Adjustment Process

All threshold modifications must follow:

1. Documentation of triggering condition
2. Data-supported justification
3. Cross-track impact assessment
4. Governance authority approval
5. Version increment
6. Effective date recording
7. Monitoring adjustment alignment

Threshold changes must not occur mid-evaluation cycle.

---

## Impact Assessment Requirements

Before implementing the adjustment, assess:

- Cross-track classification impact
- Historical incident reclassification implications
- Monitoring false positive/negative balance
- Escalation protocol alignment
- Release decision matrix stability

Threshold changes affect the entire governance system.

---

## Strengthening vs Relaxation

Strengthening thresholds (more protective):

- May increase R2/R3 classification frequency
- May increase monitoring sensitivity
- Must be documented but encouraged when justified

Relaxing thresholds (less protective):

- Requires heightened justification
- Requires retrospective analysis
- Requires executive governance approval (if applicable)
- Must include risk exposure impact statement

Relaxation carries a higher governance burden.

---

## Documentation Requirements

Each threshold adjustment must record:

- Previous threshold definition
- New threshold definition
- Rationale for change
- Affected governance layer(s)
- Version reference
- Approval authority confirmation

Traceability preserves credibility.

---

## Governance Integrity Rule

Threshold integrity defines enforcement credibility. Frequent or unexplained adjustments erode trust.
Threshold governance ensures that:

- Enforcement remains principled
- Severity remains meaningful
- Escalation remains proportional
- Release gating remains defensible

---

## Final Principle

- Thresholds define where safety boundaries are drawn.
- Adjusting them reshapes risk posture.
- Such changes must reflect increased clarity or protection, never convenience.
- Disciplined threshold governance protects long-term integrity.

---
