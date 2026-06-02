# Eco‑Cat‑Food — Non‑Confidential Technical Package

> Language: English | 中文：[`Eco-Cat-Food_Technical_Package_NONCONFIDENTIAL_SINGLE_v0.9_2026-02-10.zh-CN.md`](Eco-Cat-Food_Technical_Package_NONCONFIDENTIAL_SINGLE_v0.9_2026-02-10.zh-CN.md)

> **SUPERSEDED / HISTORICAL — 2026-05-30 status update**
> This v0.9 package reflects the historical FSHR small-molecule route as of 2026-02-10. That route has since been retired as a Gate 0.5 No-Start. This document is retained for transparency and auditability, but it does not represent the current active development path and should not be shared as the current project technical package. See the [current public status](../STATUS_UPDATE_2026-05-30.md).

Version: v0.9‑EN

Date: 2026-02-10

Original audience: Technical due diligence / research collaborators (technical teams / investor technical advisors)

Current status: **NON-CONFIDENTIAL HISTORICAL PACKAGE — superseded; not the current technical package**

Contact: [Wayne Zhang](https://www.linkedin.com/in/waynezhangfan)

---

**Important Notice (Please Read First)**

- This project is currently in a **purely theoretical/planning phase**: as of the date of this document, we **have not obtained any in vitro or in vivo empirical data**; both the scientific feasibility and safety of the approach are **unknown**.
- This non‑confidential technical package is intended solely to show how we decompose R&D into an **auditable Gate process and deliverables** (“governance & audit maturity”), and to make explicit which key scientific questions still have **zero data and require validation**.
- This document **does not constitute** any evidence of, or imply, **efficacy, safety, cross‑species selectivity, reversibility, or field feasibility**; all external communications must comply with Section 8, Evidence & Claims Policy.
- **Version consistency requirement**: When citing or paraphrasing this document, you must include **version number + date**.

Non‑confidential content covered by this document (no numerical thresholds included):
- An auditable phased Gate R&D process;
- A clear deliverables structure and acceptance criteria (expressed as templates/field‑level structures, not slogan‑style statements);
- A governance position for structural risk management of “uncontrolled intake (ad libitum feeding)” and “non‑target exposure”;
- Evidence grading and change control for external claims;
- The external deliverable package structures and field templates for Gate 4/6, the P0 risk minimal‑falsification table, and traceability ID/change‑control templates and flow (all without structure/synthesis/formulation/threshold numbers).

## This document does **NOT** include and will not be distributed externally:

- Chemical structures/SMILES, SAR maps, hit compound lists, synthesis routes, or process details;
- Formulations and content specifications, feeding/dose instructions, or any field‑deployable feeding operation details;
- Raw experimental datasets, full statistical analysis outputs, CRO SOW/quotes, or supplier/specific site information;
- Full‑text papers/PDFs, screenshots, or extracted charts (externally we provide only DOI metadata and publicly verifiable sources).

---

## Table of Contents
- 0. Non‑Confidential Verifiable Checklist
     * Version & Change Log (Non‑Confidential)
- 1. Project Overview (Non‑Confidential)
     * Current Maturity (Dual‑axis: governance maturity vs scientific evidence maturity)
- 2. R&D Process Overview: Phase 0–7 (Auditable Gate Map)
- 3. Process specifics: Freeze→Run→Review→Audit (Standardized closed loop)
- 4. Gate 1 (In vitro closed loop) — deliverables, field dictionary, acceptance criteria (Non‑Confidential)
- 5. Uncontrolled Intake and the “Scenario‑Required Safety Window” (Dose/Exposure Model)
- 6. B Standard governance (health/behavior unchanged): endpoint framework, stop criteria, audit points
- 7. Target species = cat / minimizing non‑target impact: functional selectivity + worst‑case exposure
- 8. Evidence & External Claims Policy (Evidence & Claims Policy)
- 9. Regulatory & ethics path assumptions (Non‑Confidential)
- 10. Supplemental packages available under NDA (scope)
- 11. References (DOI metadata only)
- Appendix A: Gate 1 Standardized Results Table (TSV) Template (field level)
- Appendix B: Gate Decision Memo Template (externally auditable structure)
- Appendix C: Field intake/BW pilot data table template (field level)
- Appendix D: 30‑minute third‑party quick audit checklist (Non‑Confidential)
- Appendix E: Gate 4 (exposure & intake calibration) deliverable structure + Dose Model input templates (field level)
- Appendix F: Gate 6 (controlled feeding, B Standard) deliverable structure + AE/SAE & behavior scoring templates (field level)
- Appendix G: Traceability IDs & change control templates (Non‑Confidential)
- Appendix H: Claims Register template (field level)
- Appendix I: DOI metadata verification record template (field level)

---

# 0. Non‑Confidential Verifiable Checklist

This project is currently in a theoretical/planning phase; the primary value is an **actionable, auditable R&D governance and deliverables system** (not experimental results).

## 0.1 Version & Change Log (Non‑Confidential)

To ensure consistency in external referencing, this document provides a minimal, auditable change log (without any confidential details):

| change_id | from_version | to_version | date | Change summary (non‑confidential) | affected_clm_ids | owner |
|---|---|---|---|---|---|---|
| CHG‑NC‑20260209‑001 | v0.4‑ZH | v0.5‑ZH | 2026-02-10 | Added hard “zero‑data” qualifiers and dual‑axis maturity; completed minimum criteria for cross‑species comparability, minimum auditability standard for field pilots, a formal definition of K_required, an audit‑grade definition of B Standard, and REG‑Gate; corrected placeholder titles in the references table. | policy‑level (global positions/templates) | CTO |
| CHG‑NC‑20260210‑001 | v0.5‑ZH | v0.6‑ZH | 2026-02-10 | Added Claims Register template; froze the rule for selecting the primary exposure metric for K_required; completed minimum category requirements for bridging controls and the mandatory Gate 1 false‑positive exclusion checklist; completed the minimum time‑window structure for B Standard; added DOI metadata verification workflow and record template; added jurisdiction selection principles (category‑level); changed external wording from “cat‑targeting” to “target species is cat (target species) + non‑target governance”. | policy‑level (global positions/templates) | CTO |
| CHG‑NC‑20260210‑002 | v0.6‑ZH | v0.7‑ZH | 2026-02-10 | Implemented audit rules into the field dictionary: added comparability/bridging/false‑positive flags to the results table; froze the Dose Model input dependency structure and primary quantile set; completed Claims Register approval‑chain fields. | policy‑level (global positions/templates) | CTO |
| CHG‑NC‑20260210‑003 | v0.7‑ZH | v0.8‑ZH | 2026-02-10 | To avoid drift in execution‑phase language: completed controlled vocabulary for flags; added `bridging_level` and implemented bridging‑strength grading in the results table; removed the textual conflict between p99 “example wording” and “primary criterion fixed at p99”; removed “no impact on non‑targets” wording from the audit checklist. | policy‑level (global positions/templates) | CTO |
| CHG‑NC‑20260210‑004 | v0.8‑ZH | v0.9‑ZH | 2026-02-10 | Performed pre‑release DOI metadata verification and archived the verification record (public Crossref source); synchronized corrections to reference titles/years with the verification source. | EVD‑NC‑001~013 | CTO |

Within the non‑confidential scope, we have already produced/frozen:

- **Gate map**: purpose, key outputs, and primary stop categories for Phase 0–7 (Section 2).
- **Standardized closed‑loop process**: unified Freeze→Run→Review→Audit wording plus change‑control requirements (Section 3).
- **Gate 1 deliverable structure**: deliverable directory structure and the hard requirement of “raw data + metadata must be delivered” (Section 4.2).
- **Gate 1 results table field dictionary**: a field set for cross‑batch/cross‑CRO aggregation (Section 4.3 + Appendix A).
- **Gate decision memo template**: ensures conclusions, non‑extrapolation boundaries, follow‑up evidence, and stop reasons are auditable (Appendix B).
- **Calibration approach for ad libitum feeding**: external pilot outputs (quantiles) and escalation rules (Section 5.2 + Appendix C).
- **Gate 4 deliverable structure (exposure/intake calibration)**: deliverable directory structure and Dose Model input table templates (Section 5.4 + Appendix E).
- **Gate 6 deliverable structure (controlled feeding)**: AE/SAE event log and behavior scoring templates (Section 6.5 + Appendix F).
- **Traceability IDs & change control templates**: traceable association rules across claims/evidence/Gate decisions (Section 8.5 + Appendix G).
- **B Standard governance framework**: endpoint categories and the principle of “freeze first, then run” for AE/SAE and stop criteria (Section 6).
- **Target species = cat / non‑target governance wording**: cross‑species functional selectivity + worst‑case exposure framework + external claims discipline (Section 7).
- **Evidence grading and external claims policy**: no fabrication, no extrapolation, evidence levels and claim classification (Section 8).
- **Claims Register template**: an executable vehicle for external messaging (Section 8.6 + Appendix H).
- **DOI metadata verification workflow & record template**: publicly verifiable citation trace (Section 8.7 + Appendix I).

---

# 1. Project Overview

Eco Cat Food is an R&D program exploring cat contraception via **small‑molecule antagonism of FSHR (Follicle‑Stimulating Hormone Receptor)**, with cat food considered as a delivery vehicle.

Current status: **purely theoretical/planning phase**.

This non‑confidential technical package does not include any experimental dataset and does not externally claim validated efficacy/safety.

We treat three hard problems as engineering constraints that must be governed by process:
1) **Uncontrolled intake**: individual variation in food intake and body weight leads to a wide exposure range;
2) **B Standard as a co‑primary**: contraceptive effect must be met together with “no clinically significant adverse health/behavior signal”;
3) **Target species = cat / non‑target exposure**: the feeding modality cannot fully avoid exposure of male cats and non‑target species, so cross‑species functional selectivity must be quantified early, and safety must be governed under a worst‑case exposure framework.

