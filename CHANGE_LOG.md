# CHANGE_LOG

## 2026-07-02 — Authoritative source links + annual-figures reference

**Summary.** Added IRS.gov / Medicare.gov / SSA.gov links next to every tax-year-specific figure
in the three guides, verified the 2026 values against the official sources, and created a
maintenance reference file listing every figure that must be updated each tax year.

**Verification of 2026 figures (against official sources, 2026-07-02):**
- 402(g) $24,500 · 415(c) $72,000 · catch-up $8,000 · super catch-up (60–63) $11,250 · totals
  $32,500 / $35,750 / $80,000 / $83,250 — all confirmed via IRS Notice 2025-67 / IRS newsroom.
  (Confirmed the 60–63 super catch-up correctly *stays* $11,250 for 2026, not 150% of $8,000.)
- IRMAA 2026 thresholds $109,000 single / $218,000 MFJ, 5 tiers (top $500k / $750k) — confirmed.
- Social Security wage base 2026 = **$184,500**. The union guide showed a stale "$168,600 in
  2024"; corrected the figure and its worked example ($189,500 YTD / $184,500 base).

**Links added.**
- 401(k) footnote (all 3 pages): added the IRS COLA limits-table link alongside the existing
  401(k) topic-page link; labeled the figures "for 2026."
- IRMAA paragraph (all 3 pages): added a Medicare.gov "Medicare costs & IRMAA" link and the
  top-tier thresholds.
- Union Supplemental Pay Credit: added an SSA "contribution & benefit base" link.

**New file.** `ANNUAL-TAX-FIGURES.md` — a per-tax-year update checklist: every indexed figure with
its 2026 value, where it appears, the authoritative source URL, and grep-able search strings, plus
a "figures that are statutory / don't change yearly" section.

**Link health.** medicare.gov and both IRS pages return 200; ssa.gov cbb.html 403s to automated
clients (anti-bot) but is the canonical page and loads in a browser.

## 2026-07-01 (3) — Split into three plan guides + left-rail plan selector

**Summary.** Added a "Viewing plan" dropdown to the left rail of every guide (Union / Legacy
Non-Bargained / Mobility Program) and split the content so each population has a clean, dedicated
page without cross-plan comparison clutter.

**Files.**
- `mobility.html` (new) — standalone AT&T Mobility Program guide (12 sections): cash-balance-only
  pension (5% basic benefit credit + 30-yr-Treasury interest), no Mod 75, SLA/50/75 J&S with
  always-on pop-up (no 100% J&S), lump sum = account, 401(k), IRMAA, and a retiree-healthcare
  section explaining that the Medical Program's own age/service test (not the pension) gates
  retiree-medical access.
- `non-bargained.html` — retitled to "Legacy Non-Bargained"; added the plan dropdown; removed the
  Mobility comparison cards and the inline Mobility difference note (now its own page). Section 02
  slimmed to a short "which guide" table + pointer.
- `index.html` — added the plan dropdown (replaced the earlier single "Switch guide" link + CSS).

**Nav mechanism.** Each page's `<select id="planSel">` marks its own page `selected` and navigates
on change (`window.location.href`). Styled to match the dark sidebar with a gold caret.

**Verified (DOM parse of all three served pages + live eval):** dropdown present with correct
selected option and all 3 targets; every sidebar anchor resolves (14 Union / 17 Legacy NB / 12
Mobility); Mobility content present; no console errors; the Legacy NB Mod-75 calculator still
computes correctly (6% for 53/30 met; Appendix B / Not eligible for 52/22). Screenshot capture was
flaky in this session (backgrounded renderer reporting 0-width); layout parity is high-confidence
since all three pages share the identical, previously screenshot-verified stylesheet.

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
