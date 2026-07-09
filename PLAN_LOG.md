# PLAN_LOG

## 2026-07-08 (3) — Mobility Program case-study training page (case-studies-mobility.html)

**Task.** Complete the case-study set with a Mobility Program quiz. The plan is simpler
(cash-balance-only), so 5 cases / 24 checkpoints: who's covered (Orange Contract bargained;
legacy mgmt employed 12/31/2005) and single-account structure (no greatest-of, no pension
Mod 75, flat NRA 65); mechanics (flat 5% Basic Benefit Credit, broad Pension Compensation,
quarterly 30-Yr Treasury interest that continues after termination); payment forms (SLA =
account / 141.5292 example, 50/75% J&S only, pop-up always applies, 90%-of-SLA floor for
pre-2006 participants, no QDRO waiver); rates and rollover (lump sum = account, NOT
segment-rate-converted, 20% withholding vs direct rollover, Rule of 55, $7,000 cash-out);
healthcare and survivors (Medical Program's own Rule-of-75-style test still applies, post-2001
hires pay 100%, no Retiree Death Benefit; estate default).

**Source of truth.** All facts mirror the SPD-verified content of `mobility.html`, including the
SPD's own annuity-factor worked example. Several questions deliberately contrast the legacy
plans' rules (rate timing, pop-up condition, death benefit).

**Files.** New `case-studies-mobility.html` (same engine/visual system); nav link + strategy
callout in `mobility.html`; footer cross-links in `case-studies.html` and `case-studies-nb.html`.

**Risks.** Don't import legacy rules (segment-rate timing, Mod 75 pension subsidy, 100% J&S,
death benefit). Numeric tolerance for rounding. Keep the shared visual system.

**Next steps.** Build page → validate in preview (flow, math, responsive) → push → CHANGE_LOG.

## 2026-07-08 (2) — Legacy Non-Bargained case-study training page (case-studies-nb.html)

**Task.** Mirror the union case-studies page for the Nonbargained (management) plan, testing the
concepts that differ from (and get confused with) the union rules: which program applies and
greatest-of-three (not a sum); CAM formula math (1.6% x CAM Income / 12, two-piece CAM Income);
the frozen cash balance (pay credits stopped 1/14/2005, interest only, lump-sum lever); NB Mod 75
(0.25%/mo with 30+ yrs before 55, NOT fully unreduced; 0.5%/mo under 30; flat age-55 threshold;
CAM/PBM only; J&S pop-up gated on Mod 75); lump-sum paths (post-2018 full lump sum vs CAM Excess
Calculation, $400/mo test) and segment-rate timing; severance vs Mod 75 timing (4%/yr capped 50%
at 13+); healthcare (2022 management pre-Medicare subsidy elimination) and the Retiree Death
Benefit (greater-of, 10%/yr decay, 1-year claim deadline).

**Source of truth.** All facts mirror the SPD-verified content of `non-bargained.html`; the CAM
Excess numbers reuse the SPD's own worked example. No new plan claims.

**Files.** New `case-studies-nb.html` (same engine/visual system as `case-studies.html`);
nav link + strategy callout in `non-bargained.html`; footer cross-link in `case-studies.html`.

**Risks.** Do not import union-only rules (30+ yrs unreduced at any age, 55/56 split, additive
formulas). Numeric tolerance for rounding. Keep the shared visual system.

**Next steps.** Build page → validate in preview (flow, math, responsive) → push → CHANGE_LOG.

## 2026-07-08 — Advisor case-study training page (case-studies.html)

**Task.** Build an interactive case-study page that tests an advisor's knowledge of the AT&T
union plan: Mod 75 (pairs vs. sum, tested-at-termination), early-commencement reduction math
(0.5%/mo, 55 vs. 56 threshold), Pre-99 pension-band calculation, cash-balance mechanics,
interest-rate effects on lump sums (segment rates, prior-November lock), and retiree healthcare
(enroll vs. subsidize, 2001 hire-date rule, 2021 Medicare-subsidy elimination). The advisor must
answer (numeric input or multiple choice) to advance; questions gate sequentially and cases
unlock in order. Link the page from `index.html`.

**Source of truth.** All facts and figures come from the already-SPD-verified content of
`index.html` (sections 04–08, 10) — no new plan claims are introduced. Every answer explanation
links back to the relevant guide section.

**Files.** New `case-studies.html`; nav link + strategy-section callout in `index.html`.

**Risks.** Numeric answers must tolerate rounding (accept small tolerances, strip $/%/commas);
must not contradict the guide (e.g., 30+ yrs = unreduced at any age; cash balance never
rate-converted or reduced). Keep the union guide's visual system.

**Next steps.** Build page → validate in preview (flow, math, responsive) → push → CHANGE_LOG.

## 2026-07-01 — Non-Bargained (management) resource page

**Task.** Build a dedicated resource page for AT&T Non-Bargained (non-union / management)
employees that mirrors the existing union guide (`index.html`), using the Management SPDs in the
project library.

**Source of truth (verified by reading the PDFs directly with pdftotext):**
- `Management SPDs/202010---SPD---Nonbargained-Program...-78-49754 (1).pdf` (2020, current)
- `Management SPDs/ATT Non Bargained Pension SPD (1).pdf` (2017, superseded)
- `Management SPDs/Mobility-Program-of-the-ATTWarnerMedia... (1).pdf` (2020) — only the
  management-relevant portions are referenced.

**Key structural differences from the union guide (must be reflected accurately):**
1. Pension benefit = **greatest of** three formulas (CAM / Cash Balance / PBM), *not* a sum.
2. **CAM Formula** (1.6% × CAM Income ÷ 12) is the primary/active formula for most.
3. **Cash Balance Formula is FROZEN** — basic benefit credits stopped Jan 14, 2005; only
   interest credits continue (30-Year US Treasury rate). No age-credit-factor table exists in
   these SPDs (SPD directs to Recordkeeper).
4. **PBM Formula** for PBM Eligible Participants (promoted from a Banded Program ≥ Jun 13, 2001).
5. **Mod 75** applies to CAM/PBM only (not Cash Balance). Reduction before age 55 = 0.5%/mo, or
   **0.25%/mo with 30+ years** (not fully unreduced as in the union Pre-99 rules). Threshold is a
   flat age 55 (no 55/56 contract split).
6. Forms: SLA, 50% J&S (90%), 75% J&S (85%), **100% J&S (80%)**. Pop-up only if Mod 75 met.
7. **Full lump sum** if terminated ≥ May 25, 2018 and BCD ≥ Jun 1, 2018; else CAM Excess Calc.
8. **Retiree Death Benefit** — unique to the Nonbargained Program (Wages-based, lump sum).
9. NRA = 65 or 5th anniversary of participation (later). Vesting = 3 years.

**Files.** New `non-bargained.html`; cross-link added in `index.html` nav. Tracking files added.

**Risks.** Do not reproduce union-specific figures (age credit factors, 55/56 split) that don't
apply here. Frozen cash-balance mechanics are historical and not fully documented in the SPD —
flag and direct to Recordkeeper rather than inventing numbers.

**Next steps.** Build page → validate (open, check responsive, calculator) → push → CHANGE_LOG.