## 1.1 Current maturity (dual‑axis: governance maturity vs scientific evidence maturity)

To prevent outsiders from misreading “process maturity” as “science has been validated”, we decompose project maturity into two independent axes:

- **Governance/Audit maturity (G‑Maturity)**: whether the Gate map, deliverable structures, field dictionaries, evidence grading, change control, and audit closed loop exist as a coherent, executable system at the document level.
- **Scientific evidence maturity (S‑Maturity)**: whether there is reviewable in vitro/in vivo data supporting key conclusions on efficacy, safety, cross‑species selectivity, reversibility, and field feasibility.

Within the non‑confidential scope, our statements are limited to: **G‑Maturity has an auditable design and templates**, while **S‑Maturity is currently “zero data, pending validation”**.

Current status (as of 2026-02-10):
- G‑Maturity: a Phase 0–7 governance framework and key deliverable templates have been established (this document + appendices).
- S‑Maturity: **0 (zero experimental data)**. Any scientific statement must be framed only as a hypothesis to be tested; we do not externally imply “validated / close to deployment”.

---

# 2. R&D Process Overview: Phase 0–7 (Auditable Gate Map)

We progress via “milestone freezing (freeze the rules first) + staged Gate reviews”.

This external version describes go/stop logic only at the **category level**; any content involving numerical thresholds is provided only under NDA.

## 2.1 Gate map (non‑confidential)

| Phase | Purpose | Key outputs | Primary stop reasons (category) |
|---|---|---|---|
| 0 Governance/Audit | Prevent wording drift and non‑auditable data | Evidence levels & claim types; data delivery standards; change control | Unable to provide raw data / non‑reviewable deliverables |
| 1 Literature skeleton | Rewrite “claims” into “testable hypotheses” | DOI metadata list; hypothesis → minimum evidence mapping | High‑risk claims being communicated externally as conclusions |
| 2 Freeze Gate 1 execution package (theoretical) | Avoid “do chemistry first, then look for readouts” | Gate 1 question list; deliverable structure; QC categories; go/stop rules (category) | Gate 1 cannot form a closed loop (potency/mechanism/selectivity/false‑positive exclusion) |
| 3 Gate 1 in vitro data | Establish an auditable in vitro closed loop | Functional antagonism, mechanism classification, cross‑species functional selectivity, false‑positive filtering data package | Signal not reproducible; suspected false positives; insufficient cross‑species separation |
| 4 Exposure & intake calibration | Turn “ad libitum feeding” into a computable constraint | Intake/BW distribution (quantiles); mixed‑feeding exposure calibration; scenario‑required safety window (K_required) | Scenario‑required safety window far beyond achievable range |
| 5 Hit→Lead / optimization | Drive chemistry iterations with data | Iteration loop (objective function/stop rules); candidate prioritization | Cannot reach the selectivity/robustness required to enter higher‑risk phases |
| 6 Controlled small‑sample feeding | Validate B Standard and reversibility hypotheses | Controlled feeding safety/behavior package design and audit results | B Standard shows unacceptable adverse signals |
| 7 Field pilot | Validate scenario feasibility and auditability | Field pilot design, contamination/missingness governance, auditable results report | Field inference non‑auditable / severe contamination |


## 2.2 P0 risks and minimum falsification (non‑confidential)

The table below binds the most critical structural risks (P0) to the minimum falsification / supporting evidence actions, aiming to decide early whether this approach is worth continued investment under ad libitum feeding and non‑target exposure constraints.

| Risk (P0) | Why it is P0 | Minimum falsification / supporting evidence (category) | Stop/escalation triggers (category) |
|---|---|---|---|
| Uncontrolled intake makes K_required too large | Potentially structurally infeasible | Field pilot produces intake/BW quantiles and back‑feeds the Dose Model for scenario analysis | If K_required clearly exceeds achievable range: stop, or change scenario constraints |
| Insufficient cross‑species functional selectivity | Non‑target ingestion/contact chain cannot be closed | Same‑platform functional readouts for cat/dog/human FSHR + related receptor counterscreens | If stable separation cannot be achieved in a comparable system: stop or escalate to stricter verification/alternative strategy |
| B Standard fails (health/behavior) | Co‑primary failure ⇒ NoGo | Controlled small‑sample feeding: AE/SAE + behavior scoring (blinding preferred) | If clinically significant adverse signals appear: stop or return to mechanism/exposure control |
| Exposure risk for special populations (kittens/pregnant/lactating) | Field exposure hard to exclude | Strictly downgrade relevant statements to hypotheses; freeze monitoring/stop rules and minimum supporting evidence before field entry | If auditable risk governance and supporting evidence path cannot be defined: no field entry |
| Reversibility / recovery after stopping is inadequate | Determines product profile and compliance risk | Predefine reversibility criteria (category) and verify during controlled feeding | If predefined criteria cannot be met: adjust target or stop |
| Field inference not auditable (missingness/contamination/identification) | Even if done, conclusions may be unreliable | Pilot rehearsal of identification/loss‑to‑follow‑up/contamination governance + freeze missingness & contamination rules | If missingness/contamination cannot be controlled in an audit sense: no field entry |
| Content variability/stability causes exposure spikes | Amplifies worst‑case exposure risk | Verification plan and release rules for quality/uniformity/stability (category) | If an auditable QC window cannot be defined: no field entry |

Note: Detailed field templates for P0 risks are provided in Appendices C/E/F; numerical thresholds are provided only under NDA.


---

# 3. Process specifics: Freeze→Run→Review→Audit (Standardized closed loop)

Externally, “process” often conflates three workflows: R&D workflow, feeding/exposure governance workflow, and evidence/audit workflow. We solidify all of them using the same four‑step closed loop:

## 3.1 Freeze (freeze the rules first)
Before each Gate starts, freeze:
- **Question list**: what must be answered in this phase;
- **Deliverable structure**: directories/tables/fields of the package (audit‑friendly and outsource‑acceptance‑friendly);
- **QC and data acceptability**: which data are exploratory only vs which can support go/no‑go decisions;
- **Category logic for go/stop**: categories of conditions that trigger stop / additional work / repeat / escalation;
- **Change control**: any change must record “reason, impact assessment, approver, version”.

## 3.2 Run (execute per the frozen plan)
Hard requirements during execution (third‑party auditable design principles):
- **Raw data must be delivered**: e.g., raw per‑well plate readouts, plate maps, timestamps, analysis software version and fitting parameters;
- **Reproducibility by design**: include validation across independent experiment days/batches;
- **Controls and counterscreens**: design false‑positive filtering and related receptor/pathway interference checks in parallel;
- **Cross‑species comparability**: cross‑species comparisons should use comparable formats to reduce “false selectivity due to incomparability”.

