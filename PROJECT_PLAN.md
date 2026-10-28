# PROJECT_PLAN.md — Medicine Research Project Plan

## Mission
Build a transparent, traceable, and conservative research knowledge base on diabetes/metabolic disease that distinguishes evidence from hypothesis, reports uncertainties and null results, and never provides clinical advice or cure promises.

## Objectives
1. Establish a human evidence baseline for Type 2 diabetes remission with precise definitions and verifiable citations.
2. Document disease mechanisms (hepatic/pancreatic fat, insulin resistance, beta-cell dysfunction/recovery limits).
3. Critically evaluate emerging pharmacologic, surgical, and regenerative approaches.
4. Evaluate natural compounds (starting with Shikuwasa, nobiletin, tangeretin; Indian alternatives: amla, jamun, mosambi, kinnow) with preclinical/human separation.
5. Maintain reproducible clinical-trial intelligence from registries.
6. Create a transparent prioritization framework without overstating evidence.

## Scope
- **In scope:** T2D-focused documentation, evidence appraisal, source/claim registries, templates, governance.
- **Out of scope:** Clinical decision support, treatment recommendations, apps/tools making medical decisions, PHI handling, unapproved external integrations, implementing interventions.

## Workstreams
1. **Governance & Infrastructure** — AGENTS, methodology, registries, templates, git hygiene.
2. **Disease Baselines** — Per-disease biology, remission evidence, gaps.
3. **Mechanisms** — Fat distribution, beta-cell biology, recovery limits.
4. **Interventions** — Emerging treatments and natural compounds.
5. **Trials Intelligence** — Registry tracking, verification.
6. **Synthesis** — Prioritization, uncertainty mapping.

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
| Overstating preclinical findings | High | Separate evidence by study type; label hypotheses |
| Stale trial statuses | Med-High | Require `last-verified` for registry entries |
| PHI/credentials leakage | High | `.gitignore` protections; no PHI policy enforced |
| Fabricating citations | High | Flag unverified claims; do not invent references |

## Success Metrics
- All material T2D claims traceable via source/claim registries or flagged unverified.
- Remission trials (DiRECT/DIADEM-I) documented with verifiable details and limitations.
- Natural compounds clearly separated by evidence type with no treatment recommendations.
- Trial intelligence method reproducible with verified statuses.
- Governance documents consistent across repo.
- Clean initial commit with only intended files.
