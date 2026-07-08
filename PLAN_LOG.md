# PLAN_LOG

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