## 3.3 Review (standardized Gate review outputs)
Each Gate review output is one of:
- **Pass**: proceed to the next Gate;
- **Conditional Pass**: proceed only after predefined add‑on evidence / repeats / mechanism clarification;
- **Stop**: stop further investment; reasons must map to the frozen stop categories.

The review record must include:
- the phase conclusion (pass/conditional/stop) and evidence level;
- non‑extrapolation boundaries (what conclusions cannot be drawn from these data);
- minimum prerequisites for the next phase (minimum add‑on evidence).

## 3.4 Audit (how a third party can review)
Minimum requirements to be third‑party‑review‑friendly:
- the deliverable package contains a `README` (data dictionary, version, generation steps);
- key tables use diff‑friendly TSV/CSV;
- traceable links exist between data and conclusions (e.g., results table fields → QC → decision memo).


## 3.5 Process flow (text version)

Each Gate is executed as a closed loop: Freeze→Run→Review→Audit:

Freeze (question list / deliverable structure / QC & stop logic)
  → Run (generate raw data + metadata, produce a standardized results table)
  → Review (Gate decision memo: Pass / Conditional Pass / Stop)
  → Audit (third‑party review: data dictionary, version, traceability links, change control)

Relationship between phases and Gates (high level):

- Phase 0/1: governance and evidence system (external claims discipline)
- Gate 1: in vitro closed loop (potency/mechanism/selectivity/false‑positive exclusion)
- Gate 4: intake/BW and exposure calibration → K_required (scenario constraint)
- Gate 6: controlled feeding to validate B Standard and reversibility (only after data support)
- Gate 7: field pilot (auditability as a prerequisite)

---

# 4. Gate 1 (In vitro closed loop) — deliverables, field dictionary, acceptance criteria (Non‑Confidential)

The goal of Gate 1 is to establish a minimal, auditable in vitro closed loop, preventing “starting chemical optimization without reproducible readouts”.

## 4.1 Four categories of questions Gate 1 must answer
1) **Potency**: is there a reproducible functional antagonism signal on cat FSHR?
2) **Mechanism**: can we distinguish competitive/orthosteric vs allosteric/non‑competitive mechanisms?
3) **Cross‑species functional selectivity**: does a reproducible functional separation exist between cat vs non‑target species (at least dog/human)?
4) **False‑positive exclusion**: are toxicity/assay interference/pathway interference systematically ruled out?

## 4.1.1 Minimum frozen criteria for cross‑species “comparability” (category‑level, non‑confidential)

To avoid “false selectivity due to incomparability”, any cross‑species functional comparison used for external messaging or Gate decisions must meet the following **methodological category** requirements (no numerical thresholds):

- **Same platform / same primary readout**: cat/dog/human use the same class of functional readout platform (e.g., the same cAMP readout class), and share the same data processing and curve‑fitting workflow.
- **Frozen stimulation conditions**: rules for stimulus ligand/dose setting must be frozen; if different ligands or agonist strengths are required across species, **bridging controls** must be provided to prove comparability (otherwise the comparison must not be used for selectivity claims).
- **Expression and system recording**: record category information on receptor constructs, expression system, and expression level; avoid apparent selectivity driven solely by overexpression/system differences.
- **In‑plate / inter‑batch bridging controls**: each batch includes comparable positive/negative controls and reference compounds (for drift monitoring and inter‑batch bridging).
- **Consistent QC grading**: QC criteria are consistent across species; any result that does not reach “decision‑grade data” must not be used for selectivity conclusions.
- **Bias handling**: if key deviations exist (platform/stimulation/system/analysis workflow inconsistency), they must be flagged in the results table as `qc_grade != decision‑grade` or `comparability_flag = not_comparable` (field names can be further refined under NDA), and must trigger escalation verification rather than direct progression.

## 4.1.2 Minimum category requirements for bridging controls (non‑confidential)

Cross‑species comparability must be operationalized via auditable “bridging controls”. Minimum frozen requirements (category‑level) within the non‑confidential scope:

- **Reference compound bridging**: include at least 1 cross‑species shared reference compound to monitor system drift and support inter‑batch/plate bridging (the compound identity need not be disclosed externally).
- **Control bridging**: each batch includes positive/negative controls and key concentration points/curves for the reference compound (category‑level) to judge whether “this batch is eligible for cross‑species comparison”.
- **Bridging strength grading** (strong → weak):
  1) same‑day, same‑plate cross‑species bridging (ideal; minimal drift);
  2) same‑day cross‑plate bridging (requires recording plate‑to‑plate calibration and batch metadata);
  3) different‑day bridging (allowed only with stable reference and QC records; must be interpreted conservatively).
- **Mandatory `not_comparable` conditions (category‑level)**: if any of the following occurs, cross‑species comparison for that batch must be flagged `not_comparable` and must not be used for “selectivity” claims:
  - missing bridging controls (reference compound or key controls missing);
  - bridging controls fail the frozen QC category requirements;
  - key deviations in stimulation conditions/analysis workflow without effective bridging proof of comparability.

## 4.1.3 Mandatory Gate 1 false‑positive exclusion checklist (category‑level, non‑confidential)

To avoid “looks effective but is actually an assay artifact” mis‑progression, Gate 1 false‑positive exclusion must include at least the following **mandatory check categories** (no specific thresholds or operational details):

- **Cell/system toxicity and activity decline trends** (within the same system as the primary readout or a bridgeable system);
- **Assay interference** (e.g., luminescence/fluorescence/reporter/readout interference categories);
- **Sample physicochemical issues** (solubility, precipitation/crystallization, aggregates/micelles, etc. as categories that may cause false signals);
- **Non‑specific pathway perturbation / membrane disruption effects** (category risks that may appear as antagonism);
- **Chemical alert structure categories** (reactive / false‑positive‑enriched fragments, etc.; only category labeling and disposition principles are provided here, not specific structure rules).

Frozen escalation/stop positions (category‑level):
- If any mandatory item shows a “high‑risk signal” → the data must not be treated as decision‑grade evidence; it must trigger a second readout/orthogonal verification or a stop;
- If escalation verification cannot clarify → flag as `invalid` and stop, or return to rebuild chemistry/system fundamentals.

## 4.2 Gate 1 deliverable package

We do not provide data externally, but we can specify the deliverable package structure (for outsource acceptance and audit):

- `Gate1_Deliverable_Package/`
  - `README.md` (version, experiment batches, data dictionary, generation steps)
  - `Protocols/` (brief version: experiment overview, controls, QC category metrics; detailed numerical thresholds are in the NDA version)
  - `RawData/` (raw per‑well readouts, plate maps, timestamps; export tables or controlled formats)
  - `Analysis/` (curve‑fitting parameters, software versions, fitting strategy notes)
  - `QC/` (QC summary table: which data are decision‑grade vs exploratory vs invalid)
  - `Results/` (standardized results TSV: compound × experiment × species/receptor/readout)
  - `Decision/` (Gate 1 decision memo: pass/conditional/stop and reasons)

## 4.3 Example standardized results table (TSV/CSV) fields (non‑confidential)
To enable aggregation across batches and CROs, the results table should include at least the following fields (excluding any chemical structure):
- `compound_id`: compound identifier (de‑identified ID)
- `batch_id`: batch/source (may be anonymized)
- `assay_id`: assay identifier
- `species`: cat/dog/human/other
- `target`: FSHR/LHR/TSHR/…
- `cell_system`: brief system description (category level is sufficient)
- `readout`: primary readout type (e.g., cAMP/other)
- `mode`: antagonism / counterscreen / toxicity / interference
- `concentration_unit`: concentration unit
- `ic50` / `pIC50`: potency metric (if data are qualified)
- `e_max`, `hill_slope`: curve parameters (if qualified)
- `fit_quality`: fit quality category (e.g., good/acceptable/poor)
- `qc_grade`: data qualification grade (e.g., decision‑grade / exploratory / invalid)
- `replicate_n`, `independent_day_n`: replicate information
- `comparability_flag`: cross‑species comparability flag (comparable / partial / not_comparable)
- `bridging_control_present_yes_no`: whether bridging controls are present (Y/N)
- `bridging_level`: bridging strength level (1/2/3/NA; definitions in Appendix A)
- `bridging_qc_grade`: bridging control QC category (good / acceptable / poor / missing)
- `interference_flag`: assay interference risk flag (none / suspected / confirmed / not_assessed; Appendix A)
- `aggregation_flag`: aggregation/physicochemical false‑positive risk flag (none / suspected / confirmed / not_assessed; Appendix A)
- `cytotoxicity_flag`: cytotoxicity/activity decline risk flag (none / suspected / confirmed / not_assessed; Appendix A)
- `notes`: anomaly notes (e.g., suspected interference / cytotoxicity trend)

