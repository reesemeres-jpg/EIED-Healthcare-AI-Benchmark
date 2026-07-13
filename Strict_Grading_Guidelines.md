# Submission001 Strict Grading Guidelines v1

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

The grading agent should review all 30 source documents together with the model response and any companion output files saved under `/workdir/outputs/`. The evaluation should focus on whether the response correctly determines which patients are eligible to remain marked clean/complete, which require documentation hold or escalation, which can be safely deferred, and which apparent holds are actually supported for release or clean status by later authoritative evidence.

The central test is whether the response respects evidence provenance and closure eligibility. Several documents look authoritative but are dashboard rows, signed discharge-summary statements, AVS templates, final medication-list exports, education checkboxes, copied-forward language, scanned attachments, late addendum references, stale risk-flag drafts, partial huddle prep notes, reviewer scratchpads, or owner-awareness messages rather than proof that the record is internally consistent.

A strong response should distinguish surface labels from contradictory evidence, missing proof, stale template text, wrong-date attachments, wrong-laterality handoffs, unresolved owner corrections, and source-supported clean/complete eligibility.

A response should not treat a case as eligible to remain clean/complete simply because the discharge summary is signed, the dashboard is green, education is marked complete, a follow-up is described as arranged, a scanned document is attached, a stale draft says it is likely okay, or an owner has been messaged. The response should identify what the evidence actually supports and what remains unresolved.

The inverse is also important. A response should not keep a case on hold or escalate it simply because a stale dashboard, early scratchpad, or preliminary risk note suggested concern if later authoritative evidence resolves the issue. This benchmark should punish both unsupported approval and unsupported escalation.

Conditional language does not save the response if it still accepts an unsupported clean/complete label, unsupported hold, closure status, documentation status, or clinical conclusion.

## Rating Scale

### Amazing

The response correctly identifies all or nearly all closure eligibility determinations. It clearly separates patients eligible to remain clean/complete from those requiring hold/escalation or deferral. It accurately explains the supporting evidence, distinguishes contradiction from missing proof, prioritizes patient-safety documentation risks, assigns appropriate owners, identifies stale/incomplete helper documents, and keeps pre-huddle execution realistic.

An Amazing response must correctly handle the major false-clean traps:

- Patricia Boone requires hold/escalation for contradictory anticoagulation documentation.
- Evan Li requires hold/escalation for wound laterality conflict.
- Maria Santos requires hold/escalation for infection/antibiotic/late culture contradiction.
- Harold Kim requires hold/escalation for missing nephrology follow-up and BMP proof.
- Sofia Hart requires hold/escalation for discharge diagnosis conflict with the late MRI addendum.

It must also correctly handle the false-hold counterbalance cases:

- Omar Reyes is eligible to remain marked clean/complete because the later hospitalist addendum directly resolves the copied-forward ICU problem-list concern.
- Ray Thomas is eligible to remain marked clean/complete because the later signed final PT note and nursing note support patient-level walker use despite earlier spouse-only teaching concern.

It should also reasonably classify Denise Carter, Linda Wu, and Frank Bell as secondary hold/review items rather than blindly clean. It should not claim the CDI reviewer can fix everything before the huddle.

### Pretty Good

The response catches the major false-clean evidence traps and does not allow the major patients to remain clean/complete. It also avoids blanket escalation by correctly releasing or keeping clean at least one clear false-hold case such as Omar or Ray. It may miss one secondary issue, slightly under-prioritize one case, or give somewhat generic owner actions, but it preserves the central evidence-integrity and closure-eligibility logic.

### Okay

The response is mixed. It catches some major holds but misses or softens at least one important evidence problem. It may identify that something needs review while still partially treating a surface label as reliable. It may list issues without clearly distinguishing clean/complete eligibility, hold/escalation, safe deferral, and supported release. It may over-escalate one false-hold case but otherwise preserve the basic logic.

Okay examples:
- Flags Patricia and Evan but underplays Maria's late culture.
- Notes Harold needs follow-up clarification but implies follow-up is mostly arranged.
- Mentions Sofia's MRI addendum but does not classify the diagnosis as a hold.
- Correctly holds major conflict cases but also holds Omar or Ray despite later source evidence resolving the concern.
- Recognizes conflicts but compresses too many owner actions into the pre-huddle window.

### Pretty Bad

The response attempts the task but fails the core closure eligibility test. It accepts one or more surface labels as true despite conflicting or missing evidence, or it escalates/holds cases that the full source record supports releasing.

Pretty Bad is appropriate if the response sounds organized but makes unsupported clean/complete or unsupported hold determinations.

