# Safety Boundary & Refusal Evaluation

## EvalOps Track — Medical GPT-Based Chatbot (MedOpsGPT)

---

## Overview

This evaluation track assesses whether **MedOpsGPT** consistently enforces medical safety boundaries and refuses unsafe requests correctly, even under pressure, ambiguity, or emotional manipulation.

In medical-adjacent AI systems, some of the highest-impact failures occur not because the model lacks knowledge, but because it answers questions it should not answer.

This evaluation exists to ensure that MedOpsGPT:

* Does not cross into clinical decision-making
* Maintains strict refusal behaviour where required
* Escalates appropriately in emergency contexts
* Preserves boundary integrity across repeated or adversarial prompting

---

## Why This Evaluation Exists

Medical AI systems face a structural tension:

* Users want certainty, reassurance, and answers
* Safety requires restraint, refusal, and escalation

Without explicit governance, models tend to:

* Provide “helpful” partial answers after disclaimers
* Collapse refusals under pressure or repetition
* Offer reassurance that delays appropriate care
* Treat disclaimers as permission to proceed

This evaluation treats **boundary enforcement itself as a safety-critical behaviour**, not a UX concern.

---

## Core Safety Question

> **Should the model answer this at all — and if not, does it refuse correctly?**

A refusal that is:

* Clear
* Closed
* Respectful
* Properly redirected

is considered a successful outcome.

---

## Scope of This Track

This evaluation applies to medical-adjacent requests involving:

* Diagnosis or condition identification
* Medication recommendations or dosage guidance
* Emergency decision-making or triage
* Treatment plans or medical judgment
* Requests framed emotionally, authoritatively, or persistently

The track evaluates **what the model must not do**, regardless of:

* Factual correctness
* Confidence or fluency
* User intent or disclaimers

---

## What This Evaluation Is Not

This track does **not** evaluate:

* Medical factual accuracy in isolation
* Hallucination risk unrelated to boundaries
* Quality of clinical reasoning where answering is allowed

Those risks are handled by separate evaluation tracks with independent stop rules.

Passing this track does **not** imply passing others.

---

## Evaluation Philosophy

This evaluation is governed by three non-negotiable principles:

### 1. Refusal Is Success

A correct refusal is a positive outcome, not a failure.

### 2. Boundaries Are Binary

Either the model crossed the line, or it did not.
Tone, disclaimers, and partial compliance do not soften violations.

### 3. Safety Overrides Helpfulness

When helpfulness conflicts with safety boundaries, safety wins.

---

## How This Evaluation Is Used

Results from this track are used to:

* Gate releases and block unsafe configurations
* Detect systemic boundary erosion patterns
* Inform mitigation and regression priorities
* Provide audit-grade evidence of boundary governance

This evaluation is **release-blocking by design**.

---

## Public vs Private Artifacts

This repository contains framework-level documentation only, including:

* Evaluation intent and scope
* Category definitions
* Minimum expected behaviours
* Failure pattern mappings
* Scoring interpretations
* Sanitized evaluation summaries

Detailed execution records, prompts, incidents, and mitigations are maintained as confidential internal artifacts due to their sensitivity.

---

## Documents in This Evaluation

* evaluation-charter — authority, scope, and stop rules
* category-plan — boundary failure surfaces evaluated
* minimum-expected-outputs — non-negotiable refusal baselines
* failure-pattern-mapping — how global failures manifest here
* scoring-interpretation — how severity is applied in this track
* evalSummary — public, sanitized evaluation outcome

---

## Final Principle

> In medical AI, the most dangerous answer is the one that feels helpful but crosses a boundary.

This evaluation exists to ensure MedOpsGPT never confuses helpfulness with authority.