## 4.4 Mechanism classification and “second readout” trigger (non‑confidential position)

- If evidence suggests an allosteric/non‑competitive mechanism or a risk of biased signaling, require an additional **second class of readout** (non‑cAMP) to reduce the probability of mis‑progression driven by a single readout.
- The selection and thresholds for the second readout are frozen in the NDA version; externally we commit only that “triggers and an escalation verification path exist”.

## 4.5 Gate 1 stop categories (non‑confidential)
- Not reproducible: consistent antagonism signal cannot be replicated across batches/days;
- High false‑positive risk: toxicity/interference/non‑specific pathway perturbation cannot be excluded;
- Insufficient cross‑species separation: in a comparable format, cat vs non‑target species cannot form sufficient separation (early exploration is allowed, but stricter standards must be met before higher‑risk phases);
- Mechanism risk: mechanism indicates higher systemic risk and cannot be de‑risked via escalation verification.

## 4.6 Gate 1 QC metric categories (metric names public; thresholds under NDA)
- **Assay window**: Z' factor (or equivalent), signal window / SNR (S/B, S/N), control stability;
- **Repeatability**: variability of controls/key points (CV‑type metrics), consistency across independent experiment days;
- **Curve quality**: convergence, reasonable plateau/slope, systematic bias checks;
- **False‑positive filtering**: cytotoxicity/activity decline trends, assay interference (e.g., luminescence/fluorescence/reporter interference investigation paths), non‑specific pathway perturbation;
- **Sample quality**: record and disposition for solubility/precipitation/aggregation tendency (category level).

---

# 5. Uncontrolled Intake and the “Scenario‑Required Safety Window” (Dose/Exposure Model)

## 5.1 Why modeling must come first
Ad libitum feeding means individual exposure depends on:
- distribution of food intake (even within the same site, the spread can be large);
- distribution of body weight;
- content variability of the active ingredient in food;
- individual differences in absorption/clearance (PK variability).

Therefore, we do not treat “average intake” as an acceptable safety basis; we use high‑end consumers (quantiles) to drive the “scenario‑required safety window”.

## 5.2 Minimal field pilot (non‑confidential framework)
The purpose is not to prove efficacy, but to calibrate input distributions so the model becomes computable:
- Output: distribution features of intake and body weight (recommended at least p10/p50/p90/p99), with site differences and uncertainty recorded;
- Quality requirements: methods repeatable, data auditable, clear handling for missingness and error;
- Escalation rule: if high‑end quantiles cannot be stably obtained, automatically escalate measurement methods (e.g., from site‑level to rough individual‑level estimation).

### 5.2.1 Minimum frozen auditability standard for field pilots (category‑level, non‑confidential)

The field pilot aims to “calibrate distributions”, so auditability must be prioritized (otherwise quantile outputs are not trustworthy and cannot back‑feed the model). Within the non‑confidential scope, we freeze the following minimum rule categories:

- **Grading of identification/repeated‑measurement methods**: site‑level counting is only for coarse calibration; if frozen high‑end quantiles (p99) cannot be produced or site differences cannot be explained, methods must be escalated to repeatable individual identification (video ID / tagging are optional categories). Otherwise, pilot outputs must not be used for Gate decisions.
- **Predefined handling of missingness and error**: missingness causes and mechanisms must be categorized (e.g., device/observation missingness, unidentifiable individuals, extreme weather) and category‑level sensitivity analysis strategies must be frozen to avoid post‑hoc explanations.
- **Contamination event logging**: any event categories that make exposure non‑attributable (e.g., cross‑site migration, external feeding, intervention interruption) must be logged and enter the audit chain; severe contamination should trigger escalation or stop rather than being ignored post‑hoc.
- **Versioning and traceability**: measurement workflows, identification methods, and data processing scripts/rules must be versioned; key version changes must follow change control and document impacts on quantile comparability.

## 5.3 External definition of “scenario‑required safety window (K_required)”
- **Purpose**: translate the engineering constraint of “ad libitum feeding” into a computable, auditable **minimum required safety window** for early go/no‑go (not an average‑value narrative).
- **Inputs (distributions/uncertainty)**:
  - in vitro potency (as a starting point for target exposure/occupancy, with a prior range of “effective multiple factors”);
  - distributions of intake and body weight (at least to high‑end quantiles);
  - active‑ingredient content variability in food (within‑batch / between‑batch);
  - variability of key PK parameters (absorption/clearance/protein binding, expressed as prior distributions).
- **Formal definition (no numbers)**:
  - Define an “effective exposure target” `C_target` (e.g., target free concentration linked to in vitro functional antagonism; specific multiples are provided only under NDA).
  - Under a given feeding scenario and input distributions, the model generates an exposure distribution `C` (or `C_avg`/`C_max`, etc., per the frozen position; one or multiple may be output).
  - **K_required** is defined as the minimum safety‑window multiple required of a candidate molecule to keep high‑end exposures within a manageable range. Externally, we use one of two equivalent, auditable reporting conventions:
    1) **Quantile convention**: `K_required(p) = Q_p(C) / C_target` (where `p` is the frozen high‑end quantile: this document freezes Gate 4’s primary criterion at `p99`, and requires at least reporting `p90` as sensitivity; it also freezes which `C` metric is used).
    2) **Worst‑case combination convention**: `K_required^WC = max(C | key inputs take conservative upper‑bound combinations)`, then normalize as `K_required^WC / C_target` (to provide an upper‑bound warning line).
- **Rule for selecting the primary exposure metric (category‑level; frozen to prevent selective reporting)**:
  - Must compute and report at least two classes of `K_required`: one based on `C_avg` (or a time‑integrated metric such as AUC) and one based on `C_max` (peak metric).
  - Gate 4’s decision primary criterion defaults to the **more conservative (larger)** of the two, preventing “choose C_avg when favorable, choose C_max when unfavorable”.
  - If mechanism/risk assessment requires a single primary metric (e.g., clearly peak‑driven or time‑integral‑driven), the trigger categories must be specified in Freeze via change control, and the decision memo must record `change_id` and an impact assessment.
- **Frozen position for input dependency structure / correlation handling (category‑level; prevent arbitrary assumptions)**:
  - Default: if the field pilot and PK data support paired observations for the same individual, prioritize **data‑estimated correlation/dependency structure** (recording method version and uncertainty in outputs).
  - If only marginals exist without paired observations, both must be provided:
    1) results under the **independence assumption** (baseline);
    2) results under a **conservative dependence assumption** (upper‑bound sensitivity), with Gate decisions defaulting to the more conservative outcome.
  - Escalation triggers (category‑level): if the independence vs conservative dependence assumption materially changes Gate conclusions (e.g., decision flips), then the data collection must be upgraded to obtain paired observations / estimate dependency; otherwise no progression to higher phases.
- **Frozen quantile set for the primary criterion (category‑level; avoid post‑hoc quantile choice)**:
  - Gate 4 must report `K_required(p)` for the frozen high‑end quantile set (at least `p90` and `p99`), and also report `K_required^WC` (worst‑case convention).
  - Gate 4’s primary criterion defaults to `p99` (and uses the more conservative of the `C_avg` and `C_max` conventions); `p90` is for scenario sensitivity and communication support, not a substitute for the primary criterion.
  - If `p99` cannot be stably estimated in an audit sense (insufficient sample/identification), the measurement method must be escalated per 5.2; before that is met, a lower quantile must not be used as a substitute to progress.
- **Outputs should include**: `K_required` (per frozen conventions), sensitivity ranking of key inputs, and a category‑level determination of “structurally infeasible / must change scenario constraints”.

If K_required materially exceeds what can reasonably be expected as a safety window from biological and PK perspectives, the conclusion is not “run bigger studies”, but **structural stop or mandatory changes to scenario constraints** (e.g., change the exposure distribution, change delivery controllability).


## 5.4 Gate 4 deliverable package structure (exposure & intake calibration; non‑confidential)

Purpose of Gate 4: make the “ad libitum feeding” constraint explicit, and produce auditable input distributions and scenario analysis output structures for updating the Dose/Exposure Model (no numeric values disclosed externally).

