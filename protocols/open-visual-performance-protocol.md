# The Open Visual Performance Protocol (OVPP)

**Version 1.1 — operational release.**
A practical, open protocol organizations can adopt to reduce visual friction in screen-intensive work while protecting privacy and preserving employee trust.

> Designed to be **implemented, not sold.** Use your own data, your own staffing model, and your own clinical partners.

## 1) What this protocol is for

OVPP is for organizations that want to:

- measure visual load as an operational variable,
- reduce preventable visual friction with low-risk interventions,
- define a safe referral path for people who need clinical care,
- and decide whether to scale by evidence rather than intuition.

This protocol explicitly **does not** replace eye-care practice and does not produce diagnosis by managers.

## 2) Principles (non-negotiable)

1. **Measure patterns, not people.** All routine analytics are aggregated by team/role and never expose individual medical information.
2. **Cheap universal layers first, clinical pathways last.** Improve environments, schedules and behavior before referrals.
3. **Fixed instrument over time.** Keep one validated screening tool across baseline, midline and re-measurement.
4. **Conservative by default.** Use explicit assumptions, scenario bands, and avoid over-claiming gains.
5. **Voluntary participation + opt-out safety.** Participation is not a performance requirement.
6. **Visible work only.** Build this as part of operating rhythm, not a one-off campaign.

## 3) Program operating model

### 3.1 Roles and boundaries

- **Program owner (People/People Operations):** owns timeline, communication, adoption.
- **Data steward:** maintains aggregated reporting and retention controls.
- **Facilities/IT:** executes environment and tool configuration changes.
- **Health and safety/occupational team:** receives escalations and manages the referral path.
- **Licensed ophthalmologist/clinic:** performs diagnosis and treatment for clinically indicated cases.

Boundary rule: managers and HR run screening and interventions at Layers 0–3 only; clinicians handle Layer 4+.

### 3.2 Layered workflow

1. **Layer 0 — Anonymous screening baseline**
2. **Layer 1 — Risk map and load prioritization**
3. **Layer 2 — Environment standardization**
4. **Layer 3 — Designed visual pauses and rhythm redesign**
5. **Layer 4 — Selective referral pathway**
6. **Layer 5 — Re-measurement and governance review**

**Invariant sequence:** baseline → environmental remediation → scheduled micro-pauses → selective referral → re-measurement.

## 4) Layer 0: screening and baseline

Use one validated symptom instrument for the full cycle (examples: CVS-Q, DEQ-5, OSDI, SPEED).

Operational rules:

- Use fixed timing: baseline (D+0), midline (optional D+60), final (D+90), then quarterly/semester repeats.
- Keep question sets unchanged throughout one pilot.
- Do not mix instruments mid-program unless a full restart is approved.
- Record only aggregate identifiers: area, role group, seniority band (optional), work modality (home/office/hybrid).

Output:

- Baseline symptom prevalence by role cluster.
- Baseline symptom intensity category (mild/moderate/severe).

## 5) Layer 1: risk mapping by role

Stratify by function and exposure:

- coding/review,
- QA,
- design,
- support/video-heavy,
- finance/analysis,
- mixed-screen roles.

Combine:

- symptom scores,
- hours at screen and call load,
- number of monitors,
- baseline posture/environment score.

Output:

- role-level heat map of visual load,
- list of priority cohorts for intervention,
- no individual-level heat maps.

## 6) Layer 2: environment standardization checklist

Apply this to every workstation and remote setup (with equivalent home-office validation):

- viewing distance: 50–70 cm,
- top of monitor at or slightly below eye level (neutral gaze downward 15–20°),
- anti-glare and matte surfaces,
- monitor centered to natural line of sight;
- avoid direct screen-facing bright windows and bright side reflections,
- humidity target 40–60%,
- indoor temperature ~21–23 °C,
- airflow redirected away from the eyes,
- font/contrast/brightness checked at task-specific zoom,
- software reminders and screen layout simplified.

Critical spend note:

- **Do not prioritize blue-light filters as a preventive investment** unless a new validated evidence package is published.

## 7) Layer 3: pauses as infrastructure

Treat visual recovery as always-on infrastructure:

