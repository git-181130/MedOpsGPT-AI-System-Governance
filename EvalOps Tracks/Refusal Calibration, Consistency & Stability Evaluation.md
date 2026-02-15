# Refusal Calibration, Consistency & Stability Evaluation

## EvalOps Track — Medical GPT-Based Chatbot (MedOpsGPT)

---

## Overview

This evaluation track assesses whether **MedOpsGPT** refusal behaviour is calibrated, consistent, and stable across time, tone, phrasing, and user context.

In medical AI systems, safety is not achieved solely by refusing unsafe requests.

It also requires that the model:

* Refuses when it should
* Answers when it is allowed
* Behaves the same way every time for equivalent requests

This evaluation exists to ensure MedOpsGPT is predictable and trustworthy, not merely cautious.

---

## Why This Evaluation Exists

Safety boundary and escalation evaluations answer a binary question:

> Should the model answer at all?

This track answers a different, equally important question:

> Is the model refusing the right amount, in the same way, every time?

Without explicit calibration governance, models often drift into one of two failure modes:

* **Over-refusal** — blocking safe, allowed information and degrading usability
* **Under-refusal** — inconsistently leaking unsafe or boundary-adjacent guidance

Both failures erode trust.

Inconsistency amplifies risk at scale.

---

## What This Evaluation Covers

This track evaluates refusal behaviour across:

* Allowed, non-diagnostic medical education
* Boundary-adjacent requests
* Emotional, authority-based, and manipulative framing
* Rephrasing, repetition, and multi-turn conversations
* Cross-session consistency

The focus is on **calibration and reliability**, not emergency escalation dominance or diagnostic correctness.

---

## What This Evaluation Does Not Cover

This track does **not** assess:

* Whether a request should be refused at all (Safety Boundary & Refusal track)
* Emergency escalation correctness (Disclaimer & Escalation track)
* Clinical reasoning accuracy
* Medical factuality or hallucination risk (unless directly tied to refusal behaviour)

Passing other tracks does **not** imply passing this one.

---

## Core Evaluation Principles

This evaluation is governed by four non-negotiable principles:

### 1. Calibration Over Caution

Refusing everything is not safer than refusing correctly.

### 2. Consistency Over Cleverness

Equivalent prompts must yield equivalent outcomes.

### 3. Stability Over Time

Refusal behaviour must not drift across turns, tone, or repetition.

### 4. Proportionality Builds Trust

Refusal explanations must match the actual level of risk.

---

## How This Evaluation Is Used

Results from this track are used to:

* Detect refusal drift and calibration errors
* Identify phrasing- or emotion-dependent behaviour
* Gate releases when refusal reliability is compromised
* Inform mitigation and regression strategies
* Provide audit-grade evidence of refusal governance

This evaluation may block release, even if safety boundary checks pass.

---

## Documents in This Evaluation

This evaluation track includes the following public governance documents:

* ## [Evaluation Charter](https://drive.google.com/file/d/1cSsT93cWKKEBXTZNUQ3wTPcOGFnpqxci/view?usp=drive_link) — authority, scope, and decision rules
* ## [Category Plan](https://drive.google.com/file/d/1USHYddVuBl-9tiTooNPqmOE5bZQKOKaK/view?usp=drive_link) — refusal calibration and stability failure surfaces
* ## [Minimum Expected Outputs](https://drive.google.com/file/d/1r1ujKfnyEnMcBRyBXYWeGTu74gQ9jbbK/view?usp=drive_link) — non-negotiable calibration baseline
* ## [Failure Pattern Mapping](https://drive.google.com/file/d/1qD8-eaqMFY0gnytYLHDoqEO606hqR-lj/view?usp=drive_link) — how calibration failures manifest
* ## [Scoring Interpretation](https://drive.google.com/file/d/15vIyqMXlO0LO70q_zVu6MoUHNc9fE5V2/view?usp=drive_link) — how severity is applied in this track
* ## [Evaluation Summary](https://drive.google.com/file/d/1PNI3zBblLOxTX5Q2hNWZvYSbIKF3OrsA/view?usp=drive_link) — sanitized evaluation outcome and decision

Detailed prompts, execution logs, incidents, and mitigations are maintained as confidential internal artifacts.

---

## Final Principle

> A system that is safe but unpredictable is not trustworthy.

This evaluation exists to ensure MedOpsGPT refusal behaviour is not only safe, but reliable, proportional, and repeatable.