Externally describable deliverable structure:

- `Gate4_Deliverable_Package/`
  - `README.md` (version, data dictionary, generation steps)
  - `Intake_BW_Pilot/` (methods overview, quantile outputs, missingness/error handling; template in Appendix C)
  - `Exposure_Calibration/` (mixed‑feeding exposure calibration design overview, sample list template; template in Appendix E)
  - `DoseModel/` (input table templates, scenario definitions, sensitivity analysis output structures; template in Appendix E)
  - `QC/` (data qualification and audit points)
  - `Decision/` (Gate 4 decision memo; template in Appendix B)

One of the key outputs of Gate 4 is K_required (the order‑of‑magnitude requirement of the scenario‑required safety window), used to decide whether to enter higher‑cost phases or field pilots.

---

# 6. B Standard governance (health/behavior unchanged): endpoint framework, stop criteria, audit points

B Standard is defined as a co‑primary requirement alongside efficacy:
- **Efficacy (reduced fertility)** and **B Standard (no clinically significant adverse health/behavior signal)** must both be met.

## 6.1 B Standard endpoint framework (non‑confidential)
- Health endpoints (categories): body weight/body condition, appetite and drinking, mental state, basic vitals, observable discomfort/pain signals;
- Behavior endpoints (categories): activity/exploration, aggression/territorial behaviors, social withdrawal/stress, sleep and abnormal behaviors;
- Reproduction‑related endpoints (categories): estrus‑related behavior phenotypes; reversibility observation windows (as part of the product phenotype).

## 6.2 AE/SAE and stop logic (non‑confidential)
- Predefine AE/SAE grading and escalation paths;
- Freeze stop criteria before execution; do not modify post‑hoc during execution;
- Conditional pass and add‑on evidence must have explicit lists (e.g., repeats, mechanism clarification, additional monitoring).

## 6.3 Boundary position for “some hormone changes may be allowed” (non‑confidential)
- We do not require “hormones must remain completely unchanged” as a premise.
- For example, luteal‑phase/progesterone pattern changes may occur mechanistically; acceptability depends on whether **systemic adverse consequences** are introduced, and must be governed via frozen monitoring and stop criteria.

## 6.4 “Audit‑grade definition” of B Standard (non‑confidential)

Externally, what B Standard can commit to is **methodology and governance**, not “results will definitely be unchanged”. Therefore, we freeze the minimum auditable definition of B Standard into the following category elements (no numerical thresholds):

- **Versioned behavior scoring tools**: use an explicit ethogram/scale (version, training materials, scoring guidance) and embed it into Protocols and the data dictionary; any version change must follow change control and assess impact on historical comparability.
- **Observer training and consistency**: perform training and consistency sampling before formal scoring (freeze category criteria for inter‑rater reliability and retraining triggers); continue sampling and review during scoring to prevent drift.
- **Blinding preferred**: behavior scoring and key interpretation should be blinded whenever possible (at least blinded to group allocation); if blinding is not possible, record the reason and add independent review and bias controls.
- **AE/SAE dictionary and attribution workflow**: maintain an AE/SAE event dictionary, grading conventions, and escalation paths; establish an auditable chain of “report → grade → attribute → adjudicate → action (stop/add‑on/continue)”, and record adjudicator role and version.
- **“Clinical significance” decision workflow**: avoid post‑hoc narrative; ensure reviewable conclusions via a frozen decision workflow (trigger categories + review mechanism + decision record templates).
- **Data traceability and reviewability**: traceable linkage between raw behavior materials (e.g., videos/timestamps/metadata) and scoring tables; missingness and anomalies must be categorized and explained per frozen positions.

### 6.4.1 Minimum time‑window structure (category‑level, non‑confidential)

To avoid narrative “reversibility/recovery”, controlled studies relevant to B Standard must freeze a minimum time structure (no day counts; structure and principles only):

- **Baseline**: collect pre‑intervention health and behavior baselines (same scale/same observation workflow) for within‑subject comparison and change interpretation.
- **Intervention**: execute intervention under controlled conditions and continuously monitor AE/SAE and behavior endpoints; any deviations enter the deviation log.
- **Follow‑up / recovery**: after stopping intervention, track recovery trends and potential delayed adverse signals at pre‑frozen observation point categories; serves as the audit basis for whether the “reversibility hypothesis” still holds.

Rule: if real‑world constraints require changing the time structure or observation point categories, it must be handled via change control in Freeze, and `change_id` plus comparability impact assessment must be recorded in the Gate decision memo.


## 6.5 Gate 6 deliverable package structure (controlled feeding: B Standard & reversibility; non‑confidential)

Purpose of Gate 6: validate the B Standard governance framework and reversibility hypothesis under controlled conditions, and produce an auditable safety/behavior data package (raw data not publicly disclosed externally).

Externally describable deliverable structure:

- `Gate6_Deliverable_Package/`
  - `README.md` (version, data dictionary, generation steps)
  - `Protocol_Summary/` (endpoint categories, blinding/randomization principles, AE/SAE grading and stop categories)
  - `Event_Log/` (AE/SAE event log template; Appendix F)
  - `Behavior_Scoring/` (behavior scoring templates and consistency assessment positions; Appendix F)
  - `Lab_Observations/` (health indicator category list and observation record templates; non‑confidential positions)
  - `QC/` (data qualification and deviation records)
  - `Decision/` (Gate 6 decision memo; Appendix B)

---

# 7. Target species = cat / minimizing non‑target impact: functional selectivity + worst‑case exposure

Because the feeding modality cannot fully segregate exposure by sex and cannot fully prevent non‑target ingestion, we interpret “target species is cat (target species)” as a **testable requirement**, and treat “no impact on non‑targets” as a **high‑risk claim prohibited from extrapolation** (unless supported by a strong evidence closed loop).
- **Cross‑species functional selectivity**: quantify functional separation of cat vs non‑target species early in comparable assay formats;
- **Worst‑case exposure governance**: do not use average exposure as the safety basis; constrain by high‑end consumers and accidental ingestion scenarios;
- **External claims discipline**: when evidence is insufficient, do not claim “no impact on other species”; explicitly state it as a hypothesis pending validation.

---

# 8. Evidence & External Claims Policy (Evidence & Claims Policy)

## 8.1 Core rules
- **No fabrication**: do not present hypotheses/inference as measured results.
- **No extrapolation**: any key statement must state “evidence level + non‑extrapolation boundary”.

## 8.2 Evidence levels (external position)
- **Strong**: directly relevant, reproducible, with clear extrapolation boundaries;
- **Medium**: publicly verifiable but with species/mechanism/scenario differences;
- **Weak**: background/review; not used for key go/no‑go.

## 8.3 Claim types (must be labeled externally)
- **Conclusion**: supported by strong evidence within the stated boundaries;
- **Hypothesis**: reasonable but unproven; must include “minimum supporting evidence”;
- **Goal**: desired profile; not a statement of reality.

## 8.4 External red lines (examples)
The following statements must be treated as hypotheses until strong evidence exists:
- “Does not affect behavior/health”
- “Safe for kittens/pregnant/lactating cats”
- “No impact on other species”


## 8.5 Traceability IDs & change control (non‑confidential)

- `CLM-###`: external key statement (conclusion/hypothesis/goal) ID
- `EVD-###`: evidence item ID (can be linked to DOI metadata)
- `GATE{n}-DM-YYYYMMDD-###`: Gate decision memo ID
- `TPL-###`: template/field dictionary version ID (e.g., Appendices A/C/E/F/G)
- `RISK-P0-###`: P0 risk item ID (Section 2.2)

## 8.6 Claims Register (non‑confidential)

Numbering rules alone (CLM/EVD) are insufficient to prevent “external red lines” from drifting in PPTs/emails/meeting notes; therefore, we require a **Claims Register** as the executable vehicle to govern external messaging.

What can be disclosed in the non‑confidential scope is the **register structure and fields** (no confidential conclusions/data):
- Minimum field template: Appendix H
- Rule: any external statement must have a corresponding `clm_id` in the register and explicitly state its `claim_type` (conclusion/hypothesis/goal), evidence level, non‑extrapolation boundary, and forbidden extrapolations; otherwise it must not be communicated externally.
- Approval chain (non‑confidential auditable elements): before setting a claim status to `approved_for_external`, `approved_by_role`, `approved_at`, and `review_checklist_version` must be filled (demonstrating a checklist‑based review, not verbal decisions).