- implement prompts integrated to workflow tools (calendar/IDE/meeting tools),
- align pause timing to existing cadences (for example sprint blocks, review cycles, meeting cadence),
- set default pause windows where possible.

Recommended operating cadence:

- every 20 minutes: 20 seconds gaze-reset,
- every 90 minutes: 5–10 minutes break with reduced near-focus demand,
- at least one no-screen segment in long meetings when possible.

Evidence principle: instructions work only when prompts are present and sustained.

## 8) Layer 4: referral protocol

Apply this section only after layers 0–3 and exposure corrections.

### 8.1 Initial triage buckets

- **Low risk**
  - mild, infrequent symptoms,
  - no functional impact,
  - short response to basic pauses.

- **Moderate risk**
  - recurrent weekly symptoms,
  - visible functional impact,
  - plausible association with screen/environment exposure.

- **High risk**
  - persistent symptoms,
  - recurrent blur or strong discomfort,
  - pain, photophobia, persistent redness, recurrent unsupervised drop use,
  - symptomatic contact lens users.

### 8.2 Immediate referral criteria

Escalate immediately to occupational health + eye-care pathway when any of the following appears:

- severe ocular pain,
- significant vision change,
- marked unilateral symptoms,
- heavy discharge,
- suspected infection/inflammation,
- trauma,
- sudden severe photophobia,
- worsening in a contact lens wearer.

### 8.3 Referral handoff package

With informed consent, provide:

- role and exposure pattern,
- estimated screen hours and call load,
- home-office or desk constraints,
- screening score bucket and symptom pattern,
- environmental interventions already completed.

## 9) Layer 5: governance and dashboard

Minimum indicator stack (all aggregated):

| Indicator | Source | Cadence |
|---|---|---|
| Symptom prevalence | screening instrument | semiannual |
| Symptom intensity by level | screening instrument | quarterly |
| Exposure load | IT/self-report | quarterly |
| Environmental correction status | facilities checklist | monthly |
| Pause adherence | software data/self-report | monthly |
| Campaign participation | platform logs | monthly |
| Perceived productivity and quality signals | short internal survey | quarterly |

Three rhythms are mandatory:

- **monthly:** environment and pause adherence,
- **quarterly:** exposure and symptom intensity,
- **semiannual:** prevalence and strategy review.

## 10) 90-day pilot blueprint

| Week | Milestone |
|---|---|
| 1–2 | baseline screening + current-state map |
| 2–3 | risk map + priority area decision |
| 3–6 | environment actions (standardization) |
| 4–12 | pause and communication playbook |
| 6–12 | selective referral workflow |
| 12–13 | re-measurement + board review |

Exit criteria:

- at least one measurable improvement signal in adherence or symptoms, or a clear documented reason if null,
- documented decision to scale, adapt, or pause.

## 11) ROI and anti-overclaim policy

Use a scenario model:

- **Cost of inaction** = `N × loaded_cost_per_person × prevalence × productivity_loss`
- **Recovered benefit** = `cost_of_inaction × recoverable_fraction`

Scenario bands (for internal simulation only):

- conservative / base / high-risk bands,
- explicit assumptions stored with every calculation,
- never present one deterministic return.

Never claim that all measured productivity loss is caused by visual fatigue or that referral actions recover all losses.

## 12) Privacy, ethics, and legal posture

- Aggregate reports only; no individual results returned to managers.
- No mandatory participation.
- No diagnosis by non-clinical staff.
- Keep referral handling separate from performance records.
- Provide the purpose statement to participants in plain language.

**Data minimization:** only what is necessary for the program decision.

## 13) Ready-to-run checklist

- [ ] Choose one screening instrument and lock it.
- [ ] Define role groups and target area.
- [ ] Publish the non-negotiables to leadership and participants.
- [ ] Run baseline and publish role-level heat map.
- [ ] Roll environment and pause layers together.
- [ ] Activate referral criteria with explicit immediate escalation rules.
- [ ] Run re-measurement and close pilot by evidence.

## Final note

This version is open and intentionally conservative. Translate thresholds to local legal and clinical requirements, but keep the sequence and ethics unchanged.
