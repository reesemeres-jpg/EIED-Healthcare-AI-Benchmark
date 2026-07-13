# EIED Benchmark Index

Version 1.0 contains twelve complete benchmarks. Each benchmark includes 30 fictional source documents, four batch archives, a system/task prompt, strict grading guidelines, and design notes.

## Benchmark 001 - Discharge Documentation Closure Eligibility Audit

**Domain:** Clinical documentation integrity and care-transition closure

**Decision question:** Has the record earned clean/complete closure status?

Audits discharge records that appear complete and determines whether medication, wound, infection, follow-up, education, diagnosis, and DME evidence actually supports closure.

**Evidence pressure:** Signed-but-conflicting records; late results; wrong laterality; missing follow-up proof; stale copied-forward text; resolved apparent holds.

**Decision classes:** Remain clean/complete; hold; escalate; defer; release from hold.

**Distinctive contribution:** Separates administrative completion from evidentiary closure.

## Benchmark 002 - Prior Authorization Evidence Review

**Domain:** Payer criteria, imaging, specialty medication, and DME authorization

**Decision question:** Has the request earned submission, hold, or escalation?

Tests whether prior authorization packets satisfy current payer criteria rather than merely appearing administratively complete or being labeled criteria met.

**Evidence pressure:** Criteria windows; body-region mismatch; therapy history; medication safety; exceptions; stale scratchpads; later addenda.

**Decision classes:** Submit; hold; correct; withdraw; escalate; release from hold.

**Distinctive contribution:** Tests exact criteria application without inheriting queue status.

## Benchmark 003 - Clinical Trial Eligibility Validation

**Domain:** Oncology research screening and protocol eligibility

**Decision question:** Has the candidate earned the right to proceed?

Evaluates protocol eligibility using consent version and timing, lab windows, washout periods, performance status, medication restrictions, imaging, language support, and exceptions.

**Evidence pressure:** Retired consent; pre-consent procedures; out-of-window labs; exact washout timing; current ECOG; interpreter attestation; final imaging.

**Decision classes:** Eligible; hold; exclude; escalate to PI; defer; release from hold.

**Distinctive contribution:** Tests protocol-specific eligibility, timing, and exception evidence.

## Benchmark 004 - Registry Enrollment Audit

**Domain:** Population health registry and colorectal screening outreach

**Decision question:** Has the patient earned inclusion, exclusion, suppression, or outreach?

Audits registry labels against outside records, patient identity, procedure quality, screening intervals, high-risk factors, and stale exclusions.

**Evidence pressure:** Outside record matching; spouse-result mismatch; incomplete colonoscopy; scheduled vs completed; total vs segmental colectomy; stale hospice flags.

**Decision classes:** Outreach; suppress; exclude; update; hold; escalate; release.

**Distinctive contribution:** Tests registry truth, identity, and completion-status integrity.

## Benchmark 005 - Medical Necessity Documentation Review - Post-Acute Services

**Domain:** Home health, DME, wound therapy, oxygen, infusion, and outpatient therapy

**Decision question:** Has the service earned a medically necessary determination?

Determines whether post-acute service requests are supported by patient-specific skilled-need, functional, safety, and treatment evidence rather than signed forms or supplier-ready packets.

**Evidence pressure:** Template language; service-specific criteria; skilled need; homebound status; wound and oxygen proof; copied forms; later supporting notes.

**Decision classes:** Support; hold; correct; escalate; deny/withdraw; release from hold.

**Distinctive contribution:** Tests whether post-acute documentation earns medical necessity.

## Benchmark 006 - Medical Necessity Documentation Review - Utilization Management

**Domain:** Imaging, procedures, treatment history, and exception pathways

**Decision question:** Has medical necessity been established for this service and patient?

Reviews diagnostic and procedural requests for current symptoms, conservative treatment, body-region matching, procedure history, contraindications, and urgent exceptions.

**Evidence pressure:** Wrong body region; stale therapy; prescribed vs completed treatment; symptom-duration rules; identity mismatch; urgent exceptions; later addenda.

**Decision classes:** Submit/approve pathway; hold; correct; withdraw; escalate; release from hold.

**Distinctive contribution:** Tests patient-specific procedural necessity and exception pathways.