## 8.7 DOI metadata verification workflow (non‑confidential)

To satisfy the audit requirement of “DOI metadata only, publicly verifiable sources”, we execute a minimal pre‑release verification workflow (no full‑text papers):

- **Objects to verify**: every DOI in Section 11 and in `04-References.NC.tsv/.csv`.
- **Verifier**: not the author (role can be a team member/legal/external advisor; record role only).
- **Verification source**: Crossref or the publisher landing page (either is acceptable; must record the source URL).
- **Verification output**: record whether `doi / title / venue / year` match; if not, correct or remove; and write into the verification record table (Appendix I).
- **Execution in this version**: v0.9 has executed the workflow above, with records archived as `05-DOI-Verification.NC.tsv/.csv` (same names in the external directory); summary in Appendix I.

---

# 9. Regulatory & ethics path assumptions (non‑confidential)

The concept of “small‑molecule FSHR antagonism contraception delivered via cat food” may touch multiple regulatory boundaries in most jurisdictions. As we are currently in a zero‑data stage, this section provides only **non‑confidential path assumptions and gate‑based governance positions**, without any actionable feeding details.

## 9.1 Why this must be front‑loaded
- **Regulatory classification may determine ‘scientifically feasible but regulatorily impossible’**: e.g., veterinary drug / medicated feed / bait, etc., with drastically different data packages and distribution control requirements.
- **Non‑target exposure and human contact chain are structural constraints**: ad libitum feeding cannot fully avoid exposure of male cats and non‑target animals; regulatory assessments typically require auditable arguments for non‑target and environmental risks.

## 9.2 Non‑confidential frozen position for “compliance gate (REG‑Gate)”
Before any field pilot (Gate 7), the following **minimal compliance package** must be formed and frozen (category‑level, no agency‑specific details/thresholds):

1) **Target jurisdiction and candidate regulatory pathway**: identify the launch jurisdiction (country/region) and candidate classification (e.g., animal drug / medicated feed / other), and record selection rationale and alternative pathways.
2) **Non‑target and environmental risk module**:
   - enumerate non‑target exposure scenarios (companion animals / wildlife / human contact chain, etc.);
   - risk‑control hypotheses (category‑level positions for packaging/distribution controls/use‑scenario constraints);
   - bind to Gate 1/4 evidence: cross‑species functional selectivity data and worst‑case exposure governance (K_required) must be upstream inputs, not post‑hoc additions.
3) **Animal welfare and ethics governance**: ethics approval pathway, AE/SAE monitoring and reporting, and stop criteria and clinical care principles (category‑level) must be frozen before execution.
4) **Data integrity and auditability**: raw data retention, deviation management (deviation log), change control, and third‑party review interfaces must be executable.

## 9.3 Stop rules (regulatory/ethics dimension)
If an auditable regulatory/ethics path assumption cannot be formed in the target jurisdiction, or the “non‑target/environmental risk” module cannot be bound into a closed loop with Gate data, the conclusion is not “run field studies first”, but: **do not enter the field phase (Gate 7)**, and return to rebuild scenario constraints / delivery control strategies.

## 9.4 Principles for selecting the launch jurisdiction and reset conditions (category‑level, non‑confidential)

To avoid post‑hoc narratives (“pick a jurisdiction first, then justify later”), we freeze category‑level principles for selecting the launch jurisdiction (we do not disclose specific countries/regions; we disclose only the decision logic framework):

| Decision dimension | Selection principle (category‑level) | Action if not met (category‑level) |
|---|---|---|
| Regulatory classification clarity | Candidate pathway (animal drug / medicated feed / other) has clear definitions and actionable precedents/guidance in that jurisdiction | Long‑term ambiguity → pause field planning; complete Gate 1/4 evidence loop first and re‑evaluate |
| Controllability of distribution and use scenario | Able to propose an auditable governance hypothesis for “distribution control/labeling/use boundaries” (even category‑level) | Cannot propose a controllable hypothesis → not a launch jurisdiction, or must rebuild delivery/scenario constraints |
| Non‑target/environmental risk requirement strength | Requirement strength matches the evidence path the project can bear, and can be mapped to Gate 1/4/6 deliverables | Cannot map or cost not bearable → switch pathway or stop |
| Animal welfare/ethics executability | Ethics approval and AE/SAE governance chain can be implemented and audited | Cannot form an auditable ethics path → no field/controlled study phases |
| Data integrity and third‑party review interface | Meets basic requirements for raw data retention/audit/third‑party review | Cannot meet → do not enter high‑cost phases (especially field) |

Reset condition examples (category‑level):
- the candidate pathway changes fundamentally (classification shifts from A to B);
- external audit concludes “distribution control/non‑target risk governance hypothesis is not auditable”;
- Gate 4 outputs show K_required is structurally infeasible, invalidating regulatory pathway assumptions.

---

# 10. Supplemental packages available under NDA (scope)
After signing an NDA, we can provide more detailed “actionable/auditable” materials, including:
- specific numerical thresholds, QC gates, and stop rules for Gate 1/2/…;
- more detailed SOPs, quality systems, and outsourcing acceptance standards;
- SAR and chemistry iteration strategies at structure/series level;
- specific Dose/Exposure Model inputs/outputs, sensitivity and scenario analyses;
- detailed execution modules and animal welfare/ethics compliance modules for field/controlled feeding studies.

---

# 11. References (DOI metadata only)

| DOI | Title (as published) | Year | Journal/Conference | Evidence level | Notes (non‑confidential) |
|---|---|---:|---|---|---|
| 10.1016/j.theriogenology.2024.06.005 | Antibody fragments targeting the extracellular domain of follicular stimulating hormone receptor for contraception in male dogs and cats | 2024 | Theriogenology | Medium | Precedent for species‑specific binding (not evidence of small‑molecule efficacy). |
| 10.1021/jm049676l | Identification of substituted 6-amino-4-phenyltetrahydroquinoline derivatives: potent antagonists for the follicle-stimulating hormone receptor | 2005 | Journal of Medicinal Chemistry | Medium | Precedent for small‑molecule FSHR antagonism (scaffold‑level anchor). |
| 10.1210/en.2018-00317 | Allosteric Regulation of the Follicle-Stimulating Hormone Receptor | 2018 | Endocrinology | Medium | Consideration for allosteric regulation / biased signaling. |
| 10.3389/fendo.2018.00757 | Small Molecule Follicle-Stimulating Hormone Receptor Agonists and Antagonists | 2019 | Frontiers in Endocrinology | Medium | Review of small‑molecule modulators and methodological constraints. |
| 10.1016/j.mce.2016.07.013 | Profiling of FSHR Negative Allosteric Modulators on LH/CGR Reveals Biased Antagonism with Implications in Steroidogenesis | 2016 | Molecular and Cellular Endocrinology | Medium | Principles for biased antagonism and cross‑receptor profiling. |
| 10.1016/j.mce.2010.12.023 | A negative allosteric modulator demonstrates biased antagonism of the follicle stimulating hormone receptor | 2011 | Molecular and Cellular Endocrinology | Medium | Biased antagonism/readout dependence: supports “≥2 functional readout classes + cross‑receptor family profiling” as hard requirements. |
| 10.1095/biolreprod.113.109397 | Inhibition of Follicle-Stimulating Hormone-Induced Preovulatory Follicles in Rats Treated with a Nonsteroidal Negative Allosteric Modulator of Follicle-Stimulating Hormone Receptor1 | 2014 | Biology of Reproduction | Medium | In vivo endocrine/ovarian endpoint background anchor (non‑cat; different modality), used to highlight risk boundaries for “mechanism–phenotype coupling”. |
| 10.1038/s41467-023-38721-0 | Durable contraception in the female domestic cat using viral-vectored delivery of a feline anti-Müllerian hormone transgene | 2023 | Nature Communications | Medium | Cat‑relevant long‑term follow‑up and endpoint/monitoring references (different modality). |
| 10.1002/vms3.552 | Vaginal stimulation enhances ovulation of queen ovaries treated using a combination of eCG and hCG | 2021 | Veterinary Medicine and Science | Medium | Background for cat reproductive physiology and endpoint wording (not a cat‑food delivery study). |
| 10.1177/1098612X18791872 | Hybrid model intermediate between a laboratory and field study: A humane paradigm shift in feline research | 2018 | Journal of Feline Medicine and Surgery | Medium | Reference for field/ethics methodological frameworks. |
| 10.1186/s13620-021-00189-z | Development of an ethogram/guide for identifying feline emotions | 2021 | Irish Veterinary Journal | Weak | For training/background use; insufficient alone as a key endpoint definition. |
| 10.3390/ani11010020 | Comparison of the Morphology and Developmental Potential of Oocytes Obtained from Prepubertal and Adult Domestic and Wild Cats | 2020 | Animals | Weak | Background on juvenile reproductive biology (not safety evidence). |
| 10.1016/j.theriogenology.2010.01.010 | The GnRH antagonist acyline prevented ovulation, but did not affect ovarian follicular development or gestational corpora lutea in the domestic cat | 2010 | Theriogenology | Medium | Phenotype‑boundary analogy (GnRH axis; not FSHR). |

