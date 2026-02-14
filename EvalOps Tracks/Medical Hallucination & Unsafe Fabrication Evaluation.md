# Medical Hallucination & Unsafe Fabrication Evaluation

## EvalOps Track — Medical GPT-Based Chatbot (MedOpsGPT)

---

## Overview

This evaluation track assesses whether **MedOpsGPT** maintains epistemic integrity when providing medical information.

In medical AI systems, one of the most dangerous failure modes is not refusal or escalation failure, it is **confidently presenting false or fabricated information as truth**.

This evaluation exists to ensure MedOpsGPT:

* Does not invent medical facts, causes, or mechanisms
* Does not fabricate statistics, probabilities, or certainty
* Handles uncertainty honestly and explicitly
* Avoids confident speculation under pressure
* Maintains factual consistency across prompts
* Prevents hallucination-driven reassurance or delay-of-care

This track governs **truthfulness**, not politeness or completeness.

---

## Why This Evaluation Exists

Large language models are optimized to:

* Sound fluent
* Be helpful
* Fill gaps in conversation

In medical contexts, these tendencies can lead to:

* Invented explanations
* False precision
* Overconfident but incorrect statements
* Plausible-sounding speculation

In healthcare, plausible but false is more dangerous than incomplete but honest.

This evaluation enforces a strict rule:

> **If the model does not know, it must say so.**

---

## Core Safety Question

> **Is the information provided truthful, supported, and appropriately uncertain, or is it fabricated or overstated?**

A response that explicitly acknowledges uncertainty is considered safer than a confident answer without evidence.

---

## What This Evaluation Covers

This track evaluates MedOpsGPT behaviour across:

* Medical education and symptom explanation
* Ambiguous or under-specified medical queries
* Follow-up pressure seeking certainty
* Requests for probabilities, rankings, or comparisons
* Mechanistic or causal explanations
* Cross-prompt factual consistency
* Interaction between hallucination and reassurance
* Combined edge cases involving other safety tracks

The focus is on **epistemic discipline**, not clinical diagnosis.

---

## What This Evaluation Does Not Cover

This track does **not** evaluate:

* Whether the model should refuse (Safety Boundary & Refusal)
* Emergency escalation correctness (Disclaimer & Escalation)
* Clinical reasoning structure (Clinical Reasoning & Differential Safety)

Passing other safety tracks does **not** imply passing hallucination evaluation.

---

## Evaluation Philosophy

This evaluation is governed by four non-negotiable principles:

### 1. Uncertainty Is a Safety Feature

Saying “I don’t know” is preferable to guessing.

### 2. Confidence Must Match Evidence

Authoritative tone does not justify unsupported claims.

### 3. Precision Implies Authority

Numbers, rankings, and mechanisms require strong justification.

### 4. Truth Overrides Helpfulness

Completeness is secondary to correctness.

---

## How This Evaluation Is Used

Results from this track are used to:

* Detect hallucination-driven safety risk
* Block releases with unsafe fabrication behaviour
* Guide mitigation and regression testing
* Provide audit-grade evidence of epistemic governance
* Signal senior-level safety ownership and rigor

This evaluation is **release-gating by design**.

---

## Documents in This Evaluation

This evaluation track includes the following public governance documents:

* evaluation-charter — authority, scope, and rules
* category-plan — hallucination failure surfaces
* minimum-expected-outputs — epistemic safety floor
* failure-pattern-mapping — hallucination failure families
* scoring-interpretation — severity application
* evalSummary — sanitized evaluation outcome and decision

Execution logs, fact checks, incidents, and mitigations are maintained as confidential internal artifacts.

---

## Final Principle

> In medical AI, sounding right is not enough.
> The system must be right or clearly say it does not know.

This evaluation exists to ensure MedOpsGPT earns trust through honest uncertainty and factual integrity.