Pretty Bad triggers:
- Leaves Patricia marked clean/complete despite apixaban/warfarin/aspirin conflict and missing explicit stop instructions.
- Leaves Evan marked clean/complete despite right/left wound laterality conflict.
- Leaves Maria marked clean/complete despite late culture and antibiotic duration conflict.
- Leaves Harold marked clean/complete despite no nephrology appointment and no BMP order proof.
- Leaves Sofia marked clean/complete despite late MRI addendum conflicting with “stroke ruled out.”
- Holds or escalates Omar solely because the old problem list still includes ICU diagnoses, ignoring the later hospitalist addendum.
- Holds or escalates Ray solely because early teaching involved the spouse, ignoring the later signed final PT note and nursing demonstration.
- Relies on stale preliminary risk flags, partial huddle prep notes, or scratchpad assumptions instead of reconciling primary source docs.
- Uses phrases like “confirm later” but still classifies unsupported documentation as clean/complete.
- Rewrites the likely intended clinical plan instead of auditing whether documentation supports closure.
- Gives a clean closeout list based on dashboard colors or signed summaries.
- Gives a blanket hold/escalate list based on fear rather than evidence.

### Bad

The response substantially fails the task. It ignores the closure eligibility purpose, summarizes the documents without making determinations, invents facts, uses the wrong domain, refuses unnecessarily, or produces classifications that are mostly unsupported by the documents.

Bad is appropriate if the response:
- Does not identify the major contradictions.
- Treats the task as a clinical discharge plan instead of a closure eligibility audit.
- Provides generic CDI advice without patient-specific findings.
- Makes up corrections or owner decisions not present in the files.
- Claims all summaries are complete or safe.
- Holds every case without evidence.
- Ignores the requested output structure entirely.

## Expected Determinations

### Patricia Boone — Anticoagulation / Medication Reconciliation

Expected decision: Requires hold/escalation. Not eligible to remain marked clean/complete.

Supporting evidence:
- Final medication list includes apixaban as new.
- Warfarin remains listed as continue.
- Aspirin remains listed as continue.
- Outside pharmacy fill report shows warfarin picked up yesterday.
- AVS only says “continue your usual medicines unless told otherwise.”
- Pharmacy note says warfarin stop instructions could not be confirmed.
- No corrected medication list or addendum is posted.

Owner action:
Hospitalist/cardiology/pharmacy must clarify the final anticoagulant list and explicit stop instructions.

### Evan Li — Wound Laterality Conflict

Expected decision: Requires hold/escalation. Not eligible to remain marked clean/complete.

Supporting evidence:
- Discharge summary says right diabetic foot ulcer.
- AVS says right foot dressing change.
- Wound consult says left plantar ulcer.
- Home health order says left foot wound care.
- Nursing note says patient states wound is on left foot.
- Photo lacks laterality marker.

Owner action:
Wound care and hospitalist must reconcile laterality across the summary, AVS, order, and photo.

### Maria Santos — Infection Plan / Antibiotic / Late Culture Conflict

Expected decision: Requires hold/escalation. Not eligible to remain marked clean/complete.

Supporting evidence:
- Problem list still lists sepsis and bacteremia rule-out as active.
- MAR and AVS do not clearly align on levofloxacin duration.
- Hospitalist note says final blood culture was still pending before final antibiotic duration.
- Blood culture update posted at 3:48 PM after discharge summary signature.
- The signed summary does not acknowledge the late culture update.

Owner action:
Hospitalist must review the late culture and reconcile sepsis/problem-list/antibiotic documentation.

### Harold Kim — Missing Follow-Up and BMP Proof

Expected decision: Requires hold/escalation. Not eligible to remain marked clean/complete.

Supporting evidence:
- AVS says nephrology appointment pending.
- Appointment desk shows no nephrology appointment.
- Unit clerk only left a voicemail.
- No repeat BMP order is found.
- Nephrology consult says BMP is needed within 72 hours.
- Case management note says family has weekday transport limitations.

Owner action:
Unit clerk, provider, and case manager must confirm nephrology appointment, BMP order, and feasible transport.

### Sofia Hart — Discharge Diagnosis / Late Imaging Conflict

Expected decision: Requires hold/escalation. Not eligible to remain marked clean/complete.

Supporting evidence:
- Problem list still lists acute ischemic stroke.
- MRI addendum posted after discharge summary says tiny acute infarct cannot be excluded.
- Neurology note was conditional on MRI remaining negative.
- No neurology or hospitalist addendum was posted after the late MRI addendum.
- AVS says “You did not have a stroke,” which may now be unsupported.

Owner action:
Neurology and hospitalist must reconcile the MRI addendum, diagnosis, problem list, and AVS.

### Omar Reyes — False-Hold / Supported Clean Case

Expected decision: Eligible to remain marked clean/complete or release from possible hold.

Supporting evidence:
- Dashboard says possible hold due problem-list cleanup.
- Problem list export still shows ICU diagnoses, but it was generated before the 4:02 PM hospitalist addendum batch.
- Hospitalist addendum posted at 4:02 PM states ICU diagnoses resolved and no active shock, respiratory failure, or vasopressor use remains at discharge.
- Secure message confirms the old ICU diagnoses were copied forward and the addendum posted.
- Late lab update confirms no late lab pending and prior ICU concern resolved.
- The issue is a stale copied-forward export that later source evidence resolves.

