# CHANGE_LOG

## 2026-07-08 (2) — Legacy Non-Bargained case studies (case-studies-nb.html)

Companion to the union case-studies page: **six client scenarios (30 checkpoints)** built around
what makes the Nonbargained (management) plan different, and where union-trained advisors slip.
Same engine and visual system as `case-studies.html` (gated numeric/multiple-choice checkpoints,
hint after one miss, reveal after two, first-attempt scoring, miss-list with review links, reset).

Coverage: (1) which program applies + greatest-of-three, not a sum (CAM $2,800 vs $95k cash
balance; Mod 75 attaches to CAM/PBM only); (2) CAM math ($70k × 12 = $840k pre-2000 piece,
$2.4M CAM Income, 1.6%/12 → $3,200/mo; still accruing vs the frozen CB); (3) the two lump-sum
doors (frozen-since-1/14/2005 interest-only CB; post-2018 full lump sum; SPD's CAM Excess
example: $180k − $90k → $500/mo ≥ $400 → partial $90k lump sum + residual annuity; segment-rate
exposure on CAM only); (4) NB Mod 75 vs the union rule (30+ yrs is NOT unreduced at any age here:
0.25%/mo before 55 → 36 mo = 9% → $2,730; under 30 yrs 0.5%/mo → 18%; pop-up gated on Mod 75);
(5) severance vs Mod 75 timing (50% cap → $65,000 vs 1 more year to 50/25; taxable, not
rollable); (6) healthcare + Retiree Death Benefit (same Mod 75 gate; management pre-Medicare
subsidy gone for last day ≥ 1/1/2022 regardless of hire date; greater-of $120k × 0.70 = $84,000
vs $2,900 × 12 = $34,800; fixed beneficiary order; one-year claim deadline). All facts mirror the
SPD-verified `non-bargained.html`; explanations deep-link its sections.

**Links:** "Training" nav item + Strategy Playbook callout in `non-bargained.html` (plain anchor,
kept off the `.navitem` observer); footer cross-link in `case-studies.html`; the NB page footer
links back to the union case studies.

**Validated in preview:** no console errors on either page; wrong/right MC flow; all 30
checkpoints solvable with the authored answer key (every numeric value accepted exactly); score
29/30 after one deliberate miss; every MC has exactly one correct option; reset re-locks cases;
all nine deep-link anchors exist in `non-bargained.html`; its Mod 75 calculator and nav observer
still run; no horizontal overflow at desktop or 375px mobile. Design-hook findings are the
documented intentional visual-system exceptions (TODO.md note extended).

**Files:** `case-studies-nb.html` (new), `non-bargained.html`, `case-studies.html`,
`PLAN_LOG.md`, `TODO.md`. Pushed as b9c641c.

## 2026-07-08 — Interactive advisor case studies (case-studies.html)

New standalone training page with **six client case studies (30 checkpoints)** testing the
concepts advisors most often get wrong. The advisor must calculate (numeric input) or choose
(multiple choice) correctly to advance; questions gate sequentially within a case and cases
unlock in order. Wrong picks lock out with an explanation of the specific misconception; numeric
questions give a hint after one miss and a reveal option after two. First-attempt answers score,
and a results screen links every miss back to the guide section to review.

Coverage: (1) Mod 75 pairs-vs-sum + tested-at-termination + deferred-vested consequences;
(2) early-commencement reduction math (0.5%/mo, 24 mo → 12% → $1,232, West 55 vs Southeast 56,
cash balance unaffected); (3) Pre-99 pension-band arithmetic ($51.81 × 17 × 1.06 = $933.62,
supplemental $10.20, service-as-of-12/31/1998 trap); (4) cash-balance mechanics (age credit
factors, $164 pay credit, $293.60 interest credit, wage-base Supplemental Pay Credit);
(5) segment rates and the lump sum (inverse relationship, prior-November calendar-year lock,
Dec-vs-Jan commencement, cash balance not rate-converted, 20% withholding vs direct rollover);
(6) retiree healthcare (enroll-vs-subsidize, 2001 hire-date rule, 2021 Medicare-subsidy
elimination, pre-65 bridge value, deferred-vested = no enrollment). All facts mirror the
SPD-verified content of `index.html`; every explanation deep-links the relevant guide section.

**Links added in `index.html`:** a "Training" nav item (plain anchor, kept off the `.navitem`
scroll-observer to avoid an invalid-selector throw) and a callout at the end of the Strategy
Playbook (Section 11).

**Validated in preview:** no console errors; wrong/right MC flow, hint + reveal flow, tolerant
number parsing ("$ 2 ", commas, %), case gating/unlock, 30/30 solvable with the authored answer
key, first-try scoring (28/30 after two deliberate misses), miss-list links, reset; index nav +
callout links resolve; no horizontal overflow at desktop or 375px mobile. (Preview screenshot
tool timed out repeatedly; verification done via DOM snapshot/inspect/eval instead.) Design-hook
findings are the documented intentional visual-system exceptions (see TODO.md).

**Files:** `case-studies.html` (new), `index.html`, `PLAN_LOG.md`, `TODO.md`. Pushed as a4643d5.

## 2026-07-02 (6) — Merge the two "unreduced" Mod 75 cards back to one

The 30+ years and "under 30 yrs, at/after threshold age" cards produce the *same* employee benefit
(a fully unreduced pension), so they were merged into a single "Meets Mod 75 & threshold age /
Unreduced" card. Back to three cards on the standard 3-column grid (removed the temporary
`.compare.grid2` CSS). Kept the body explicit about both paths, 30+ years is unreduced at any age
(threshold not required); under 30 years is unreduced once at/after 55/56, so a 30+-year client below
the threshold age doesn't misread the heading as a requirement.