## Benchmark 007 - Quality Measure Inclusion Validation

**Domain:** Hypertension quality-measure denominator, exclusion, and numerator review

**Decision question:** Has the patient earned inclusion, exclusion, compliance, or hold status?

Separates denominator membership, valid exclusions, and numerator compliance rather than inheriting a compressed dashboard status.

**Evidence pressure:** Qualifying encounters; BP source rules; exclusion evidence; repeat readings; outside values; dates; stale status; denominator vs numerator conflation.

**Decision classes:** Include; exclude; compliant; noncompliant; hold; release.

**Distinctive contribution:** Tests measure membership and performance as separate claims.

## Benchmark 008 - Medication Safety Verification

**Domain:** High-risk medication release, dispensing, and alert verification

**Decision question:** Has the medication plan earned release or withholding?

Validates medication plans against current orders, renal function, weight, monitoring, outside prescriptions, recent events, discontinuations, and resolved allergy or duplicate alerts.

**Evidence pressure:** Stale labs; claims vs active therapy; critical late values; interacting prescriptions; cancelled procedures; overdose history; delabeling; outside monitoring.

**Decision classes:** Release; hold; cancel; request information; urgent escalation; release from hold.

**Distinctive contribution:** Tests release decisions for high-risk medication evidence.

## Benchmark 009 - Case Closure Readiness Audit

**Domain:** Patient safety, complaint, referral, privacy, communication, equipment, and follow-up cases

**Decision question:** Has the case earned true resolution and closure?

Determines whether communication, corrective action, referral outcomes, source identity, privacy review, equipment resolution, and owner accountability support case closure.

**Evidence pressure:** Attempted vs completed communication; planned vs verified action; wrong-patient evidence; final vendor reports; privacy obligations; owner/due-date gaps.

**Decision classes:** Close; hold; transfer; escalate; defer; release from hold.

**Distinctive contribution:** Tests whether attempted work has become verified resolution.

## Benchmark 010 - Clinical Coding Evidence Validation

**Domain:** Diagnosis and principal-diagnosis coding integrity

**Decision question:** Has the diagnosis or principal-diagnosis assignment earned final coding?

Validates proposed coding against final patient-specific physician documentation, specialist conclusions, baseline trends, pathology, operative reports, addenda, and identity-correct evidence.

**Evidence pressure:** Abnormal lab vs diagnosis; empiric treatment; draft vs final documentation; baseline comparison; wrong-patient attachments; expected postoperative support; unsigned queries.

**Decision classes:** Finalize; revise; remove; query; hold; escalate; release from hold.

**Distinctive contribution:** Tests whether diagnosis and sequencing claims earn final coding.

## Benchmark 011 - Longitudinal Evidence Reconciliation

**Domain:** Whole-record reconciliation across hospital, clinic, specialist, rehabilitation, home, pharmacy, and portal records

**Decision question:** Does the longitudinal record support the conclusion?

Determines whether a conclusion remains supported after the entire multi-month record is reconciled across hospital care, clinic follow-up, specialists, rehabilitation, home health, pharmacy, outside records, and patient communication.

**Evidence pressure:** Copied-forward diagnoses; repeated but unsupported causality; service discharge vs recovery; contextually unreliable measures; recurrence after closure; stale holds resolved by current evidence.

**Decision classes:** Supported; supported with revision; not supported; unresolved; release from hold; keep open/hold.

**Distinctive contribution:** Tests whether the full longitudinal story supports the durable conclusion.

## Benchmark 012 - Clinical Guideline Applicability Audit

**Domain:** Patient-specific guideline population, eligibility, exclusion, version, and safety-gate validation

**Decision question:** Does the evidence actually justify applying this rule?

Determines whether patient-specific evidence establishes entry into the active guideline population and satisfies inclusion pathways, exclusions, setting, chronicity, and safety prerequisites.

**Evidence pressure:** Unconfirmed qualifying diagnosis; independent eligibility pathways; wrong guideline version; acute vs chronic abnormalities; excluded populations; disease eligibility vs medication-safety gates.

**Decision classes:** Applicable; applicable with conditions; not applicable; insufficient evidence; defer pending verification; correctly withheld.

**Distinctive contribution:** Tests the right to invoke a rule, not merely the ability to quote it.
