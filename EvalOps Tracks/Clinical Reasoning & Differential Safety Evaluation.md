# Clinical Reasoning & Differential Safety Evaluation

## EvalOps Track — Medical GPT-Based Chatbot (MedOpsGPT)

---

## Overview

This evaluation track assesses whether a medical GPT-based system reasons safely under uncertainty, rather than merely producing fluent or factually correct responses.

In medical contexts, harm often arises not from incorrect facts, but from **how reasoning is framed** — particularly when benign explanations, reassurance, or confidence prematurely suppress consideration of dangerous conditions.

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

## Scope of This Track

This evaluation applies to:

* Medical reasoning scenarios involving ambiguous or incomplete information
* Chest-related symptoms and other domains where delayed escalation can cause harm
* Diagnosis-seeking, reassurance-seeking, and explanation-seeking prompts
* Single-turn and multi-turn interactions, including pressure for reassurance

It evaluates **how the model reasons**, not whether it diagnoses correctly.

---

## Core Safety Question

> **Does the model reason conservatively, transparently, and stably when medical risk is uncertain?**

A response is considered safe only if it:

* Preserves diagnostic openness
* Surfaces potentially dangerous possibilities
* Separates severity from probability
* Handles uncertainty explicitly
* Resists reassurance-driven drift

User comfort or fluency must **never override safety posture**.

---

## What This Evaluation Is Not

This track does **not** evaluate:

* Medical factual correctness in isolation
* Emergency escalation phrasing alone
* Disclaimer compliance
* Refusal or jailbreak resistance

Those risks are handled in separate evaluation tracks with independent stop rules.

Passing this track does **not** imply passing other safety evaluations.

---

## Evaluation Structure

The evaluation is executed across multiple reasoning categories, each isolating a distinct failure surface, such as:

* Differential diagnosis completeness
* Inclusion of high-risk conditions
* Risk prioritization and ordering
* Reasoning transparency
* Uncertainty handling and confidence calibration
* Stability under reassurance-seeking pressure
* Consistency across equivalent clinical scenarios

Each category operates with independent severity thresholds and stop rules.

---

## Severity & Release Philosophy

This evaluation uses a severity-based gating model:

* Decisions are driven by **worst-case impact**, not averages
* A single critical reasoning failure can block release
* Tone quality, empathy, or partial correctness do not mitigate unsafe reasoning

The system is never declared “safe” in absolute terms.

It may only be declared **safe enough to ship under defined controls**, with known residual risk.

---

## Public vs Private Artifacts

This repository intentionally contains only framework-level documentation, including:

* Evaluation intent and scope
* Reasoning expectations
* Category definitions
* Severity logic

Detailed execution records, incidents, root cause analyses, mitigations, and regression evidence are maintained as confidential internal artifacts, as they expose model failure modes and safety controls.

This separation reflects standard practice in safety-critical AI systems.

---

## How to Read This Evaluation

If you are:

* A founder or product leader — read this to understand how reasoning risk is governed
* An evaluator or reviewer — use the category plan and minimum expectations
* An AI practitioner — treat this as a reference for conservative medical reasoning design

This evaluation is designed to be **auditable, explainable, and defensible under scrutiny**.

---

## Key Principle (Non-Negotiable)

> When reasoning safety conflicts with reassurance or fluency, safety wins.

---

## Documents in This Evaluation

* evaluation-charter — authority, scope, and escalation rules
* category-plan — emergency escalation failure surfaces
* minimum-expected-outputs — non-negotiable escalation baseline
* failure-pattern-mapping — how escalation failures manifest
* scoring-interpretation — how severity is applied in this track
* evalSummary — sanitized evaluation outcome and decision

---

## Final Note

Clinical reasoning failures are often subtle, plausible, and well-intentioned — which is precisely why they are dangerous.

This evaluation exists to make those failures visible, classifiable, and blockable before they reach users.

