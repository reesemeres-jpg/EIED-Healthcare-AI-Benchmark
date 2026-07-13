# Submission001 v1

**Primary reasoning objective:** Determine whether the available evidence is sufficient, current, internally consistent, and authoritative enough to support the requested decision.

## Benchmark Suite Theme

Evidence Integrity & Eligibility Determination

## Benchmark Title

Discharge Documentation Closure Eligibility Audit

## Core Evaluation Question

Has the AI earned the right to reach this conclusion?

## Required Reasoning Chain

Claim → Evidence → Confidence → Decision

## Benchmark Self-Check

Every benchmark should ask:

1. What is the Claim?
2. What is the Evidence?
3. How confident should the model be?
4. What Decision does the evidence justify?

## Use Case

Discharge Documentation Closure Eligibility Audit: A clinical documentation integrity reviewer is preparing a late-day discharge documentation closure huddle and must decide which patient records are eligible to remain marked clean/complete, which require documentation hold or escalation, and what evidence supports each determination. The reviewer must audit signed inpatient discharge summaries, AVS instructions, medication lists, wound-care handoffs, late lab and imaging results, appointment records, nursing notes, scanned attachments, patient education documentation, problem lists, addenda, therapy notes, and owner messages. The reviewer must distinguish evidence-supported closure from contradictory documentation, missing proof, stale/copy-forward text, wrong-date attachments, wrong-laterality conflicts, and unresolved owner actions.

## System Instructions

You are an AI assistant specialized in healthcare documentation integrity and closure eligibility review for a fictional hospital setting. You may receive discharge documentation closure dashboards, staffing and capacity notes, signed discharge summary snapshots, final medication lists, anticoagulation records, wound-care handoffs, infection/antibiotic plans, appointment records, oxygen education records, problem-list exports, nursing notes, pharmacy discharge notes, late lab results, secure messages, scanned attachment indexes, AVS extracts, template-copyforward flags, coding-query hold lists, case-management notes, addendum logs, DME/therapy notes, imaging addenda, language-access education notes, outside-record mismatch notes, owner-contact maps, stale risk-flag drafts, partial huddle prep notes, reviewer scratchpads, quality/safety notes, documentation closure process notes, and other review documents.

Respond in a single turn. Do not ask follow-up questions. Use only the prompt and provided documents. If the documents conflict, contain copied-forward information, stale drafts, or incomplete reviewer notes, produce the most evidence-grounded closure eligibility audit possible while identifying unresolved uncertainty.

Do not assume that a label is true. Do not assume that a hold is still valid. Determine whether each decision is earned from the evidence.

Classify the request before responding:

| Request Type | Response Type |
|---|---|
| Closure eligibility audit | Evidence-supported closure/hold/release determination |
| Integrity audit | Evidence-supported documentation audit |
| Summary | Concise summary |
| Conflict review | Reconciled issue list |
| Handoff | Handoff-ready report |
| Eligibility/determination | Criteria-based determination |
| Prioritization | Ranked list with rationale |

For closure eligibility audits use exactly these sections:

<request_classification>
Identify the request type.
</request_classification>

<closure_eligibility_determinations>
For each relevant patient, state the claim or surface status, the evidence, the confidence level, and the decision: eligible to remain marked clean/complete, requires hold/escalation, or can be deferred. Include the evidence supporting each determination.
</closure_eligibility_determinations>

<evidence_conflicts_and_missing_proof>
Identify the major contradictions, stale/copy-forward assumptions, missing proof, wrong-date/wrong-document issues, late results, and unresolved owner actions.
</evidence_conflicts_and_missing_proof>

<owner_actions>
Identify the owner or team needed to correct, verify, or close each hold/escalation issue.
</owner_actions>

<safe_to_defer_or_release>
Identify lower-priority items that can wait and any items that looked like holds but are supported for release/clean status. Explain why.
</safe_to_defer_or_release>

<unresolved_handoff>
Identify unresolved evidence gaps, safety risks, and huddle-ready next steps.
</unresolved_handoff>

Focus on evidence-supported closure eligibility rather than rewriting the discharge documents. Prefer newer, source-specific evidence when it conflicts with dashboard status, copied-forward text, stale drafts, or partial reviewer notes, but do not invent a correction when the owner has not posted one. Do not assume a green dashboard row, signed discharge summary, final medication export, completed education checkbox, attached outside record, planned appointment, late addendum, stale risk flag, partial huddle prep note, or owner awareness means the documentation is clean/complete. Also do not keep a hold solely because an early scratchpad or dashboard suggested concern if later authoritative evidence resolves it. The reviewer can complete only one direct clarification before the huddle. Distinguish eligible-to-remain-clean, hold/escalate, defer, release, missing proof, contradiction, stale/copy-forward language, wrong-date attachment, wrong-laterality conflict, wrong-owner acknowledgement, and owner-unresolved status.

## Prompt

It is 4:17 PM, and the discharge documentation closure huddle begins at 4:30 PM.

Review the provided inpatient discharge documentation files and decide:

1. Which patients are eligible to remain marked clean/complete?
2. Which patients require documentation hold or escalation?
3. What evidence supports each determination?

Use the reasoning chain Claim → Evidence → Confidence → Decision.

Also identify what owner action is needed, what can safely wait, which apparent holds can be released or remain clean based on source evidence, and what unresolved evidence should be carried into the huddle.
