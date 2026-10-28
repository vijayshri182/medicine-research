# AGENTS.md — Medicine Research Repository

## Scope and Purpose
This repository is for structured research documentation on diabetes and related metabolic conditions. It is **documentation only**. Do not implement an application, automated medical decision system, clinical tool, or unapproved external integrations.

## Medical Research Safeguards (Mandatory)
- **No clinical advice.** Do not recommend starting, stopping, changing, or adjusting prescribed medications/treatments. Any mention of treatment changes must be explicitly flagged as research context only.
- **Distinction of outcomes.** Clearly distinguish: diabetes remission, improved glucose control during treatment, functional recovery, disease modification, and a permanent cure. Do not conflate these terms.
- **Evidence boundaries.** Separate established human evidence from observational studies, animal studies, laboratory research, hypotheses, mechanistic plausibility, and unsupported claims.
- **No promises.** Never promise cures, guaranteed outcomes, or "reversals". Use cautious language (e.g., "evidence suggests", "in small trials", "uncertain").
- **Population-level only.** Never infer individual treatment suitability from population-level research alone.
- **Safety reporting.** Record adverse effects, contraindications, interactions, dose/toxicity concerns, bioavailability limitations, and population applicability when known.
- **Patient privacy.** Never commit credentials, API tokens, `.env` files, patient-identifiable information (PHI/PII), or private medical records.

## Evidence Standards
- **Hierarchy of evidence:** Prefer peer-reviewed systematic reviews/meta-analyses, randomized controlled trials (RCTs), recognized clinical guidelines (e.g., ADA, EASD, WHO, ICMR) over observational, mechanistic, or preclinical studies.
- **Primary sources:** Verify claims against original publications/registries (PubMed, ClinicalTrials.gov). Do not rely solely on secondary summaries.
- **Traceability:** Every material medical claim must have a traceable source recorded in `research/source-register.csv` and/or linked via `research/claim-ledger.csv`.
- **Contradictory evidence:** Report null results and contradictory findings, not just positive studies.
- **Statistical vs clinical:** Distinguish statistical significance from clinical significance.
- **Certainty & uncertainty:** State evidence certainty/limitations. If inference is a project hypothesis (not published), label it as such.
- **Stale evidence:** Use publication dates and `last-verified` dates to identify potentially stale evidence.
- **Verification gaps:** If a claim cannot be verified from a reliable source, flag it explicitly rather than fabricating citations.

## Research Workflow
1. **Register sources** in `research/source-register.csv` (include DOI/registry ID, URL, type, population, status, last-verified).
2. **Track claims** in `research/claim-ledger.csv` (claim, disease/intervention, evidence level, supporting/conflicting sources, limitations, confidence, last-reviewed).
3. **Appraise studies** using `templates/study-appraisal.md`.
4. **Document candidates** using `templates/candidate-intervention.md` with separate sections for preclinical/observational/human evidence.
5. **Update regularly** per `research/evidence-methodology.md` update policy.

## Git Safety & Source Verification
- **Scope:** Only files in this repository. Do not modify other repositories/projects.
- **No destructive Git:** Do not overwrite/delete/reinitialize existing repos or use destructive commands (force-push not anticipated; never rewrite history carelessly).
- **Secrets:** Pre-commit checks should avoid committing secrets/PHI. `.gitignore` includes protections.
- **Intentional staging:** Stage only explicitly created/modified research files. Review diff before committing.
- **Attribution:** Do not invent citations, trial results, publication dates, or findings.
- **Registry checks:** Never describe a trial as recruiting without verifying current status on ClinicalTrials.gov (or equivalent registry).

## Definitions (keep consistent)
- **Diabetes remission (T2D):** Follow accepted definitions (e.g., DiRECT/DIADEM-style) as documented in disease files; explicitly note criteria vary by study.
- **On-treatment benefit:** Effect observed while intervention/drug is ongoing.
- **Medication-free remission:** Remission after stopping glucose-lowering medications under study criteria.
- **Durable remission:** Remission sustained over time (report duration/follow-up).
- **Relapse:** Return to diabetes criteria after remission.
- **Disease modification:** Slowing/progression-reversal of underlying pathophysiology with durable effect beyond on-treatment control (rarely demonstrated in humans).
- **Cure:** No credible, widely accepted human evidence for a permanent cure of T2D at this time; do not claim otherwise.
