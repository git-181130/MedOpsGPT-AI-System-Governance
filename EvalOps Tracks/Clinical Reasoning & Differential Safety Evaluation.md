
# Clinical Reasoning & Differential Safety Evaluation

## EvalOps Track — Medical GPT-Based Chatbot (MedOpsGPT)

---

## Overview

This evaluation track assesses whether MedOpsGPT reasons safely under uncertainty, rather than merely producing fluent or factually correct responses.

In medical contexts, harm often arises not from incorrect facts, but from **how reasoning is framed **, particularly when benign explanations, reassurance, or confidence prematurely suppress consideration of dangerous conditions.

This track exists to ensure that the model’s reasoning process itself does not introduce risk, especially in ambiguous or high-stakes symptom scenarios.

---

## Why This Evaluation Exists

Traditional model evaluation focuses on:

* Accuracy
* Hallucination rates
* Tone and helpfulness

These metrics are insufficient for medical-adjacent systems.

Clinical risk frequently emerges when a model:

* Narrows the diagnostic space too early
* Prioritizes likelihood over severity
* Reassures before acknowledging danger
* Allows conversational pressure to erode caution
* Communicates confidence disproportionate to evidence

This evaluation treats **reasoning behaviour as a safety surface**, not a stylistic preference.

---

## Core Safety Question

> **Does the model reason conservatively, transparently, and stably when medical risk is uncertain?**

A response is considered safe only if it:

* Preserves diagnostic openness
* Surfaces potentially dangerous possibilities
* Separates severity from probability
* Handles uncertainty explicitly
* Resists reassurance-driven drift

User comfort or fluency must never override safety posture.

---

## What This Evaluation Covers

This track evaluates MedOpsGPT behaviour across:

* Medical reasoning scenarios involving ambiguous or incomplete information
* Chest-related symptoms and other domains where delayed escalation can cause harm
* Diagnosis-seeking, reassurance-seeking, and explanation-seeking prompts
* Single-turn and multi-turn interactions, including pressure for reassurance
* Differential diagnosis completeness
* Inclusion of high-risk conditions
* Risk prioritization and ordering
* Reasoning transparency and confidence calibration
* Consistency across equivalent clinical scenarios

The focus is on **reasoning integrity**, not diagnostic correctness.

---

## What This Evaluation Does Not Cover

This track does **not** evaluate:

* Medical factual correctness in isolation
* Emergency escalation phrasing alone
* Disclaimer compliance
* Refusal or jailbreak resistance

Those risks are handled in separate evaluation tracks with independent stop rules.

Passing this track does **not** imply passing other safety evaluations.

---

## Evaluation Philosophy

This evaluation is governed by four non-negotiable principles:

### 1. Diagnostic Openness Is Required

Premature narrowing of possibilities is unsafe.

### 2. Severity Overrides Likelihood

Low probability does not justify ignoring high-impact conditions.

### 3. Uncertainty Must Be Explicit

Confidence must match available evidence.

### 4. Safety Overrides Reassurance

When reasoning, safety conflicts with fluency or comfort, safety wins.

---

## How This Evaluation Is Used

Results from this track are used to:

* Detect reasoning-driven safety risk
* Block releases with unsafe reasoning behaviour
* Guide mitigation and regression testing
* Provide audit-grade evidence of clinical reasoning governance
* Demonstrate senior-level ownership of reasoning safety

This evaluation is **release-gating by design**.

---

## Documents in This Evaluation

* ## [Evaluation Charter](https://drive.google.com/file/d/16ycvMtK6tYJakjCHLZIx1ehBF1aqV73B/view?usp=drive_link)  — authority, scope, and stop rules
* ## [Category Plan](https://drive.google.com/file/d/1U55Xzw8JWTWcpQqH0w7yx2roJ3eAUsKt/view?usp=drive_link) — reasoning failure surfaces evaluated
* ## [Minimum Expected Outputs](https://drive.google.com/file/d/1zAaM9KaIJhBFvmsD55pfI2G_abKjaaex/view?usp=drive_link) — non-negotiable reasoning baselines
* ## [Failure Pattern Mapping](https://drive.google.com/file/d/1osFlgaqUGH6g3p2VRETJS1w8rAzCOBRP/view?usp=drive_link) — how reasoning failures manifest
* ## [Scoring Interpretation](https://drive.google.com/file/d/1U_G1XPF64CBrA4-7nboNPwGcsa3uZ5bf/view?usp=drive_link) — how severity is applied in this track
* ## [Evaluation Summary](https://drive.google.com/file/d/1-70NK-difBjKAmqUui6LJBOdTyLPc_ar/view?usp=drive_link) — sanitized evaluation outcome and decision

Detailed execution records, incidents, root cause analyses, mitigations, and regression evidence are maintained as confidential internal artifacts.

---

## Final Principle

> Clinical reasoning failures are often subtle, plausible, and well-intentioned, which is precisely why they are dangerous.

This evaluation exists to make those failures visible, classifiable, and blockable before they reach users.

