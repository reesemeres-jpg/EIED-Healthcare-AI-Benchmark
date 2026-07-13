# EIED

## Evidence Integrity & Eligibility Determination

### A Healthcare AI Benchmark Suite for Evidence Validation, Documentation Integrity, and Eligibility Reasoning

**Version 1.0 | Final Portfolio Release | Meredith Reese, RN | July 2026**

The **Evidence Integrity & Eligibility Determination (EIED)** benchmark suite evaluates whether AI systems can determine when available evidence actually supports a healthcare decision.

Rather than rewarding factual recall, polished language, or agreement with a dashboard label, EIED asks whether the evidence is **sufficient, current, internally consistent, patient-specific, and authoritative enough** to justify the conclusion.

> **Has the AI earned the right to reach this conclusion?**

## Suite Identity

**Claim → Evidence → Confidence → Decision**

Every benchmark asks:

1. What is the **Claim**?
2. What is the **Evidence**?
3. How confident should the model be?
4. What **Decision** does the evidence justify?

## Signature Principle

> **Labels are claims—not evidence.**

A record marked *Complete, Signed, Reviewed, Attached, Scheduled, Verified, Green,* or *Closed* may still be unsupported. The inverse matters too: a stale hold, preliminary note, or incomplete-looking record may be resolved by later authoritative evidence.

EIED therefore penalizes both:

- unsupported release, approval, inclusion, finalization, application, or closure; and
- unsupported hold, denial, exclusion, escalation, or deferral.

## Version 1.0 at a Glance

- **12** original healthcare AI benchmarks
- **360** fictional source documents
- **48** submission-ready batch archives
- **12** system/task prompts
- **12** strict grading rubrics
- **12** benchmark design notes
- Domains spanning documentation closure, prior authorization, research eligibility, population health, medical necessity, quality measurement, medication safety, case resolution, coding integrity, longitudinal reconciliation, and clinical guideline applicability

## Benchmark Index

| # | Benchmark | Primary domain | Core decision |
|---:|---|---|---|
| 001 | [Discharge Documentation Closure Eligibility Audit](Benchmarks/Benchmark001_Discharge_Documentation_Closure_Eligibility_Audit/) | Clinical documentation integrity and care-transition closure | Has the record earned clean/complete closure status? |
| 002 | [Prior Authorization Evidence Review](Benchmarks/Benchmark002_Prior_Authorization_Evidence_Review/) | Payer criteria, imaging, specialty medication, and DME authorization | Has the request earned submission, hold, or escalation? |
| 003 | [Clinical Trial Eligibility Validation](Benchmarks/Benchmark003_Clinical_Trial_Eligibility_Validation/) | Oncology research screening and protocol eligibility | Has the candidate earned the right to proceed? |
| 004 | [Registry Enrollment Audit](Benchmarks/Benchmark004_Registry_Enrollment_Audit/) | Population health registry and colorectal screening outreach | Has the patient earned inclusion, exclusion, suppression, or outreach? |
| 005 | [Medical Necessity Documentation Review - Post-Acute Services](Benchmarks/Benchmark005_Medical_Necessity_Post_Acute_Services/) | Home health, DME, wound therapy, oxygen, infusion, and outpatient therapy | Has the service earned a medically necessary determination? |
| 006 | [Medical Necessity Documentation Review - Utilization Management](Benchmarks/Benchmark006_Medical_Necessity_Utilization_Management/) | Imaging, procedures, treatment history, and exception pathways | Has medical necessity been established for this service and patient? |
| 007 | [Quality Measure Inclusion Validation](Benchmarks/Benchmark007_Quality_Measure_Inclusion_Validation/) | Hypertension quality-measure denominator, exclusion, and numerator review | Has the patient earned inclusion, exclusion, compliance, or hold status? |
| 008 | [Medication Safety Verification](Benchmarks/Benchmark008_Medication_Safety_Verification/) | High-risk medication release, dispensing, and alert verification | Has the medication plan earned release or withholding? |
| 009 | [Case Closure Readiness Audit](Benchmarks/Benchmark009_Case_Closure_Readiness_Audit/) | Patient safety, complaint, referral, privacy, communication, equipment, and follow-up cases | Has the case earned true resolution and closure? |
| 010 | [Clinical Coding Evidence Validation](Benchmarks/Benchmark010_Clinical_Coding_Evidence_Validation/) | Diagnosis and principal-diagnosis coding integrity | Has the diagnosis or principal-diagnosis assignment earned final coding? |
| 011 | [Longitudinal Evidence Reconciliation](Benchmarks/Benchmark011_Longitudinal_Evidence_Reconciliation/) | Whole-record reconciliation across hospital, clinic, specialist, rehabilitation, home, pharmacy, and portal records | Does the longitudinal record support the conclusion? |
| 012 | [Clinical Guideline Applicability Audit](Benchmarks/Benchmark012_Clinical_Guideline_Applicability_Audit/) | Patient-specific guideline population, eligibility, exclusion, version, and safety-gate validation | Does the evidence actually justify applying this rule? |

## Portfolio Materials

- [Portfolio overview (PDF)](Portfolio/EIED_v1_0_Portfolio_Overview_Meredith_Reese_RN.pdf)
- [One-page portfolio summary (PDF)](Portfolio/EIED_v1_0_One_Page_Summary_Meredith_Reese_RN.pdf)
- Editable DOCX versions are included in the same folder.

## Repository Navigation

- `Portfolio/` - polished portfolio overview and one-page summary in DOCX and PDF
- `Benchmarks/` - twelve complete benchmark packages with source documents, prompts, rubrics, design notes, and original archives
- `BENCHMARK_INDEX.md` - portfolio-facing summary of all twelve benchmarks
- `COVERAGE_MATRIX.md` - cross-benchmark reasoning coverage and distinctive contribution map
- `EVALUATION_FRAMEWORK.md` - EIED pillars and reasoning methodology
- `DESIGN_METHODOLOGY.md` - construction principles and balanced failure design
- `PACKAGE_MANIFEST.md` - verified package counts and structure
- `GITHUB_PUBLISHING_GUIDE.md` - repository description, topics, and publishing checklist
- `RIGHTS_AND_USE.md` - copyright and reuse terms
- `DISCLAIMER.md` - scope, fictional-data, and validation limitations
- `AUTHOR.md` - author background and related benchmark suites

## Relationship to Other Suites

- **HORB** asks: *Can the AI reason through realistic healthcare operations?*
- **EIED** asks: *Has the AI earned the right to reach this conclusion?*
- **UCM** asks: *Has the AI exceeded what it can justify?*

HORB emphasizes operational reasoning. EIED emphasizes evidence-supported decisions. UCM emphasizes uncertainty boundaries and confidence calibration.

## Author

**Meredith Reese, RN**  
Registered Nurse | Healthcare AI Evaluation & Benchmark Design  
GitHub: https://github.com/reesemeres-jpg

## Scope

All scenarios and records are fictional. EIED is a portfolio and evaluation-design project, not clinical guidance or a validated regulatory instrument. No protected health information is included.
