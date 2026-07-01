# CHANGE_LOG

## 2026-07-01 (2) — Fill 401(k) and retiree-medical gaps from new SPDs

**Summary.** Two SPDs were added to `Management SPDs/` (`ATT-Retirement-Savings-Plan_78-63233.pdf`,
`Medical SPD 2021.pdf`). Updated `non-bargained.html` to replace "verify, not in library" placeholders
with facts sourced directly from these documents.

**401(k) (Section 11), from the Retirement Savings Plan SPD:**
- Real match tiers: 80% of first 6% (default), or 133⅓% of first 3% + 100% of next 3% (~7% of pay)
  for management hired/rehired on/after 1/1/15. Match on first 6% only; catch-up not matched.
- Match eligibility upon hire; match in AT&T Shares with immediate diversification; 100% vested after
  3 Years of Service (auto at death/disability/age 65).
- Mega-backdoor confirmed: after-tax contributions permitted + Roth In-Plan Rollover (irrevocable).
- No "true-up" described in the SPD, front-loading caution retained and grounded accordingly.

**Retiree medical (Section 08 + calculator), from the Medical Program SPD:**
- Confirmed Mod 75 (same table) at termination is the gate to retiree ("Post-Employment") medical
  eligibility for former Management/Bargained/Nonmanagement-Nonunion employees.
- Compliance correction: changed "subsidized retiree medical" to "eligible to enroll," since the
  retiree pays a monthly contribution and the company subsidy varies by group/hire date (up to 100%
  of cost for some). Added the pre-Medicare-bridge nuance (coverage ends at Medicare eligibility,
  transition to private exchange + possible Part B/D premium reimbursement) and the legacy
  Pension-Based Eligibility path.
- Calculator healthcare card relabeled "Eligible to enroll" / "Not eligible" with accurate detail.

**Sources section** updated to cite both new SPDs. **Verified:** calculator re-tested (3 cases),
content assertions confirmed present in the served page.

**Note.** The two new source PDFs are large binaries and were left untracked (only referenced).

## 2026-07-01 — Add Non-Bargained (management) resource page

**Summary.** Added a dedicated advisor field guide for AT&T Non-Bargained (non-union / management)
employees, mirroring the existing union guide's design and structure but with content accurate to
the Nonbargained Program SPD.

**Files.**
- `non-bargained.html` (new) — 17-section guide reusing the union guide's stylesheet.
- `index.html` — added a reciprocal "Switch guide" nav link (+ `.switch` CSS) and footer link.
- `PLAN_LOG.md`, `TODO.md`, `CHANGE_LOG.md` (new) — project tracking files.
- `.claude/launch.json` (new) — static-server config for local preview.

**Content accuracy (verified against the SPD PDFs, not just the consolidated summary).**
- Pension = **greatest of** CAM / Cash Balance / PBM (not a sum, unlike the union guide).
- CAM = 1.6% × CAM Income ÷ 12 (primary/active formula).
- Cash Balance is **frozen** (pay credits stopped Jan 14, 2005; interest-only thereafter); no
  age-credit-factor table reproduced because the SPD does not publish one.
- PBM scoped to Banded-Program promotions on/after Jun 13, 2001.
- Mod 75 (CAM/PBM only): reduction before age 55 = 0.5%/mo, or 0.25%/mo with 30+ years; flat
  age-55 threshold (no 55/56 split).
- Forms: SLA + 50/75/100% J&S (90/85/80%); pop-up only if Mod 75 met.
- Full lump sum (post-May-25-2018) and CAM Excess Calculation both documented.
- Retiree Death Benefit section (Nonbargained-only feature).
- Mobility management differences summarized; Management Cash Balance Program gap flagged.

**Tests / validation.**
- Served locally; calculator logic verified across 4 cases (Mod 75 thresholds, 0.25%/0.5% rate
  split, flat age-55 threshold) — all correct.
- All 17 sidebar anchors resolve; both cross-links (index ↔ non-bargained) and footer link work.
- No horizontal overflow; responsive sidebar collapse confirmed below 980px.

**Status.** Complete.

**Known issues / follow-ups.** See `TODO.md` — Management Cash Balance Program SPD, 401(k) plan
specifics, and retiree-healthcare SPDs are not yet in the library and are flagged in-page.