## 2026-07-02 (5) — Add the missing Mod 75 scenario (Union guide)

The "What Mod 75 changes on the Pre-99 benefit" comparison (Section 06) was missing a distinct
outcome: <strong>Mod 75 met, under 30 years, at/after the threshold age</strong> = fully unreduced
(same result as 30+ years, reached via age rather than service). It had been buried as a sub-bullet
inside the "before threshold age" card. Broke it out into its own card, so the comparison is now four
scenarios: (1) Mod 75 met, 30+ yrs (unreduced at any age); (2) Mod 75 met, under 30 yrs, at/after
threshold age (unreduced via age); (3) Mod 75 met, under 30 yrs, before threshold age (0.5%/mo
reduction); (4) does not meet Mod 75 (penalized). Switched this block to a 2×2 grid (new
`.compare.grid2` class with a mobile 1-column override). Verified 2 columns at desktop, 1 at mobile,
no overflow.

## 2026-07-02 (4) — Clarify the "30+ years" Mod 75 card (Union guide)

In the Union guide's "What Mod 75 changes on the Pre-99 benefit" comparison (Section 06), the first
card said only "30+ years of service" while the other two referenced Mod 75, reading like a separate
category. Relabeled it "Mod 75 met, 30+ years of service" and added that it satisfies Mod 75 via the
any-age + 30-year combination and is unreduced at **any** age (the threshold age doesn't apply).
Declined to add "meets threshold age" as literally suggested, since 30+ years is unreduced regardless
of age, so implying the client must reach 55/56 would be inaccurate. Union guide only; the Legacy
Non-Bargained card already references Mod 75 and follows that plan's different 0.25%/mo rule.

## 2026-07-02 (3) — Lump-sum rate timing (A1), Rule of 55 (A2), 401(k) loan handling (A3)

Implemented the remaining Priority-A items from `REVIEW-Jordan-Notes-vs-Guides.md`.

**A1 — Lump-sum interest-rate / segment-rate timing.** Added a "Timing the lump sum around interest
rates" callout to the payment sections of the **Union** and **Legacy Non-Bargained** guides: a
defined-benefit annuity-to-lump-sum conversion uses IRS minimum present-value segment rates and moves
inversely to rates; AT&T locks the prior-November rates for the commencement calendar year. Linked
the IRS segment-rate page. Added the contrasting "no interest-rate timing to worry about" note to the
**Mobility** payment section (its lump sum is the account, not rate-converted).

**A2 — Rule of 55.** Added a callout (all 3 guides, 401(k) section): separating in the year one turns
55+ allows penalty-free 401(k) withdrawals in-plan, and **rolling to an IRA forfeits it** (back to
59½). Note the plan may limit how withdrawals are taken.

**A3 — 401(k) loan at separation.** Added a callout (all 3 guides): pay off (allow ~72h to post),
default (1099-R taxable distribution + possible penalty), or keep (leave enough balance). Grouped
A2+A3 under a new "At separation: two traps to handle" subheading.

**Verified:** all 3 pages parse clean (no broken anchors; sections 14/18/12); IRS segment link on
Union + Legacy NB; Rule-of-55 and 1099-R present on all 3; Mobility carries the contrast note only;
NB Mod-75 calculator still computes (58/31 → "None", "Eligible to enroll").

## 2026-07-02 (2) — Retiree-medical rewrite (A4), $7,000 cash-out (SMM), severance section

Implemented the reviewed items from `REVIEW-Jordan-Notes-vs-Guides.md` after the Bargained SPDs,
Medical SPD, 2024 SMM, and Severance Pay Plan were confirmed as controlling sources.

**A4 — Retiree-medical subsidy (all 3 guides).** Rewrote the retiree-healthcare sections to
distinguish *coverage eligibility* (Mod 75, unchanged) from *subsidy* (largely eliminated), per the
Medical Program SPD (2021) + the Dec 2020 Retiree Benefit Changes announcement:
- Hired on/after 1/1/2001 → 100% of cost (no subsidy).
- Management pre-Medicare subsidy eliminated for last day on/after 1/1/2022.
- 65+ Medicare subsidy eliminated for bargained *and* management for last day on/after 1/1/2021.
- Corrected the Union guide's over-optimistic "subsidized" framing; sharpened the Legacy
  Non-Bargained and Mobility "up to 100% of cost" callouts with the concrete dates.
- Added **Alight** (retiree-health enrollment) to the contacts on all three pages.

**NEW-1 — Mandatory cash-out $5,000 → $7,000 (all 3 guides).** Per the July 2024 SMM (NIN 78-72720),
effective Jan 1, 2024, across all programs. Corrected the small-benefit cash-out callouts.

**NEW-2 — Severance & surplus section (Legacy Non-Bargained only).** New Section 14 documenting the
AT&T Severance Pay Plan (management): allowance = % of Annual Basic Pay by TOE (4%/yr, capped 50% at
13+ yrs), tied to the Mod 75 "should I leave now?" decision. Renumbered subsequent sections (15–18)
and added the nav entry. Added the Severance Pay Plan, 2024 SMM, and Dec 2020 changes to Sources.

**Verified:** all three pages parse clean (no broken anchors; NB nav now 18 items ending at
Section 18 Contacts); the NB Mod-75 calculator still computes (51/26 → ~24%, "Eligible to enroll");
$7,000, A4 subsidy language, and Alight present on all pages.

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
