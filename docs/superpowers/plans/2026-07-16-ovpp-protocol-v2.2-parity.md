# OVPP Protocol v2.2 EN/PT-BR Parity Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Bring `protocols/open-visual-performance-protocol.md` (EN) into full structural parity with `protocols/protocolo-aberto-desempenho-visual.md` (PT-BR), apply a wording clarity pass to both, and bump both to Version 2.2.

**Architecture:** PT-BR is the canonical content source (it already has all 13 sections). EN is fully rewritten to mirror it section-by-section, translated with the clarity pass baked in. PT-BR gets a small, targeted clarity edit (version line + the one dense formula block) — it doesn't need a full rewrite since it's already the mature document. Two ancillary docs get version/parity notes. A final verification task checks structural parity and re-reads both files against the repo's non-negotiable compliance rules.

**Tech Stack:** Plain markdown, no build tooling, no test framework. "Testing" here means structural checks (`grep`/`diff`) and human/compliance review, not automated tests.

## Global Constraints

- PT-BR (`protocols/protocolo-aberto-desempenho-visual.md`) is the canonical content source; EN must mirror it section-by-section, same 13 headings, same order (spec section 1).
- No new rules, criteria, or content added or removed anywhere in either protocol file — this is a parity + wording-clarity pass only (spec Non-goals).
- Version bump `2.1 → 2.2` in both protocol files, `protocols/README.md`, and `PRODUCT-COMPANION-EVALUATION.md` (spec Goals).
- Out of scope, do not touch: `kit/`, `KIT-EXECUCAO.md`, root `README.md`, `index.html`, `pt-br.html` (spec Non-goals — confirmed neither landing page references a version string).
- Compliance floor (from this repo's `CLAUDE.md`): no diagnosis by non-clinical staff, no prospective-ROI language, fixed operating sequence preserved, referral never delayed by organizational measures.
- **Commit gate:** never run `git commit` without the user's explicit go-ahead for that specific commit — present the message and wait, per the user's standing instruction. Do not batch multiple tasks' commits into one without asking.
- **Commit message format:** this repo's pre-commit hook enforces Conventional Commits `<type>(<scope>): <summary>` (valid types: feat, fix, refactor, test, docs, chore, perf, ci, style, build, revert; summary ≤72 chars). The hook's parser misreads `-m "$(cat <<EOF ... EOF)"` heredoc-via-command-substitution as literal text and rejects it. Write the message to a file and commit with `git commit -F <file>` instead (the hook explicitly skips validation for `-F`/`--file` form).
- Human review: the repo owner (a licensed ophthalmologist) must review clinical/legal wording before merge — not delegable, not automatable.

---

### Task 1: Rewrite EN protocol to full v2.2 parity

**Files:**
- Modify (full rewrite): `protocols/open-visual-performance-protocol.md`

**Interfaces:**
- Consumes: PT-BR section structure and content from `protocols/protocolo-aberto-desempenho-visual.md` (read-only reference, unchanged by this task).
- Produces: 13 EN section headings (`0) Product role` … `12) Deployment checklist` + `Closing`) that Task 5's parity check greps for.

- [ ] **Step 1: Replace the entire file content**

Overwrite `protocols/open-visual-performance-protocol.md` with exactly this content:

```markdown
# Open Visual Performance Protocol (OVPP)

**Version 2.2 — compatible with the book v2.9.13 claim contract.**

Open operational protocol that turns the argument of *O Custo Invisível do Olho Seco* into a measurable, conservative, privacy-centered 90-day corporate pilot for screen-intensive teams.

> The book makes the invisible cost visible. OVPP turns that thesis into an operating system for action.

## 0) Product role

OVPP is the open implementation layer alongside the book.

| The book | OVPP |
|---|---|
| Explains why dry eye and digital visual fatigue matter for productivity | Defines how an organization can measure and act without becoming a clinic |
| Builds the executive case around presenteeism, rework, visual instability and screen load | Converts the case into phases, roles, indicators, checklists and decision criteria |
| Convinces leadership to approve measurement | Delivers a practical path to run the first 90-day pilot |
| Avoids inflating financial return | Separates capacity, quoted cost and observed benefit before any retrospective ROI |

OVPP does not replace the book. It is the book's operating companion: a reusable protocol that readers, companies, clinics and People teams can adopt once they accept the central thesis.

## 1) Purpose of this protocol

OVPP is for organizations that want to:

- treat visual load as an operational variable,
- reduce avoidable visual friction with low-risk interventions,
- turn scattered symptoms into aggregated indicators,
- protect privacy and trust,
- define a safe clinical-referral path for those who need it,
- test feasibility and measurement quality before advancing to confirmation.

This protocol does **not** replace ophthalmological practice, does **not** diagnose employees, and does **not** authorize managers to access individual medical information.

## 2) Users and buying context

Primary users:

- People/HR leaders who need a safe program,
- occupational-health teams who need a structured workflow,
- operations leaders with high screen-exposure teams,
- CFOs who require quoted cost, coverage threshold and attributable evidence,
- facilities and IT responsible for environment and tools,
- ophthalmologists or clinics supporting referred cases.

Best first teams:

- software engineering and code review,
- QA and data validation,
- customer support or success with high video/chat load,
- finance, legal, compliance and analysis,
- design, content and research,
- any hybrid team with long screen exposure and irregular ergonomics.

The best first adoption is not "wellness for the whole company." It is a bounded pilot in one high-exposure group, with a named owner, fixed metrics, and a day-90 decision to stop, adapt or advance to confirmation.

## 3) Non-negotiable principles

1. **Measure patterns, not people.** Routine analyses are aggregated by team, role or exposure group.
2. **The book's thesis, the protocol's discipline.** The book creates urgency. The protocol requires measurable execution.
3. **Organizational layers never delay care.** Environment, workflow and pauses can start early. Severity, recurrence, functional impact, contact lenses, preference or red flags trigger the clinical pathway in parallel.
4. **One instrument per cycle.** Keep the same validated questionnaire from baseline through re-measurement.
5. **No diagnosis by non-clinical staff.** Managers, HR and dashboards describe exposure and operational priorities — not disease or individual clinical risk.
6. **Voluntary participation.** Participation is never a performance criterion.
7. **Auditable economics.** Before action, use capacity and coverage threshold. ROI is retrospective only, with incremental and attributable benefit.
8. **Visible governance.** Every pilot has a sponsor, an owner, a data lead, a clinical boundary and an exit decision.

## 4) Core definitions

- **Visual load:** the sustained demand screens, close focus, meetings, multiple monitors, lighting, airflow and cognitive intensity place on the visual system.
- **Visual friction:** avoidable loss of comfort, stability or endurance while reading, focusing, reviewing, coding, designing or communicating on screens.
- **Visual presenteeism:** productivity loss while the person remains present and working, often through re-reading, slower review, discomfort, avoidance, unplanned pauses or rework.
- **Operational pattern:** an aggregated signal by role, team, location, modality or period.
- **Clinical case:** an individual health situation that requires licensed evaluation.

The protocol rests on one boundary: operational patterns belong to the organization; individual diagnosis belongs to the clinic.

## 5) Minimum viable package

A serious pilot needs these artifacts before launch:

- a plain-language purpose statement,
- a chosen screening instrument and fixed measurement dates,
- defined role and exposure groups,
- an environmental checklist,
- a pause and workflow playbook,
- referral criteria and urgency rules,
- a data-minimization and access policy,
- a dashboard template,
- a quoted bill of materials and capacity/threshold spreadsheet,
- a day-90 decision memo template.

If an item is missing, the pilot can still start as a learning exercise, but must not be sold internally as a governed program.

## 6) Operating model and roles

| Role | Responsibility | Must not do |
|---|---|---|
| Executive sponsor | budget, priority, progression decision | request individual health data |
| Program owner | schedule, communication, adoption, operational cadence | diagnose or pressure participation |
| Data lead | aggregation, retention, access and dashboard hygiene | expose identifiable responses |
| Facilities/IT | workstation, light, airflow, tools and reminders | infer health from tool data |
| Occupational health | risk pathway, escalation and policy alignment | replace ophthalmological diagnosis |
| Ophthalmology partner | diagnosis, treatment and clinical guidance | share details without consent |
| Team leads | protect pauses, normalize adherence, remove blockers | rank people by symptoms or adherence |

Boundary rule: managers and HR operate organizational measures and aggregates; occupational health and licensed ophthalmological care receive referrals in parallel whenever clinical criteria are triggered.

## 7) OVPP workflow

### Phase 0 — Sponsorship agreement

Define the target group, owner, budget, dates, privacy boundary and success criteria.

Required outputs:

- pilot charter,
- risk level,
- named program owner,
- written non-use rule for performance evaluation,
- date of the day-90 stop/adapt/advance-to-confirmation decision.

### Layer 0 — Anonymous baseline

Use one instrument suited to the whole cycle. Choosing it requires a documented identified version, validation for language, population and purpose, licensing, and local clinical interpretation; citing an instrument does not authorize its use.

Operating rules:

- baseline at D+0,
- optional midpoint at D+45 or D+60,
- final re-measurement at D+90,
- same questions and same scoring logic throughout the cycle,
- collect only aggregable identifiers such as role group, area, modality and broad exposure category.

Outputs:

- initial symptom distribution by role group,
- symptom-intensity distribution,
- response rate,
- confidence note and limitations.

### Layer 1 — Visual load and operational-priority map

Cross symptoms and exposure without creating individual maps.

Recommended dimensions:

- role or function,
- screen hours and meeting load,
- deep-focus blocks,
- multiple-monitor use or isolated laptop use,
- remote/onsite/hybrid work,
- environmental constraints,
- high-precision visual tasks such as QA, review, analysis or design.

Outputs:

- visual-load map by role,
- priority-cohort decision,
- list of environmental and workflow hypotheses,
- referral-attention list, handled only by the appropriate health pathway.

### Layer 2 — Environmental standardization

Apply the minimum checklist:

- screen distance around 40–70 cm,
- monitor's top edge at or slightly below eye level,
- neutral gaze angled slightly down, around 15–20 degrees,
- monitor aligned to the natural line of sight,
- reduced glare and reflection,
- font, zoom, contrast and brightness adjusted to the task,
- target humidity of 40–60% where controllable,
- temperature around 22–24°C where controllable,
- airflow directed away from the face,
- an equivalent home-office self-check.

Investment rule:

- do not prioritize blue-light filters as the primary preventive investment without a new, robust body of evidence.

### Layer 3 — Pauses as infrastructure

Treat visual recovery as workflow design, not willpower.

Recommended cadence:

- every 20 minutes: 20 seconds of distance focus and a blink reset,
- every 90 minutes: 5–10 minutes with lower near-focus demand,
- long meetings: one screen-free or away-from-screen segment when possible,
- high-precision work: protected pauses before extended review, QA, analysis or decisions.

Implementation options:

- calendar defaults,
- IDE or browser reminders,
- Slack/Teams prompts,
- meeting templates,
- team rituals,
- offline tools that do not track productivity.

Success is not "people were told to pause." Success is sustained prompt presence, adherence and symptom re-assessment.

### Layer 4 — Selective referral

Keep this available from day one and trigger it in parallel based on severity, recurrence, functional impact, contact lenses, preference, occupational-health judgment, or red flags. Environmental measures are never a prerequisite for care.

| Tier | Pattern | Action |
|---|---|---|
| Low | mild, infrequent symptoms; no functional impact | education, environmental checklist, next screening |
| Moderate | weekly symptoms; functional impact; screen/environment association | environmental correction, structured pauses, re-assessment in 60–90 days |
| High | persistent symptoms, recurrent blurring, strong discomfort, worsening with contact lenses, frequent unguided eye-drop use | occupational-health pathway and ophthalmological referral |

Immediate referral criteria:

- significant eye pain,
- meaningful vision decline,
- marked unilateral symptoms,
- heavy discharge,
- suspected infection or inflammation,
- trauma,
- sudden significant photophobia,
- worsening in contact-lens wearers.

Referral package, with consent:

- role and exposure pattern,
- estimated screen and call hours,
- home-office or workstation constraints,
- score range and symptom pattern,
- environmental interventions already executed.

### Layer 5 — Re-measurement and governance

At D+90, compare baseline and final measurement using the same instrument and the same aggregation logic.

Minimum dashboard:

| Indicator | Source | Cadence |
|---|---|---|
| Participation | screening platform | baseline and final |
| Symptom distribution | screening instrument | baseline, D+90, semi-annual |
| Symptom intensity | screening instrument | baseline, D+90, quarterly if escalating |
| Exposure load | self-report/safe IT aggregate | quarterly |
| Environmental correction | checklist | monthly |
| Pause adherence | self-report or non-invasive signal | monthly |
| Referral volume by tier | occupational-health aggregate | quarterly |
| Perceived focus and quality | internal mini-survey | quarterly |

Day-90 decisions:

- **Advance to confirmation:** adequate feasibility, usable data, safety and governance preserved; effect not yet confirmed.
- **Adapt:** exploratory signal or incomplete execution, with correctable limitations.
- **Stop:** no feasibility, low confidence, risk, weak governance, or an unsupported local hypothesis.

## 8) Capacity, threshold and retrospective ROI

Before any intervention, use only:

- **Equivalent capacity** — multiply the headcount (`N`) by the direct work cost for the horizon, then by the symptomatic fraction, then by the perceived-limitation factor: `N × direct_work_cost_in_horizon × symptomatic_fraction × perceived_limitation`.
- **Coverage threshold** — divide the quoted cost for the same horizon by the equivalent capacity: `quoted_cost_in_same_horizon ÷ equivalent_capacity`.

Equivalent capacity is not cash, and the threshold is not a probability of return. Record the source, date, owner and nature of each assumption. ROI remains unavailable until an incremental, attributable and auditable financial benefit exists alongside actual cost in the same horizon. Never convert a symptom score directly into money.

## 9) Privacy and ethics

Mandatory safeguards:

- aggregated reporting only,
- no individual results for managers,
- no mandatory participation,
- no diagnosis by non-clinical staff,
- health data kept separate from performance evaluation,
- referral through health channels with consent,
- a clear retention policy,
- plain-language notice to participants.

Minimum promise to participants:

> This program measures aggregated visual load and work friction. It is not a performance evaluation, and individual symptom responses will not be shared with managers.

## 10) Product packaging as book companion

Recommended ladder:

1. **Book:** creates executive awareness and urgency.
2. **Open OVPP:** offers a transparent, trustworthy protocol.
3. **Executive review kit:** turns the thesis into a decision memo.
4. **90-day pilot:** applies OVPP in one high-exposure team.
5. **Dashboard and executive review:** supports the stop/adapt/advance-to-confirmation decision.
6. **Partner clinical pathway:** supports cases that require licensed care.
7. **Annual governance cycle:** keeps measurement, environment and referral current.

The open protocol must remain usable without additional purchase. That openness builds trust and makes it easier to justify paid implementation, clinical partnership or advisory work.

## 11) Definition of done for a strong pilot

A pilot is complete only when:

- one instrument was used consistently,
- baseline and final measurement were collected,
- an exposure and operational-priority map was produced without individual exposure,
- the environmental layer was actually executed,
- pauses were implemented beyond a single message,
- referral criteria were active before symptom collection,
- urgency signals had a defined route,
- capacity and threshold were documented without presenting prospective ROI,
- a day-90 decision memo was written,
- at least one improvement, limitation or failed assumption was documented.

## 12) Deployment checklist

- [ ] Choose and lock a screening instrument.
- [ ] Define role groups, target cohort and pilot owner.
- [ ] Publish privacy and non-use promises.
- [ ] Run baseline and generate an aggregated map.
- [ ] Execute environmental standardization.
- [ ] Deploy pause infrastructure.
- [ ] Activate referral and urgency criteria.
- [ ] Re-assess at D+90.
- [ ] Produce the stop/adapt/advance-to-confirmation memo.
- [ ] Record learnings for the next cycle.

## Closing

OVPP is open and deliberately conservative. Adjust thresholds to local legal and clinical requirements, but preserve the sequence, the privacy boundary and the anti-hype posture. That is what makes it a credible companion to the book, not just a wellness campaign with better branding.
```

- [ ] **Step 2: Verify heading parity against PT-BR**

Run:
```bash
grep -oE '^## [0-9]+\)' protocols/open-visual-performance-protocol.md
grep -oE '^## [0-9]+\)' protocols/protocolo-aberto-desempenho-visual.md
```
Expected: both commands print the identical sequence `## 0)` through `## 12)`, one per line, in the same order.

**Terminology-normalization note:** the spec's clarity-pass scope flagged "sinais de alerta" / "red flags" / "critérios de encaminhamento imediato" as possibly-inconsistent terms. On inspection these are not actually inconsistent — PT-BR itself uses "sinais de alerta" as the abstract principle-level trigger (section 3) and "Critérios de encaminhamento imediato" as the concrete itemized list (section 7 / Camada 4), the same abstract-vs-concrete distinction. The EN text above preserves that exact distinction ("red flags" in section 3, "Immediate referral criteria" heading in section 7 / Layer 4). No further terminology change is needed.

- [ ] **Step 3: Commit**

Write the commit message to a temp file (do not use a heredoc-via-`$()` — see Global Constraints):
```bash
cat > /tmp/ovpp-commit-msg.txt <<'EOF'
docs(protocol): port EN protocol to v2.2 full structural parity

EN was a 44-line summary missing 11 of PT-BR's 12 sections, including
the roles/governance table. Rewritten to mirror PT-BR section-by-
section (13 headings, same tables, same rules), translated with the
agreed clarity-pass style baked in. No new rule or content added.
EOF
```
Present this message to the user and wait for explicit go-ahead before running:
```bash
git add protocols/open-visual-performance-protocol.md
git commit -F /tmp/ovpp-commit-msg.txt
```

---

### Task 2: Clarity-pass edit on PT-BR (version line + formula block)

**Files:**
- Modify: `protocols/protocolo-aberto-desempenho-visual.md`

**Interfaces:**
- Consumes: none (this is the canonical source; only these two spots are dense enough per the spec's clarity-pass scope to need rewording).
- Produces: PT-BR version string `Versão 2.2` that Task 5 greps for.

- [ ] **Step 1: Bump the version line**

In `protocols/protocolo-aberto-desempenho-visual.md`, replace:
```
**Versão 2.1 — compatível com o contrato de alegações do livro v2.9.13.**
```
with:
```
**Versão 2.2 — compatível com o contrato de alegações do livro v2.9.13.**
```

- [ ] **Step 2: Reword the section 8 formula block for clarity**

Replace this block (section `## 8) Capacidade, limiar e ROI retrospectivo`):
```
Antes da intervenção, use apenas:

- **Capacidade equivalente** = `N × custo_direto_no_horizonte × fração_sintomática × limitação_percebida`;
- **Limiar de cobertura** = `custo_cotado_no_horizonte ÷ capacidade_equivalente`.

Capacidade não é caixa e limiar não é probabilidade de retorno. Registre fonte, data, responsável e natureza de cada premissa. ROI permanece indisponível até existir benefício financeiro incremental, atribuível e auditável e custo efetivo no mesmo horizonte. Sintomas não são convertidos diretamente em reais.
```
with:
```
Antes da intervenção, use apenas:

- **Capacidade equivalente** — multiplique o efetivo de pessoas (`N`) pelo custo do trabalho direto no horizonte, depois pela fração sintomática, depois pelo fator de limitação percebida: `N × custo_direto_no_horizonte × fração_sintomática × limitação_percebida`.
- **Limiar de cobertura** — divida o custo cotado no mesmo horizonte pela capacidade equivalente: `custo_cotado_no_horizonte ÷ capacidade_equivalente`.

Capacidade equivalente não é caixa, e o limiar não é probabilidade de retorno. Registre fonte, data, responsável e natureza de cada premissa. ROI permanece indisponível até existir benefício financeiro incremental, atribuível e auditável, junto com custo efetivo, no mesmo horizonte. Nunca converta um escore de sintomas diretamente em reais.
```

Note: this changes wording only — both formulas, both variable names, and every numeric/rule claim are unchanged from the original.

- [ ] **Step 3: Verify no rule content changed**

Run:
```bash
git diff protocols/protocolo-aberto-desempenho-visual.md
```
Expected: diff shows exactly the version-line change and the section-8 reword. Manually confirm the reworded paragraph still asserts: (a) equivalent capacity ≠ cash, (b) threshold ≠ probability of return, (c) ROI unavailable until incremental+attributable+auditable benefit and real cost exist in the same horizon, (d) never convert symptom score to money. All four must still be present in identical substance.

- [ ] **Step 4: Commit**

```bash
cat > /tmp/ovpp-commit-msg-2.txt <<'EOF'
docs(protocol): bump PT-BR to v2.2 and reword capacity formula block

Version line 2.1 -> 2.2. Reworded the equivalent-capacity/coverage-
threshold block from inline formula-in-prose into labeled bullets for
readability. No rule, number, or claim changed.
EOF
```
Present this message to the user and wait for explicit go-ahead before running:
```bash
git add protocols/protocolo-aberto-desempenho-visual.md
git commit -F /tmp/ovpp-commit-msg-2.txt
```

---

### Task 3: Update `protocols/README.md`

**Files:**
- Modify: `protocols/README.md`

**Interfaces:**
- Consumes: none.
- Produces: none (leaf task).

- [ ] **Step 1: Fix the stale version claim**

Replace:
```
Both are Version 2.0 companion-product releases for *O Custo Invisível do Olho
Seco*.
```
with:
```
Both are Version 2.2 companion-product releases for *O Custo Invisível do Olho
Seco*, structurally equivalent section-by-section.
```

- [ ] **Step 2: Verify**

Run:
```bash
cat protocols/README.md
```
Expected: file reads correctly, no other line changed, "Version 2.2" and "structurally equivalent" both present.

- [ ] **Step 3: Commit**

```bash
cat > /tmp/ovpp-commit-msg-3.txt <<'EOF'
docs(protocol): correct protocols/README.md version claim to 2.2

Was stuck at "Version 2.0" (already stale vs the 2.1 files) and
implied EN/PT-BR parity that didn't exist yet. Now accurate: both
files are 2.2 and structurally equivalent.
EOF
```
Present this message to the user and wait for explicit go-ahead before running:
```bash
git add protocols/README.md
git commit -F /tmp/ovpp-commit-msg-3.txt
```

---

### Task 4: Update `PRODUCT-COMPANION-EVALUATION.md`

**Files:**
- Modify: `PRODUCT-COMPANION-EVALUATION.md`

**Interfaces:**
- Consumes: none.
- Produces: none (leaf task).

- [ ] **Step 1: Append a parity note under "Compatibility decision"**

The file currently ends with:
```
## Compatibility decision

Version 2.1 supersedes the former scenario-ROI and scale-at-D+90 language. Any older copy containing “conservative ROI”, recoverable fraction, risk map based on symptoms or a mandatory sequence before referral is incompatible and must not be deployed.
```

Append this paragraph immediately after it (same section, new paragraph):
```

Version 2.2 brings the English protocol into full structural parity with the Portuguese (PT-BR) release — same 13 sections, same tables, same rules — plus a wording clarity pass on both languages. No release gate, threshold, or non-negotiable rule changed.
```

- [ ] **Step 2: Verify**

Run:
```bash
tail -5 PRODUCT-COMPANION-EVALUATION.md
```
Expected: the new paragraph is the last thing in the file, release gates section above it is untouched.

- [ ] **Step 3: Commit**

```bash
cat > /tmp/ovpp-commit-msg-4.txt <<'EOF'
docs(protocol): note v2.2 EN/PT-BR parity in compatibility evaluation

Records that 2.2 is a structural-parity + wording pass, not a
release-gate change.
EOF
```
Present this message to the user and wait for explicit go-ahead before running:
```bash
git add PRODUCT-COMPANION-EVALUATION.md
git commit -F /tmp/ovpp-commit-msg-4.txt
```

---

### Task 5: Final structural parity and compliance verification

**Files:**
- None modified — verification only.

**Interfaces:**
- Consumes: final state of both protocol files (Tasks 1-2) and both ancillary docs (Tasks 3-4).
- Produces: none — this is the plan's terminal task.

- [ ] **Step 1: Confirm heading parity (repeat of Task 1 Step 2, post all edits)**

Run:
```bash
diff <(grep -oE '^## [0-9]+\)' protocols/open-visual-performance-protocol.md) \
     <(grep -oE '^## [0-9]+\)' protocols/protocolo-aberto-desempenho-visual.md)
```
Expected: no output (empty diff — both files have identical, identically-ordered numbered headings).

- [ ] **Step 2: Confirm both protocol files declare the same version**

Run:
```bash
grep -oE 'Version 2\.[0-9]+|Versão 2\.[0-9]+' protocols/open-visual-performance-protocol.md protocols/protocolo-aberto-desempenho-visual.md
```
Expected:
```
protocols/open-visual-performance-protocol.md:Version 2.2
protocols/protocolo-aberto-desempenho-visual.md:Versão 2.2
```

- [ ] **Step 3: Re-read both files against the CLAUDE.md non-negotiable rules**

Manually confirm, reading both full files:
- No non-clinical role is granted diagnostic authority anywhere (check the section-6/Operating model and roles tables in both languages — "Must not do" / "Não deve fazer" columns still forbid diagnosis).
- No prospective/scenario ROI language was introduced (check section 8 in both — still says ROI is retrospective-only).
- The fixed operating sequence (baseline → risk map → environment → pauses → referral → re-measurement) is unchanged and in the same order in both section 7 / Fluxo OVPP.
- Referral is still never gated behind environmental measures (Layer 4 / Camada 4 in both still says environmental measures are not a prerequisite for care).

If any of the four checks fails, stop and fix before proceeding — do not mark this task complete.

- [ ] **Step 4: Hand off for human review**

No commit in this task (nothing changed). Tell the user: structural parity and compliance checks pass; the repo owner (licensed ophthalmologist) should give the clinical/legal content a final read before this is considered done, per the plan's Global Constraints.
