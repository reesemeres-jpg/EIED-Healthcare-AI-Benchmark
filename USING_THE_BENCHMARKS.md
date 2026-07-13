# Using the EIED Benchmark Suite

## Purpose

EIED is designed to evaluate whether an AI system can determine when available evidence is sufficient, current, internally consistent, patient-specific, and authoritative enough to support a healthcare decision.

The suite is organized around the chain:

> **Claim → Evidence → Confidence → Decision**

## Downloading a Benchmark

Each benchmark is available as an individually named ZIP archive in the repository root.

1. Select the benchmark ZIP from the repository or the benchmark index in `README.md`.
2. Download and extract the archive.
3. Begin with the benchmark-level `README.md`.
4. Review the system/task prompt, source documents, grading rubric, and design notes.

## Typical Evaluation Workflow

A benchmark package can be used to:

- present the included system/task prompt and source records to an AI model;
- collect the model's final response;
- score that response against the strict grading rubric;
- analyze evidence use, justification boundaries, confidence calibration, and unsupported assumptions; and
- compare performance across repeated runs, models, or prompting conditions.

## Interpretation

EIED does not reward caution alone. It penalizes both unsupported action and unsupported withholding.

A strong response should distinguish:

- evidence from labels or assumptions;
- authoritative records from stale, preliminary, or lower-trust sources;
- decision-blocking gaps from non-blocking uncertainty; and
- what is documented from what is merely plausible.

## Scope and Safety

All patients, organizations, records, and scenarios are fictional. The suite is intended for AI evaluation, research, and portfolio demonstration. It is not clinical guidance, a validated regulatory instrument, or a substitute for professional review.
