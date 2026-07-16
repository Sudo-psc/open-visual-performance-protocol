# OVPP protocol v2.2 — EN/PT-BR parity and clarity pass

Date: 2026-07-16
Status: draft, pending user review

## Problem

`protocols/open-visual-performance-protocol.md` (EN, 44 lines) and
`protocols/protocolo-aberto-desempenho-visual.md` (PT-BR, 326 lines) are both
tagged **Version 2.1**, but they are not equivalent documents. PT-BR has grown
into a full 12-section spec (product role, purpose, users, principles,
definitions, minimum package, operating model and roles, full workflow with
Phase 0 + Layers 0-5, capacity/threshold economics, privacy and ethics,
product packaging, definition of done, deployment checklist) plus a closing
note. EN is a condensed summary that omits an entire section — most notably
section 6, "Modelo operacional e papéis" (roles, responsibilities, and
decision authority for each stakeholder: executive sponsor, program owner,
data owner, facilities/IT, occupational health, ophthalmology partner, team
leads) — along with ten other sections PT-BR carries.

This drifted from an intentional design choice into an accidental gap:
confirmed with the repo owner that EN and PT-BR are supposed to be
equivalent, and the asymmetry should be corrected, not preserved as
"EN = executive summary."

## Goals

- EN protocol becomes a full structural mirror of PT-BR: same 13 headings
  (sections 0-12 plus closing), same order, same level of content detail.
- Both documents get a wording clarity pass — denser sentences and
  formula-in-prose blocks reworded for readability — without changing
  meaning, removing any existing rule, or adding new content/rules.
- Version bumps from 2.1 to 2.2 in both protocol files and in the two
  documents that reference protocol version (`protocols/README.md`,
  `PRODUCT-COMPANION-EVALUATION.md`).

## Non-goals

- No new protocol content, rules, criteria, or sections beyond what PT-BR
  already contains today — this is a parity + clarity pass, not a v2.2
  feature addition.
- No changes to the execution kit (`kit/`, `KIT-EXECUCAO.md`) — tracked as a
  separate future spec.
- No changes to `index.html` / `pt-br.html` (confirmed: neither references a
  protocol version string).
- No change to the release gates listed in
  `PRODUCT-COMPANION-EVALUATION.md`.

## Design

### 1. Source of truth and section mapping

PT-BR (`protocolo-aberto-desempenho-visual.md`) is the canonical content
source — it is already the mature, complete version. EN
(`open-visual-performance-protocol.md`) is rewritten from scratch to mirror
it section-by-section:

| # | PT-BR heading | EN heading |
|---|---|---|
| 0 | Papel como produto | Product role |
| 1 | Objetivo deste protocolo | Purpose of this protocol |
| 2 | Usuários e contexto de compra | Users and buying context |
| 3 | Princípios inegociáveis | Non-negotiable principles |
| 4 | Definições centrais | Core definitions |
| 5 | Pacote mínimo viável do OVPP | Minimum viable package |
| 6 | Modelo operacional e papéis | Operating model and roles |
| 7 | Fluxo OVPP (Fase 0 + Camadas 0-5) | OVPP workflow (Phase 0 + Layers 0-5) |
| 8 | Capacidade, limiar e ROI retrospectivo | Capacity, threshold and retrospective ROI |
| 9 | Privacidade e ética | Privacy and ethics |
| 10 | Embalagem de produto como complemento do livro | Product packaging as book companion |
| 11 | Definição de concluído para um piloto forte | Definition of done for a strong pilot |
| 12 | Checklist de implantação | Deployment checklist |
| — | Fechamento | Closing |

Tables (e.g. the section 6 roles table, the section 7 referral tier table,
the section 7 dashboard table) are ported as tables, not flattened to prose.

### 2. Clarity pass — scope

Applied to both languages, during the same editorial pass (not a separate
step), bounded strictly to wording:

- Reword dense formula-in-prose blocks (e.g. the "Capacidade equivalente" /
  "Equivalent capacity" formulas) into a labeled bullet per variable instead
  of an inline mathematical expression embedded in a sentence.
- Split multi-clause sentences (common in PT-BR's numbered principle lists)
  into shorter sentences where doing so doesn't change what's asserted.
- Normalize terminology that is currently used inconsistently across
  sections — e.g. "sinais de alerta" / "red flags" / "critérios de
  encaminhamento imediato" all refer to the same urgent-referral concept in
  different places; pick one term per concept and use it consistently within
  each language.
- Explicitly out of bounds: no new rule, no new criterion, no new use case,
  no removed rule. If something reads as "missing" during the pass (a new
  scenario, a new instrument type), it is noted but left out of this spec.

### 3. Ancillary file updates

- `protocols/README.md` — currently states "Both are Version 2.0
  companion-product releases," which is already stale (files say 2.1) and
  also implies EN/PT-BR are at parity today, which they aren't. Update to
  "Version 2.2" and drop/rephrase the parity implication once it's actually
  true.
- `PRODUCT-COMPANION-EVALUATION.md` — add a note under "Compatibility
  decision" that 2.2 brings EN into full structural parity with PT-BR;
  release gates list is unchanged.
- `README.md` (repo root) — no change (only links to the protocol files, no
  version claims).
- `index.html` / `pt-br.html` — no change (confirmed no version string
  present).
- `kit/`, `KIT-EXECUCAO.md` — out of scope, unaffected.

### 4. Validation

No automated tests apply to prose content. Validation is:

- **Structural parity check**: both files have the same 13 headings (0-12
  plus closing) in the same order.
- **Compliance check** against the non-negotiable rules already documented
  in this repo's `CLAUDE.md` (no diagnosis by non-clinical staff, no
  prospective ROI, fixed operating sequence preserved, referral never
  delayed by organizational measures) — the rewritten EN and the reworded
  PT-BR must still satisfy all of them.
- **Human review**: the repo owner (a licensed ophthalmologist) reviews the
  clinical/legal content before merge — not delegable.
- **Commit gate**: per the user's standing instruction, no `git commit`
  happens without explicit permission at each step (spec, plan,
  implementation).

## Open questions

None outstanding — all decisions above were confirmed with the user during
brainstorming.
