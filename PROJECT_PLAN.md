# PROJECT_PLAN.md — Medicine Research Project Plan

## Mission
Use AI-assisted scientific research to help people affected by diseases by identifying credible evidence, evaluating potential treatments and disease-modifying interventions, and translating validated findings into safe, accessible, and understandable information.

## Vision
Produce reliable, useful, traceable research that helps patients and caregivers understand credible options and evidence gaps, equipping them to ask informed questions of qualified clinicians—without providing diagnoses, treatment prescriptions, or cure promises.

## Objectives
1. **Evidence baseline:** Establish a human evidence baseline for Type 2 diabetes remission with precise definitions and verifiable citations (preserve and prioritize WP-02).
2. **Mechanisms:** Document disease mechanisms (hepatic/pancreatic fat, insulin resistance, beta-cell dysfunction/recovery limits).
3. **Interventions:** Critically evaluate emerging pharmacologic, surgical, and regenerative approaches, distinguishing on-treatment benefits from medication-free remission and durable disease modification.
4. **Natural compounds:** Evaluate natural compounds (starting with Shikuwasa, nobiletin, tangeretin; Indian alternatives: amla, jamun, mosambi, kinnow) with preclinical/human separation.
5. **Trials intelligence:** Maintain reproducible clinical-trial intelligence from registries with verification dates.
6. **Synthesis & prioritization:** Create a transparent prioritization framework without overstating evidence.
7. **Discovery:** Use AI-assisted methods to investigate mechanisms, identify promising interventions, analyze contradictions, evaluate hypotheses, and locate evidence gaps.
8. **Translation:** Convert validated findings into accessible explanations, evidence summaries, affordability/accessibility assessments (including India), and questions patients can discuss with qualified clinicians.
9. **Patient-benefit focus:** Evaluate interventions by evidence strength/reproducibility, meaningful outcomes/durability, safety/harms, population applicability, affordability/availability, uncertainty/accessibility/usefulness.

## Scope
- **In scope:** T2D-focused documentation (existing scope preserved), AI-assisted discovery and translation, evidence appraisal, source/claim registries, templates, governance, patient-benefit evaluation, affordability/accessibility assessments.
- **Out of scope:** Diagnosis, treatment prescriptions, clinical decision support, treatment recommendations, apps/tools making medical decisions, PHI handling, unapproved external integrations, implementing interventions. AI output alone is not evidence.

## Workstreams
1. **Governance & Infrastructure** — AGENTS, methodology, registries, templates, git hygiene, patient-benefit framework.
2. **Discovery (AI-assisted)** — Mechanisms, promising interventions, contradictions, hypotheses, evidence gaps, source discovery.
3. **Disease Baselines** — Per-disease biology, remission evidence (WP-02 priority), gaps.
4. **Mechanisms** — Fat distribution, beta-cell biology, recovery limits.
5. **Interventions** — Emerging treatments and natural compounds.
6. **Trials Intelligence** — Registry tracking, verification.
7. **Synthesis & Prioritization** — Prioritization, uncertainty mapping, patient-benefit evaluation.
8. **Translation** — Accessible summaries, affordability/accessibility (including India), patient questions for qualified clinicians.

## Phases and Deliverables

### Phase 1 — Establish the human evidence baseline
**Goal:** Document accepted definition of T2D remission, major remission trials, eligibility, rates, durability, relapse, safety, limitations, generalizability. Start with DiRECT, DIADEM-I; verify against original sources.
**Deliverables:**
- `research/diseases/type-2-diabetes/remission-evidence.md` (verifiable entries)
- Updated `research/source-register.csv` and `research/claim-ledger.csv` for remission claims
- Notes on definitions/criteria across studies

**Acceptance Criteria:**
- [ ] Remission definition(s) stated with citations/criteria
- [ ] DiRECT and DIADEM-I described with design, population, outcomes, follow-up, relapse, limitations
- [ ] Each material claim traced or flagged unverified
- [ ] Distinction between remission/control/cure explicit

### Phase 2 — Investigate disease-modifying mechanisms
**Goal:** Hepatic/pancreatic fat, insulin resistance, beta-cell dysfunction/stress/identity, recovery potential, limits of human regenerative evidence.
**Deliverables:**
- `research/diseases/type-2-diabetes/disease-biology.md` (evidence-graded)
- `research/diseases/type-2-diabetes/beta-cell-recovery.md` (separating preclinical/human)