---

# Appendix A: Gate 1 Standardized Results Table (TSV) Template (field level)

The table below is an “empty template” (no experimental data), illustrating how we structure Gate 1 outputs into an auditable, aggregatable TSV.

```tsv
compound_id	batch_id	assay_id	species	target	cell_system	readout	mode	concentration_unit	ic50	pIC50	e_max	hill_slope	fit_quality	qc_grade	replicate_n	independent_day_n	comparability_flag	bridging_control_present_yes_no	bridging_level	bridging_qc_grade	interference_flag	aggregation_flag	cytotoxicity_flag	notes
```

## A.1 Field value enumerations (controlled vocabulary; non‑confidential freeze)

To ensure comparability across batches and CROs, within the non‑confidential scope we freeze the “allowed value sets” (no thresholds) for the following fields:

- `comparability_flag`: `comparable` / `partial` / `not_comparable`
- `bridging_control_present_yes_no`: `Y` / `N`
- `bridging_level`: `1` / `2` / `3` / `NA`
  - `1`: same‑day, same‑plate cross‑species bridging (strongest)
  - `2`: same‑day cross‑plate bridging
  - `3`: different‑day bridging (weakest; conservative interpretation required)
  - `NA`: not applicable (e.g., no cross‑species comparison performed)
- `bridging_qc_grade`: `good` / `acceptable` / `poor` / `missing`
- `interference_flag`: `none` / `suspected` / `confirmed` / `not_assessed`
- `aggregation_flag`: `none` / `suspected` / `confirmed` / `not_assessed`
- `cytotoxicity_flag`: `none` / `suspected` / `confirmed` / `not_assessed`

Note: if any flag is `confirmed` (or bridging is `poor/missing`, or `comparability_flag=not_comparable`), the record must not be marked `qc_grade=decision‑grade`; detailed disposition and thresholds are frozen in the NDA version.

---

# Appendix B: Gate Decision Memo Template (externally auditable structure)

This is also an “empty template”, illustrating the minimum audit structure of a Gate review:

- Title: Gate X Decision Memo (version/date/owner)
- Frozen review question list (reference Freeze version)
- Executive summary (pass / conditional pass / stop)
- Data package list (directory structure + data dictionary version)
- QC summary (which are decision‑grade vs exploratory vs invalid)
- Key findings (answer each question in the question list)
- Non‑extrapolation boundaries (explicitly state “what cannot be concluded from these data”)
- Deviations/anomalies and dispositions (deviation log)
- Risk updates (whether P0/P1 risks changed)
- Conclusions and next steps (minimum add‑on evidence list / stop rationale mapped to categories)

---

# Appendix C: Field intake/BW pilot data table template (field level)

This template structures the minimum field‑pilot inputs into a form that can back‑feed the Dose/Exposure Model (no site‑specific details included).

```tsv
site_id_anonymized	date	feed_mass_in_g	feed_mass_out_g	feeding_window_hours	cat_count_estimate	id_method	bw_sample_n	bw_p10_kg	bw_p50_kg	bw_p90_kg	bw_p99_kg	intake_p10_g_day	intake_p50_g_day	intake_p90_g_day	intake_p99_g_day	missingness_notes	qa_notes
```

---

# Appendix D: 30‑minute third‑party quick audit checklist (non‑confidential)

If a third party wants to quickly assess whether our “process truly exists and is auditable”, they can check:

1) Is there a clear Gate map (Phase 0–7) and stop categories for each Gate?
2) Is there a unified Freeze→Run→Review→Audit process description, including change control?
3) Is “raw data + metadata delivery” clearly required (not only screenshots/summaries)?
4) Does Gate 1 clearly include four question categories: potency, mechanism, cross‑species selectivity, and false‑positive exclusion?
5) Does the Gate 1 deliverable package provide a directory structure and a standardized results table field dictionary?
6) Is “uncontrolled intake” governed via quantile calibration and model constraints rather than assuming average intake?
7) Is B Standard clearly defined as a co‑primary, with AE/SAE and stop logic (at least category‑level)?
8) Is “target species = cat / minimize non‑target impact and risk governance (no extrapolation to ‘no impact’)” clearly framed as a testable requirement, with cross‑species functional data and a worst‑case exposure governance framework?
9) Is there evidence grading and external claims discipline (no fabrication, no extrapolation, non‑extrapolation boundaries)?
10) Is there a clear separation between externally shareable non‑confidential content vs NDA‑only content?
11) Are deliverable package structures and field templates for Gate 4/6 provided (auditable without leaking secrets)?
12) Are traceability IDs and change control templates provided, enabling review of wording evolution?
13) Are P0 risks bound to minimum falsification actions and mappable to stop categories?


---

# Appendix E: Gate 4 (exposure & intake calibration) deliverable structure + Dose Model input templates (field level)

This appendix provides no numerical values; it provides only externally shareable deliverable structures and field templates for third‑party understanding and audit.

## E.1 Gate 4 deliverable package directory structure (example)
- `Gate4_Deliverable_Package/`
  - `README.md`
  - `Intake_BW_Pilot/` (corresponds to Appendix C)
  - `Exposure_Calibration/` (sample list template in E.3)
  - `DoseModel/` (input template in E.2; scenario template in E.4)
  - `QC/`
  - `Decision/`

## E.2 Dose/Exposure Model input table template (TSV; field level)
```tsv
parameter_id\tparameter_name\tsymbol\tunit\tvalue_type\tp10\tp50\tp90\tp99\tsource_type\tevidence_level\tassumption_rationale\tversion\tnotes
```

Field notes (non‑confidential):
- `value_type`: fixed / range / distribution
- `source_type`: literature / internal / assumption
- `assumption_rationale`: if an input is assumed, the rationale and falsifiability path (category) must be stated

## E.3 Mixed‑feeding / exposure calibration sample list template (TSV; field level)
```tsv
study_id\tsample_id\tmatrix\ttimepoint_label\tcollection_window\tanalysis_method\tqc_status\tnotes
```

## E.4 Scenario definition table template (TSV; field level)
```tsv
scenario_id\tdescription\tintake_quantile\tbw_quantile\tfood_concentration_quantile\tpk_assumption\tdependence_assumption\toutput_metrics\tpass_fail_category\tnotes
```

---

# Appendix F: Gate 6 (controlled feeding, B Standard) deliverable structure + AE/SAE & behavior scoring templates (field level)

This appendix contains no dosing/formulation information; it provides only externally shareable audit structures and field templates.

## F.1 Gate 6 deliverable package directory structure (example)
- `Gate6_Deliverable_Package/`
  - `README.md`
  - `Protocol_Summary/` (endpoint categories, blinding/randomization principles, stop categories)
  - `Event_Log/` (template in F.2)
  - `Behavior_Scoring/` (template in F.3)
  - `Lab_Observations/`
  - `QC/`
  - `Decision/`


## F.2 AE/SAE event log template (TSV; field level)
```tsv
subject_id_anonymized\tdate\tevent_term\tevent_type\tseverity_grade\tseriousness\toutcome\trelationship_assessment\taction_taken\tfollow_up_needed\tnotes
```

## F.3 Behavior scoring record template (TSV; field level)
```tsv
subject_id_anonymized\tdate\tobserver_id\tethogram_version\tdomain\tscore\tcontext_notes\tblinded_yes_no\tinterrater_check\tnotes
```

Field notes (non‑confidential):
- `domain`: activity / aggression_territorial / stress_anxiety / social_withdrawal / sleep_abnormal / other
- `interrater_check`: whether included in consistency sampling (e.g., double scoring/re‑scoring; specific thresholds under NDA)