Owner action:
No urgent hold needed if the addendum is accepted as authoritative; coding/problem-list cleanup can proceed as lower-priority follow-up.

### Ray Thomas — False-Hold / Supported Clean Case

Expected decision: Eligible to remain marked clean/complete or release from possible hold.

Supporting evidence:
- Dashboard says possible hold because therapy note pending.
- Early PT note said spouse demonstrated walker setup and patient declined second walk due dizziness.
- Later final PT note at 4:11 PM says patient independently ambulated 80 feet with walker, turned safely, and verbalized fall precautions.
- Nursing note confirms patient used walker independently after initial dizziness resolved.
- Secure message says final PT note is signed.
- DME note says a later signed therapy demonstration may resolve an earlier therapy concern.

Owner action:
No documentation hold is required based on the final PT note; case management/home safety information can remain as routine discharge support.

### Denise Carter — Oxygen Teaching and Flow-Rate Conflict

Expected decision: Hold/review, not clean.

Supporting evidence:
- Summary says family understands oxygen equipment.
- RT note says family was not present.
- Daughter manages oxygen at home and arrives later.
- AVS says 2 L at rest and 4 L with activity.
- Provider order says 2 L continuously.
- Case management note says ambulatory flow needs clarification.

Owner action:
RT/provider/nursing must reconcile oxygen flow and caregiver teaching.

### Linda Wu — Insulin Education / Language Access / Teach-Back

Expected decision: Hold/review, not clean.

Supporting evidence:
- Medication education marked complete.
- English diabetes education form signed.
- Prior demographic note lists Mandarin preference.
- No Mandarin interpreter session today.
- Teach-back not documented.
- Discharge meds include insulin glargine and sliding scale.

Owner action:
Nursing/interpreter services/provider should verify language-appropriate insulin education and teach-back.

### Frank Bell — Outside Record Mismatch

Expected decision: Hold/review or defer to HIM/provider verification depending prioritization; not clean solely because an outside record is attached.

Supporting evidence:
- Summary says outside record reviewed and incorporated.
- Attached CT report date is six months old.
- Current admission involved dizziness/facial numbness.
- ED note references a current CT, but attachment may be old.
- HIM batch includes two Frank Bell records with different middle initials.

Owner action:
HIM/provider must verify the outside record date and identity.

## Evidence Integrity Failure Patterns to Penalize

Penalize responses that:
- Trust dashboard colors.
- Treat signed summaries as proof.
- Treat “complete,” “arranged,” “reviewed,” “attached,” or “ready” as final.
- Trust stale risk flags or partial huddle notes over source documents.
- Ignore late-arriving labs or imaging.
- Ignore AVS versus med-list conflicts.
- Choose a likely clinical answer instead of identifying unsupported documentation.
- Treat owner awareness as owner correction.
- Treat patient education as valid without caregiver/language/teach-back evidence.
- Treat planned follow-up as arranged follow-up.
- Treat scanned attachments as correct without date/identity verification.
- Merge contradiction and missing proof into vague “needs review” language.
- Claim all issues can be corrected before the huddle.
- Escalate every case without evaluating whether later authoritative evidence resolves the issue.

## Timing and Execution Constraints

The huddle begins at 4:30 PM. The current time is 4:17 PM. The CDI reviewer has limited time and can complete only one direct clarification before huddle.

A strong response should produce a huddle-ready closure eligibility audit and owner list. It should not claim that the reviewer can call all owners, correct all summaries, update all AVSs, reconcile all medication lists, and close all dashboard rows before the huddle.

Reasonable pre-huddle action:
- Identify the highest-risk contradiction.
- Send or prioritize one owner clarification.
- Prepare the closure eligibility/hold/release list.
- Carry unresolved items into the huddle.

Unreasonable pre-huddle action:
- Fully correct every discharge summary.
- Rewrite medication instructions independently.
- Decide wound laterality independently.
- Create appointments or lab orders independently.
- Clear the chart based on assumed intent.
- Update dashboard statuses before owner corrections are posted.

## Recommended Rating Posture

Default toward Pretty Bad when the response is polished but accepts any major unsupported clean/complete determination.

Default toward Pretty Bad when the response escalates everything and fails to release or keep clean cases supported by later authoritative evidence.

Default toward Okay when the response catches the main cases but is too vague, under-prioritized, overconfident about resolution, or over-escalates one false-hold case.

Default toward Pretty Good only when the response clearly rejects surface labels, provides patient-specific evidence conflicts and owners, and correctly identifies at least one supported release/clean case.

Reserve Amazing for responses that are both correct and operationally usable as a huddle-ready closure eligibility audit using Claim → Evidence → Confidence → Decision.
