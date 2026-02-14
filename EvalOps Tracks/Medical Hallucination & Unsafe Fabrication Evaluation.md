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

Passing other safety tracks does **not** imply passing the hallucination evaluation.

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

* ## [Evaluation Charter](https://drive.google.com/file/d/1oX1QFEYzf3I22f4PjRUgvIgXIxlY04CZ/view?usp=drive_link) — authority, scope, and rules
* ## [Category Plan](https://drive.google.com/file/d/14Iqq9v9p4rPlYoFq5PFhFh0IqEPjjtEE/view?usp=drive_link) — hallucination failure surfaces
* ## [Minimum Expected Outputs](https://drive.google.com/file/d/1Lrv_KjP64dExBymgWMzTk-yMO3UyFfG1/view?usp=drive_link) — epistemic safety floor
* ## [Failure Pattern Mapping](https://drive.google.com/file/d/1GODjzTBphfPAy_PZ9jgb4jvLoiNV0fo5/view?usp=drive_link) — hallucination failure families
* ## [Scoring Interpretation](https://drive.google.com/file/d/13i2Zd8Jw8gg6UgxoQjs3yDVjNbhB9DEa/view?usp=drive_link) — severity application
* ## [Evaluation Summary](https://drive.google.com/file/d/1r1TZhWfhXGLw9LZ51Ape53C9YHg01pn2/view?usp=drive_link) — sanitized evaluation outcome and decision

Execution logs, fact checks, incidents, and mitigations are maintained as confidential internal artifacts.

---

## Final Principle

> In medical AI, sounding right is not enough.
> The system must be right or clearly say it does not know.

This evaluation exists to ensure MedOpsGPT earns trust through honest uncertainty and factual integrity.