---

# Appendix G: Traceability IDs & change control templates (non‑confidential)

This appendix provides externally shareable traceability and change control templates, enabling third parties to review wording evolution without accessing internal directories or trade secrets.

## G.1 Traceability ID rules (recommended)
- `CLM-###`: external key statement ID
- `EVD-###`: evidence item ID (linkable to DOI)
- `GATE{n}-DM-YYYYMMDD-###`: Gate decision memo ID
- `TPL-###`: template version ID
- `RISK-P0-###`: P0 risk item ID

## G.2 Change log template (TSV; field level)
```tsv
change_id\tdate\tdocument_id\tfrom_version\tto_version\tchange_summary\taffected_clm_ids\tevidence_level_change\tapprover_role\tnotes
```

## G.3 Wording change explanation template (Markdown; structure)
- Change summary:
- Scope impact: CLM‑xxx / CLM‑yyy
- Reason for change:
- Evidence level change: none / upgraded / downgraded (downgrade must explain risk and temporary replacement wording)
- Whether non‑extrapolation boundaries changed:
- Approver role and date:

---

# Appendix H: Claims Register template (field level)

This appendix provides the minimum field structure of the Claims Register, turning the Claims Policy into an executable, auditable vehicle (no specific claim contents included).

```tsv
clm_id\tclaim_text\tclaim_type\tevidence_level\tevidence_ids\tscope_boundary\tforbidden_extrapolation\towner\tstatus\tapproved_by_role\tapproved_at\treview_checklist_version\tlast_review_date\tlinked_gate_decisions\tnotes
```

Field notes (non‑confidential):
- `claim_type`: conclusion / hypothesis / goal
- `evidence_ids`: reference as an `EVD-###` list
- `scope_boundary`: applicable boundaries (species/scenario/time windows; category description)
- `forbidden_extrapolation`: forbidden extrapolations (must be explicit)
- `status`: draft / approved_for_external / retired
- `approved_by_role`, `approved_at`: external approval role/time (prefer non‑author; auditable trace required)
- `review_checklist_version`: checklist version (evidence that the frozen checklist was followed)

---

# Appendix I: DOI metadata verification record (field level; executed for v0.9)

This appendix records pre‑release verification based on “DOI metadata only, publicly verifiable sources”. It contains no full‑text papers; it includes only publicly verifiable metadata and verification traces.

```tsv
evd_id\tdoi\ttitle\tvenue\tyear\tverified_by_role\tverified_at\tsource_url\tmatch_yes_no\tresolution\tnotes
```

Field notes (non‑confidential):
- `verified_by_role`: verifier role (not the author)
- `verified_at`: verification date (YYYY‑MM‑DD)
- `source_url`: Crossref or publisher landing page link
- `match_yes_no`: whether metadata match
- `resolution`: disposition if mismatch (correct/remove/pending confirmation)

## I.1 Pre‑release verification record for v0.9 (Crossref; non‑confidential)

This version has executed pre‑release verification for all DOIs in Section 11, and archived the records as:
- `docs/nonconfidential/05-DOI-Verification.NC.tsv`
- `docs/nonconfidential/05-DOI-Verification.NC.csv`

Same‑named files in the external directory have also been synchronized.

Verification record (TSV; full 13 entries shown): [1]

```tsv
"evd_id"	"doi"	"title"	"venue"	"year"	"verified_by_role"	"verified_at"	"source_url"	"match_yes_no"	"resolution"	"notes"
"EVD-NC-001"	"10.1016/j.theriogenology.2024.06.005"	"Antibody fragments targeting the extracellular domain of follicular stimulating hormone receptor for contraception in male dogs and cats"	"Theriogenology"	"2024"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1016/j.theriogenology.2024.06.005"	"Y"	"none"	"doi_url=https://doi.org/10.1016/j.theriogenology.2024.06.005"
"EVD-NC-002"	"10.1021/jm049676l"	"Identification of Substituted 6-Amino-4-phenyltetrahydroquinoline Derivatives:  Potent Antagonists for the Follicle-Stimulating Hormone Receptor"	"Journal of Medicinal Chemistry"	"2005"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1021/jm049676l"	"Y"	"none"	"doi_url=https://doi.org/10.1021/jm049676l"
"EVD-NC-003"	"10.1210/en.2018-00317"	"Allosteric Regulation of the Follicle-Stimulating Hormone Receptor"	"Endocrinology"	"2018"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1210/en.2018-00317"	"Y"	"none"	"doi_url=https://doi.org/10.1210/en.2018-00317"
"EVD-NC-004"	"10.3389/fendo.2018.00757"	"Small Molecule Follicle-Stimulating Hormone Receptor Agonists and Antagonists"	"Frontiers in Endocrinology"	"2019"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.3389/fendo.2018.00757"	"Y"	"none"	"doi_url=https://doi.org/10.3389/fendo.2018.00757"
"EVD-NC-005"	"10.1016/j.mce.2016.07.013"	"Profiling of FSHR negative allosteric modulators on LH/CGR reveals biased antagonism with implications in steroidogenesis"	"Molecular and Cellular Endocrinology"	"2016"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1016/j.mce.2016.07.013"	"Y"	"none"	"doi_url=https://doi.org/10.1016/j.mce.2016.07.013"
"EVD-NC-006"	"10.1016/j.mce.2010.12.023"	"A negative allosteric modulator demonstrates biased antagonism of the follicle stimulating hormone receptor"	"Molecular and Cellular Endocrinology"	"2011"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1016/j.mce.2010.12.023"	"Y"	"none"	"doi_url=https://doi.org/10.1016/j.mce.2010.12.023"
"EVD-NC-007"	"10.1095/biolreprod.113.109397"	"Inhibition of Follicle-Stimulating Hormone-Induced Preovulatory Follicles in Rats Treated with a Nonsteroidal Negative Allosteric Modulator of Follicle-Stimulating Hormone Receptor1"	"Biology of Reproduction"	"2014"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1095/biolreprod.113.109397"	"Y"	"none"	"doi_url=https://doi.org/10.1095/biolreprod.113.109397"
"EVD-NC-008"	"10.1038/s41467-023-38721-0"	"Durable contraception in the female domestic cat using viral-vectored delivery of a feline anti-Müllerian hormone transgene"	"Nature Communications"	"2023"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1038/s41467-023-38721-0"	"Y"	"none"	"doi_url=https://doi.org/10.1038/s41467-023-38721-0"
"EVD-NC-009"	"10.1002/vms3.552"	"Vaginal stimulation enhances ovulation of queen ovaries treated using a combination of eCG and hCG"	"Veterinary Medicine and Science"	"2021"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1002/vms3.552"	"Y"	"none"	"doi_url=https://doi.org/10.1002/vms3.552"
"EVD-NC-010"	"10.1177/1098612X18791872"	"Hybrid model intermediate between a laboratory and field study: A humane paradigm shift in feline research"	"Journal of Feline Medicine and Surgery"	"2018"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1177/1098612X18791872"	"Y"	"none"	"doi_url=https://doi.org/10.1177/1098612x18791872"
"EVD-NC-011"	"10.1186/s13620-021-00189-z"	"Development of an ethogram/guide for identifying feline emotions: a new approach to feline interactions and welfare assessment in practice"	"Irish Veterinary Journal"	"2021"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1186/s13620-021-00189-z"	"Y"	"none"	"doi_url=https://doi.org/10.1186/s13620-021-00189-z"
"EVD-NC-012"	"10.3390/ani11010020"	"Comparison of the Morphology and Developmental Potential of Oocytes Obtained from Prepubertal and Adult Domestic and Wild Cats"	"Animals"	"2020"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.3390/ani11010020"	"Y"	"none"	"doi_url=https://doi.org/10.3390/ani11010020"
"EVD-NC-013"	"10.1016/j.theriogenology.2010.01.010"	"The GnRH antagonist acyline prevented ovulation, but did not affect ovarian follicular development or gestational corpora lutea in the domestic cat"	"Theriogenology"	"2010"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1016/j.theriogenology.2010.01.010"	"Y"	"none"	"doi_url=https://doi.org/10.1016/j.theriogenology.2010.01.010"
```

Notes:
1. In the TSV excerpt above, values in `verified_by_role` are intentionally kept in the original Chinese to preserve exact consistency with the archived TSV record. “自动核验（Crossref API）” means “Automated verification (Crossref API)”.
