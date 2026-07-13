# EIED Suite Overview

## Full Title

**Evidence Integrity & Eligibility Determination**

## Subtitle

*A Healthcare AI Benchmark Suite for Evidence Validation, Documentation Integrity, and Eligibility Reasoning*

## Central Thesis

Trust must be earned from the evidence—not inferred from labels, signatures, dashboards, reviewer notes, repeated documentation, or workflow assumptions.

An AI response can be clinically plausible and operationally polished while still being unsupported. EIED evaluates whether the model can identify the actual claim, reconcile the complete evidence set, calibrate confidence, and choose only the decision the evidence justifies.

## Core Evaluation Question

> **Has the AI earned the right to reach this conclusion?**

## Recognizable Suite Identity

> **Claim → Evidence → Confidence → Decision**

## What EIED Measures

EIED measures whether a model can:

- distinguish administrative status from evidentiary status;
- reconcile contradictions across multiple documents and across longitudinal care settings;
- identify stale, copied-forward, wrong-patient, wrong-date, wrong-context, and non-applicable evidence;
- apply criteria, time windows, guideline populations, exclusions, and safety gates precisely;
- prefer current, patient-specific, authoritative evidence over helper documents and labels;
- distinguish repeated claims from independent confirmation;
- identify missing proof without inventing facts;
- release apparent holds when later evidence resolves them;
- make proportionate decisions and communicate owner actions clearly.

## Why the Counterbalance Matters

A benchmark that makes every green row unsafe can be beaten by escalating everything. EIED deliberately includes cases where evidence appears incomplete or dashboards and scratchpads say hold, but full source review supports release, finalization, inclusion, application, or closure.

This balanced design tests whether the model can earn both its caution and its confidence.

## Portfolio Scope

Version 1.0 contains twelve original benchmarks and 360 fictional healthcare source documents across care transitions, payer operations, clinical research, population health, utilization management, quality measurement, medication safety, case resolution, coding integrity, longitudinal evidence reconciliation, and clinical guideline applicability.