**Acceptance Criteria:**
- [ ] Mechanisms graded by human evidence strength
- [ ] Regenerative claims limited to verifiable human data
- [ ] Uncertainties and contradictions reported

### Phase 3 — Evaluate emerging interventions
**Goal:** Pharmacologic combinations, incretin-based treatments, metabolic surgery, credible regenerative approaches. Separate on-treatment vs medication-free remission/durable modification.
**Deliverables:**
- `research/diseases/type-2-diabetes/emerging-treatments.md`

**Acceptance Criteria:**
- [ ] On-treatment vs medication-free effects distinguished
- [ ] Durability/relapse reported where known
- [ ] Safety/limitations documented

### Phase 4 — Evaluate natural compounds
**Goal:** Start with Shikuwasa, nobiletin, tangeretin; then amla, jamun, mosambi, kinnow. Separate lab/animal/observational/human; include dose/formulation/bioavailability/toxicity/interactions/gaps.
**Deliverables:**
- `research/diseases/type-2-diabetes/natural-compounds.md`

**Acceptance Criteria:**
- [ ] Each compound has evidence table by study type
- [ ] Human evidence explicitly stated (often limited/absent)
- [ ] Dose/toxicity/interactions/bioavailability noted or gaps flagged
- [ ] No treatment recommendations made

### Phase 5 — Clinical-trial intelligence
**Goal:** Reproducible method to locate trials/publications; record registry ID, status, design, criteria, endpoints, sponsor, results, verification date. Never claim recruiting without checking registry.
**Deliverables:**
- `research/diseases/type-2-diabetes/clinical-trials.md` (with verification protocol)
- Registry entries as needed in source/claim registers

**Acceptance Criteria:**
- [ ] Verification method documented
- [ ] Entries include status+last-verified
- [ ] Recruiting claims require verified registry status

### Phase 6 — Synthesis and prioritization
**Goal:** Transparent framework prioritizing by human evidence, benefit, durability, safety, feasibility, affordability, uncertainty. Do not rank as proven reversals from plausibility alone.
**Deliverables:**
- `research/diseases/type-2-diabetes/research-gaps.md` (with prioritization framework)

**Acceptance Criteria:**
- [ ] Framework lists explicit criteria and weights/rubric
- [ ] Plausibility cannot override human evidence
- [ ] Uncertainty mapped; gaps prioritized conservatively

## Risks and Mitigations
| Risk | Impact | Mitigation |
|------|--------|------------|
| Citing secondary summaries as primary evidence | High | Verify against original sources; register in source-register |
| Conflating remission and cure | High | Enforce definitions in AGENTS/README/disease pages |
| Overstating preclinical findings | High | Separate evidence by study type; label hypotheses; label AI hypotheses separately |
| Stale trial statuses | Med-High | Require `last-verified` for registry entries |
| PHI/credentials leakage | High | `.gitignore` protections; no PHI policy enforced |
| Fabricating citations | High | Flag unverified claims; do not invent references |
| Treating AI output as evidence | High | AI output alone never evidence; require human verification against primary sources |
| Slipping into diagnosis/treatment advice | High | Explicit boundaries in AGENTS/README; no diagnostic/prescribing system; frame as questions for qualified clinicians |

## Success Metrics
- **Traceability:** All material T2D claims traceable via source/claim registries or flagged unverified. AI hypotheses clearly labeled as such (not findings).
- **Human evidence baseline:** Remission trials (DiRECT/DIADEM-I) documented with verifiable details and limitations (WP-02 priority maintained).
- **Evidence separation:** Natural compounds clearly separated by evidence type with no treatment recommendations.
- **Trials intelligence:** Trial intelligence method reproducible with verified statuses.
- **Patient benefit:** Validated findings translated into accessible summaries with affordability/accessibility assessments (including India where relevant) and questions for qualified clinicians.
- **Balanced evaluation:** Interventions evaluated by evidence strength/reproducibility, meaningful outcomes/durability, safety/harms, population applicability, affordability/availability, uncertainty/accessibility/usefulness.
- **Governance consistency:** Governance documents consistent across repo with clear AI/hypothesis boundaries and no diagnostic/prescribing system.
- **Clean history:** Only intended files committed with clear messages.
