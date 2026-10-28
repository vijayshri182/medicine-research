# Medicine Research

## Mission
Use AI-assisted scientific research to help people affected by diseases by identifying credible evidence, evaluating potential treatments and disease-modifying interventions, and translating validated findings into safe, accessible, and understandable information.

## Vision
A traceable, transparent research knowledge base that empowers patients and caregivers with reliable, useful, evidence-based information to discuss with qualified clinicians—without making medical diagnoses or treatment prescriptions.

## Purpose
This repository documents structured, evidence-based research into Type 2 diabetes (T2D) and related metabolic dysfunction, with emphasis on distinguishing remission, disease modification, and cure. The goal is patient benefit through reliable, traceable research—not a diagnostic or treatment-prescribing system.

## Scope
- **Primary focus:** Type 2 diabetes (see `research/diseases/type-2-diabetes/`) — preserving the existing research scope and WP-02 roadmap.
- **Approach:** Dual-track AI-assisted research (Discovery + Translation). Evidence appraisal across human trials, systematic reviews, observational studies, animal/laboratory research, and emerging interventions.
- **Boundaries:** Documentation only. No diagnosis, no treatment prescriptions, no automated medical decision systems. No clinical advice. No promises of cures. AI-generated hypotheses are not evidence.

## Disease Coverage (current)
- Type 2 Diabetes (`research/diseases/type-2-diabetes/`) — biology, remission evidence, beta-cell recovery, emerging treatments, natural compounds, clinical trials, research gaps.

## Research Workflow
1. **Discovery:** Investigate mechanisms, identify promising interventions, analyze contradictory results, evaluate hypotheses, locate evidence gaps.
2. **Source management:** Register sources in `research/source-register.csv`. Appraise via `templates/study-appraisal.md`.
3. **Claim tracking:** Log material claims in `research/claim-ledger.csv` with evidence level, supporting/conflicting sources, limitations, confidence. Label AI hypotheses separately from verified findings.
4. **Patient-benefit evaluation:** Assess evidence strength/reproducibility, meaningful outcomes/durability, safety/harms, population applicability, affordability/availability (including India), uncertainty/accessibility/usefulness.
5. **Translation:** Turn validated findings into accessible explanations, evidence summaries, affordability/accessibility assessments, and questions patients can discuss with qualified clinicians.
6. **Disease pages:** Build per-disease documentation following the roadmap in `PROJECT_PLAN.md`.
7. **Governance:** Follow `AGENTS.md` and `research/evidence-methodology.md` for safeguards and standards. AI output alone is never evidence.

## Navigation
- [Project Plan](PROJECT_PLAN.md)
- [Progress](PROGRESS.md)
- [Changelog](CHANGELOG.md)
- [Agents/Rules](AGENTS.md)
- [Research Overview](research/README.md)
- [Evidence Methodology](research/evidence-methodology.md)
- [Templates](templates/)

## Status
- **Phase:** Phase 0 — Initialization (complete after initial commit)
- **Focus:** Establishing evidence baseline for Type 2 diabetes remission (DiRECT, DIADEM-I) and building traceable registries.

## Important Notes
- Remission ≠ cure. On-treatment benefits differ from medication-free remission/durable disease modification.
- All material claims require traceable sources; uncertainties and null results are reported.
- This repo must not contain PHI/PII, credentials, or medical advice. Follow all safeguards in `AGENTS.md`.
