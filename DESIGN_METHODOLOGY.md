# EIED Design Methodology

## 1. Begin With a Decision Claim

Each benchmark starts with a real healthcare status or decision that appears simple on a dashboard: clean, ready, eligible, complete, safe, compliant, resolved, supported, or applicable.

## 2. Separate the Label From the Evidence

The dashboard or summary is treated as a claim. Supporting source documents determine whether the claim is true.

## 3. Build an Object-Specific Source Hierarchy

Benchmarks include current policies, source clinical records, final addenda, specialist conclusions, outside documents, dashboards, preliminary notes, scratchpads, and stale helper files. The model must determine which source carries authority for the specific claim object.

## 4. Add Temporal, Longitudinal, and Provenance Pressure

Later evidence may reverse earlier conclusions. Repetition may create false durability without independent confirmation. Attachments may be wrong-patient, wrong-date, wrong-body-region, or incomplete. A document's presence does not establish relevance.

## 5. Validate Population Entry Before Applying a Rule

Guideline, policy, protocol, quality, coding, and authorization logic applies only after the patient-specific qualifying population, version, inclusion pathway, exclusion, and safety prerequisites are established.

## 6. Include False-Ready and False-Hold Cases

Each benchmark contains:

- cases that appear complete or eligible but are unsupported; and
- cases that appear held or incomplete but are supported by later authoritative evidence.

This prevents approval bias and escalation bias from becoming successful shortcuts.

## 7. Require a Concrete Decision

Models must move beyond summarization and make evidence-grounded determinations with confidence, owner actions, and unresolved evidence boundaries.

## 8. Grade the Reasoning, Not Just the Final Label

Rubrics assess whether the model found decisive evidence, reconciled contradictions, respected source authority and timing, calibrated confidence, and avoided invented facts.

## 9. Preserve Distinct Claims Within the Same Case

Condition, severity, cause, recovery, closure, eligibility, safety, and implementation may have different evidence and confidence. Benchmarks should not collapse them into one global status.

## 10. Preserve Realism Without Hidden Answer Keys

Source files are written as realistic healthcare artifacts. Design notes and strict grading guidelines remain evaluator materials and are not hidden inside the source-document set.

## Benchmark Construction Standard

Every EIED benchmark includes:

- use case and system instructions;
- user task prompt;
- 30 fictional source documents;
- four source-document batches;
- strict grading guidelines;
- design notes describing targeted failure modes and tempting shortcuts;
- counterbalance cases that punish blanket escalation;
- a benchmark README that states the decision boundary and suite contribution.
