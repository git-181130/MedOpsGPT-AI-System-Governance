# Clinical Factuality & Medical Accuracy Evaluation

## EvalOps Track — Medical GPT-Based Chatbot (MedOpsGPT)

---

## Overview

This evaluation track assesses whether **MedOpsGPT** provides factually correct medical information while remaining non-diagnostic and appropriately scoped.

In medical AI systems, safety failures do not only occur when models hallucinate or escalate incorrectly.

They also occur when models provide **plausible but wrong medical information**.

This evaluation exists to ensure MedOpsGPT:

* Communicates accurate, current medical facts
* Correctly describes symptoms, warning signs, and general medical concepts
* Avoids outdated, misleading, or incorrect information
* Maintains accuracy under follow-up pressure
* Preserves correctness even when simplifying complex topics
* Does not use incorrect facts to reassure or minimize risk

This track governs **medical correctness**, not refusal behaviour, emergency escalation, or clinical reasoning structure.

---

## Why This Evaluation Exists

Large language models are optimized for:

* Fluency
* Simplicity
* Conversational clarity

In medical contexts, those strengths can create risk when:

* Nuance is oversimplified
* Edge cases are flattened
* Outdated rules of thumb are repeated
* Incorrect comparisons feel intuitively “right”

In healthcare, wrong information delivered calmly is still unsafe.

This evaluation enforces a clear standard:

> **Medical information must be correct, even when it is high-level and non-diagnostic.**

---

## Core Safety Question

> **Is the medical information provided factually correct, current, and appropriately scoped?**

A response that avoids diagnosis but contains incorrect facts is considered unsafe.

---

## What This Evaluation Covers

This track evaluates MedOpsGPT behaviour across:

* General medical education
* Symptom and warning-sign descriptions
* High-level distinctions between benign and serious patterns
* Risk factors and red flags
* Clarification of common misconceptions
* Follow-up questions seeking elaboration
* Cross-prompt factual consistency
* Interactions between factual accuracy and reassurance

The focus is **accuracy and correctness**, not triage or diagnosis.

---

## What This Evaluation Does Not Cover

This track does **not** evaluate:

* Whether the model should refuse (Safety Boundary & Refusal)
* Emergency escalation correctness (Disclaimer & Escalation)
* Hallucination of fabricated information (Medical Hallucination)
* Clinical reasoning structure or differential diagnosis

Passing other tracks does **not** imply factual correctness.

---

## Evaluation Philosophy

This evaluation is governed by four non-negotiable principles:

### 1. Correctness Is a Safety Requirement

Medical accuracy is not a quality preference — it is a safety constraint.

### 2. Simplicity Must Preserve Truth

Simplified explanations must remain medically correct.

### 3. Variability Matters

Symptoms and presentations vary; absolutes are unsafe.

### 4. Accuracy Overrides Reassurance

Incorrect facts must never be used to calm or reassure users.

---

## How This Evaluation Is Used

Results from this track are used to:

* Detect misinformation risk early
* Block releases with unsafe factual errors
* Guide mitigation and regression testing
* Provide audit-grade evidence of medical accuracy governance
* Demonstrate senior-level ownership of medical correctness

This evaluation is **release-gating by design**.

---

## Documents in This Evaluation

This evaluation track includes the following public governance documents:

* `evaluation-charter.md` — authority, scope, and rules
* `category-plan.md` — factual risk surfaces
* `minimum-expected-outputs.md` — accuracy safety floor
* `failure-pattern-mapping.md` — factual failure families
* `scoring-interpretation.md` — severity application
* `evalSummary.md` — sanitized evaluation outcome and decision

Detailed execution logs, fact-checks, incidents, and mitigations are maintained as confidential internal artifacts.

---

## Final Principle

> Medical AI must not only sound reasonable — it must be correct.
> Incorrect information, even when cautious, is unsafe.

This evaluation ensures MedOpsGPT earns trust through medical accuracy and factual integrity.


