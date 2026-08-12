# PLAN_LOG

## 2026-08-12 (2) — Union guide §09: real match formulas + company match calculator

**Task.** Replace the union guide's generic company-match copy with the documented formulas from
`Bargained SPDs/ATT-Retirement-Savings-Plan_78-63233.pdf`, and add a match calculator modeled on
the Section 07 Mod 75 calculator with a contract-family selector.

**Source facts (pdftotext of the ARSP SPD, Benefits at a Glance p.13–14 and the Amount of Employer
Contributions section p.25–27):**
- Baseline match is **80% of the first 6%** of Compensation elected as Basic Contributions.
- Special rules: 100% of first 6% (Mobility Black CWA D3 on/after 1/1/15, Mobility Blue IBEW 1547
  on/after 1/1/12); 133⅓% of first 3% + 100% of next 3%, max 7% (Technical Services, nonmanagement
  nonunion following CWA/AT&T Core on/after 1/1/15); 75% of first 6% (AT&T Corp. Core CWA hired
  before 8/9/09); 66⅔% of first 6% (AT&T National Contract IBEW SC T-3 hired before 8/9/09,
  Teamsters Local 959 Alascom); 25% of first 6% (BellSouth Utility Operations hired/rehired after
  8/8/09).
- **Match eligibility is one Year of Service unless noted.** Upon hire applies only to Management,
  Mobility Orange (CWA D1, 2-13, 4, 7, 9), Mobility Purple (CWA D6), Mobility Black (CWA D3), and
  National Internet Tier 1 CWA. This corrects the guide, which implied upon-hire generally.
- Match is allocated to the **AT&T Shares Fund** except for Technical Services, Legacy T-IBEW
  (hired on/before 8/8/09), and Cricket/AIO, whose match follows the employee's own funds.
  Diversification is **immediate and unlimited**, up to 100%, vested or not.
- Vesting 100% after 3 Years of Service; automatic at death, disability, or age 65. Catch-up
  contributions are never matched. Basic Contributions allowed up to 50% of Compensation.
- SPD's own worked example for the tiered formula: 3% contribution → 4% of pay; ≥6% → 7% of pay.
  Used to validate the calculator.

**Known source limits to state on the page.** The SPD in the library is a **2022 edition** (its
deferral limit is the 2022 figure) and match tiers come from the bargaining agreement, so a newer
contract can change them. The detailed section calls the Purple Contract "CWA District 3" while
the at-a-glance table says District 6; District 6 is used (it matches the pension guide's contract
mapping) and the discrepancy is flagged on the page.

**Files.** `index.html` only (the union guide). The management and Mobility guides already carry
their own correct match tiers and are out of scope for this request.

**Risks.** The match spread is 1.5% to 7.0% of pay across groups, so a wrong tier is a materially
wrong number in a client meeting: every tier must be traceable to the SPD, and the page must push
the advisor to verify in NetBenefits. The calculator annualizes a level rate while the real match
is per pay period with no true-up, so that assumption has to be stated, not buried.

**Next steps.** Build table + calculator → validate every formula against the SPD, including the
tiered worked example → responsive check → push → CHANGE_LOG.

## 2026-08-12 — ARSP Roth / non-Roth investment enhancements + BrokerageLink blackout

**Task.** Add the September 2026 AT&T Retirement Savings Plan (ARSP) change to the three plan
guides, sourced from `Roth-Investing-Account-Notice_Pages_1-21.pdf` (Fidelity SMM / Prospectus
Supplement and ERISA blackout notice, issued against the July 2026 SPD).

**Source facts (read directly from the PDF, pages 1–21):**
1. Effective **Sept 21, 2026**: Roth and non-Roth balances can carry separate investment elections
   in the Standard Plan Options; every BrokerageLink account splits into **BrokerageLink**
   (non-Roth) and **BrokerageLink Roth**.
2. **Blackout**: ~4 p.m. ET Sept 14, 2026 through ~9:30 a.m. ET Sept 22, 2026. No purchases and no
   exchanges into/out of BrokerageLink; sell orders allowed, settling to Fidelity Government Cash
   Reserves. Open orders canceled on/about Sept 14 after 4 p.m. ET, not re-established. Standard
   Plan Options unaffected.
3. Online BrokerageLink account opening restricted Sept 14–21; paper applications held until after
   Sept 21.
4. Features that do **not** carry to the Roth account: third-party authorization (explicitly
   including advisor access), automatic investment of payroll contributions, dividend reinvestment
   elections. Cost basis does not carry over (no effect on distribution tax treatment).
5. Split methodology: Roth balance (cost basis of Roth contributions + earnings, priced two
   business days prior) ÷ balance of eligible divisible securities = **Roth percentage**, prorated
   across holdings. Excluded: rights/warrants, fractional shares outside the dividend reinvestment
   program, unpriced/worthless securities, restricted securities. Rounding: equities and mutual
   funds 3 decimals, core cash 2, fixed income down to the nearest 1,000 units (under 1,000 units
   excluded). Overage/shortage up to $100 trued up in core cash; over $100 triggers a second
   proration. A 100% Roth account transfers entirely in kind.
6. Forced liquidation: if a holding cannot be split, Fidelity attempts contact; **if the client has
   not acted by Sept 14, 2026, AT&T has directed Fidelity to sell on their behalf**. Order: mutual
   funds (highest balance, then highest share price), equities (same rule), then fixed income
   (lowest market value first; bonds before CDs). Usually ≤ $3.00; larger amounts limited to the
   amount needed plus a 10% buffer. Trade costs and realized gain/loss borne by the existing
   BrokerageLink account; commissions waived while administratively feasible.
7. Side effects: round lots can become odd lots; trailing dividends stay in the existing account; a
   resulting position under one total share is liquidated unless the client opted into fractional
   share trading.
8. Fidelity BrokerageLink line: **(800) 890-4015**, Mon–Fri 8:30 a.m.–8 p.m. ET.

**Files.** `index.html`, `non-bargained.html`, `mobility.html` (new subsection inside the existing
Savings Plan section, glossary terms, contacts/sources line). `triggers.html` gets a short
plain-language client-facing version of the same notice. Tracking files updated.

**Risks.** Do not renumber sections or nav (the change is a subsection inside `#savings`, not a new
numbered section). Do not state which savings plan a bargained client is in: the notice names the
ARSP, so the union guide must tell the advisor to confirm the client's plan first. Keep all dates
and dollar thresholds exactly as printed. No investment advice: the notice itself carries an
explicit "not a recommendation" statement about how to invest Roth vs non-Roth balances, so the
guide describes mechanics and flags the decision rather than recommending an allocation.

**Next steps.** Write subsections → validate in preview (desktop + mobile, no overflow, nav intact)
→ push → CHANGE_LOG.

## 2026-08-11 — Rename the tool: "Financial Trigger Finder" -> "Client Milestones"

**Task.** Update every reference to the tool's name across the site.

**Scope.** `triggers.html`: `<title>`, hero `<h1>`, the sidebar "Viewing" selector option, the footer
title line, and two internal JS comments. Sidebar "Plan Guides" link label on `index.html`,
`non-bargained.html`, and `mobility.html` ("Financial trigger finder" -> "Client Milestones"). The
email export also carried the old naming: heading "AT&T Retirement Trigger Timeline: Upcoming
Milestones" -> "AT&T Retirement Timeline: Your Upcoming Milestones", the "Trigger" column header ->
"Milestone" (HTML and plain-text variants), and the popup-fallback tab title.

**Left unchanged.** The filename `triggers.html` and all four `href="triggers.html"` links, so the
published URL and any existing bookmarks keep working. Every remaining occurrence of "trigger" in
the guides is the ordinary verb (a lump sum *triggers* 20% withholding, crossing an IRMAA threshold
*triggers* the full surcharge, a rollover can *trigger* a loan default) and is correct as written.

**Validated in preview:** page renders with no console errors; title, `<h1>`, footer line, and the
sidebar selector all read "Client Milestones"; the calculator still computes (result cards render
for the default union/active case); export handler runs (clipboard/popup are blocked in the
automated file:// context, which is an environment limit, not a code error).

## 2026-07-23 (3) — Trigger Finder: rewrite all copy to plain, client-facing language

**Task.** Review the Financial Trigger tool (`triggers.html`) so the language is very basic and
written for the client (second person "you") rather than the advisor.

**Scope.** Rewrote every user-visible string: hero eyebrow/lead/meta, Section 01 inputs (heading,
intro, labels, status/entry radios, separation label + dynamic JS label, warn callout), Section 02
timeline heading/intro + export link text, Section 03 heading/intro + the "advisor's lens" box
(reframed to "Why your last day matters most"), Section 04 reference heading/intro/table/footnote,
footer descriptive + disclaimer lines and the footer title, and the sidebar section labels. In the
JS engine: input-error banners, the client snapshot line, all four result cards, every timeline
item (title + description), the timeline footnote, the separation-checklist intro and all six
steps, the closing note, and the email-export prose/messages.

**Plain-language choices.** Jargon translated in place while keeping accuracy and every hedge:
Mod 75 -> "Rule of 75"; combos "50/25" -> "age 50 with 25 yrs"; MAGI/IRMAA -> "your income" /
"Medicare surcharge"; 402(g)/415(c) -> "standard limit"; QCD kept with plain gloss; segment rates
-> "the interest rates used to set a lump sum"; deferred-vested/Appendix B factors -> "bigger
cuts"; commence -> "start your pension"; NUA -> "a special tax break for company stock (NUA)".
"the client / they" -> "you"; "before advising" -> "before you decide / talk with your advisor".
Kept the export table's requested column headers (Age, Approx. Date, Trigger, Description).

**Left intentionally.** Shared sidebar brand line ("Advisor Field Guide") and two internal JS code
comments that still say "Mod 75" (not user-visible). Calculation logic, dates, dollar figures,
and all disclaimers unchanged.

**Validated in preview:** no console errors (JS parses); default (union/active), Mobility, and a
terminated-management "missed milestone" scenario all render plain second-person copy; dynamic
separation label flips to "When you left AT&T"; email export still copies (14 milestones, updated
subtitle, columns intact); no horizontal overflow at desktop or mobile (375px); em-dash grep 0.

## 2026-07-23 (2) — Trigger Finder: export future triggers as an email-ready table

**Task.** Add a link on `triggers.html` (Section 02, Trigger timeline) that exports the timeline's
**future** triggers as a formatted table for pasting into a client email. Columns: Age, Approx.
Date, Trigger, Description.

**Approach.** The timeline is built in `render()` into an `items` array (`{d,cat,catCls,title,
desc,warn}`). Exposed the latest build via module-scoped `lastItems`/`lastDob` (cleared at the top
of `render()` so the two invalid-input early returns leave them empty; repopulated right after
`items.sort`). New "Copy future triggers as a table (for client email)" link + status span under
the section intro. `buildExport()` filters `items` to `d >= today`, builds an HTML table with
**inline styles only** (survives Outlook/Gmail paste, which strip `<style>`/classes) plus a
tab-separated plain-text twin. `copyPayload()` tries `navigator.clipboard.write` (rich HTML), then
an `execCommand('copy')` rich-selection fallback, then opens a new tab with the table for manual
copy. Age/date reuse the timeline's own `yrs`/`fmt` formatting for consistency.

**Risk.** Clipboard API needs a secure context + user gesture (fine on GitHub Pages https and on a
real click); covered by the execCommand and new-tab fallbacks. Client-facing copy: table uses
Arial (email-safe) and carries a short "planning aid, not advice; verify" footnote. Title uses a
colon, not an em-dash, per the project style rule.

**Validated in preview:** default client (age 52, Union) copies 13 future triggers; captured
clipboard HTML has exactly the 4 columns and 13 rows (first = Rule of 55 / age 54.4 / Jan 2029,
last = RMDs / age 75 / 2049); plain-text twin present; age-92 client shows the "no future triggers"
guard (err style); no console errors; no horizontal overflow at desktop or mobile (375px); em-dash
grep 0.

## 2026-07-23 — Client Examples across all three guides + non-bargained nav fix

**Task.** (1) Using the PGE Benefit Resource Guide as the pattern, add a recurring-client "Client
example" callout to each teaching section of all three AT&T guide pages (`index.html` Union,
`non-bargained.html` Legacy Non-Bargained, `mobility.html` Mobility). (2) Fix the two Left-Rail
links on `non-bargained.html` ("Financial trigger finder", "Case studies") that were missing
`class="navitem"` and therefore rendered unstyled.

**Pattern (from PGE).** New CSS: `--client:#6E4B9E` var + `.callout.client{border-left-color:
var(--client);background:#f2ecf8}` and `.callout.client .tag{color:var(--client)}`. Markup:
`<div class="callout client"><span class="tag">Client example: NAME</span><p>…</p></div>`.
Recurring characters per page, numbers computed from that section's own formulas:
- Union: Rosa Alvarez (CWA D9/West, hired 1990, blended Pre-99 + cash balance) + Marcus Bell
  (IBEW, hired 2012, cash-balance only).
- Non-Bargained: Karen Whitfield (legacy SBC mgmt, hired 1988, CAM controlling) + Dennis Okafor
  (promoted from Midwest band 2003, PBM) in the PBM section.
- Mobility: Tanya Brooks (CWA Orange, hired 2010, cash-balance only).

**Risk.** Financial-copy accuracy: every worked number must tie to the section's stated
formula/factors and stay hedged/illustrative ("confirm in NetBenefits"). Mitigated by reusing each
section's own example figures/factors. Nav fix is cosmetic (class only), low risk.

**Next steps.** Verify in preview (desktop + mobile, nav styling, no overflow), em-dash grep = 0,
update CHANGE_LOG + push.

## 2026-07-20 (4) — Trigger Finder: MOD 75 card, FRA relabel, radio reorder

**Task.** Three UI tweaks to `triggers.html`: (1) swap the "Enter using" radios so Ages/years is
first; (2) replace the free-text "Snapshot" status banner with a proper result card, labeled
"Mod 75", valued Met/On-Track to Meet/Not Met, matching the other cards' look; (3) rename the
"Birth-year rules" card to "Social Security FRA" and spell out "full retirement age" in its desc.

**Files.** `triggers.html`: swapped the two `<label class="radio-opt">` entries under "Enter
using"; changed `.results` grid from `repeat(3,1fr)` to `repeat(2,1fr)` to fit 4 cards as 2x2;
removed the normal-flow `banner.className/innerHTML` "Snapshot: ..." block, replaced with a
`snapshot` string folded into a new first `mk()` card (Mod 75) driven off `m75Status`; banner now
only used for the two validation-error early returns; renamed the Birth-year `mk()` call's label
to "Social Security FRA" and expanded "FRA" to "full retirement age (FRA)" in its description.

**Risk.** Losing the useful client-context line (age/service/group/separation) when removing the
banner; avoided by folding it into the Mod 75 card's description via the `snapshot` variable
instead of dropping it.

**Validated in preview:** radio order, 2-column grid at desktop, 1-column at mobile (no overflow),
all three Mod 75 values/colors (Met/green, On-Track to Meet/blue, Not Met/red), FRA description
spelled out, console clean, em-dash grep 0.

## 2026-07-20 (3) — Trigger Finder: wire employment status into eligibility logic

**Task.** User reported the cards (Rule of 55) and timeline don't update when the client is marked
Terminated, so benefits the client can no longer qualify for (Mod 75, age-55 subsidy) still showed
as reachable. Employment status was only driving labels, not the engine.

**Fix.** Added `termed` flag and `termRef` (separation date or today) to `render()`. Mod 75 status
for a terminated client is now met/missed only (tested at the termination reference, matching the
guides' "tested at termination" rule), never 'ontrack'. Rewired: Rule-of-55 card (new terminated-
no-date branch), retiree-medical card (missed-with/without-date wording), vesting (lost if termed
before cliff even w/o date), the Mod 75 + age-55 + Rule-of-55 timeline items, the banner, and the
separation checklist steps (milestone, 401(k), conversion window). Years-of-service in Ages mode is
now anchored to the separation date for a terminated client, not today.

**Risk.** The plan rule is that Mod 75 is tested at termination and does NOT improve by aging after
you leave; verified this framing against the guides before freezing service. Kept the counterfactual
"would have arrived" date so advisors still see how far short the client fell.

**Validated in preview:** Active↔Terminated toggle flips the retiree-medical gate, Rule-of-55 card,
and Mod 75 timeline item (neutral→red warn) with the banner in step; terminated-with-date scenarios
(56/26 met; 52/22 missed) resolve correctly; console clean; grep em-dash 0.

## 2026-07-20 (2) — Trigger Finder input redesign: explicit radios + em-dash cleanup

**Task.** User asked to replace the implicit date-vs-number entry model in `triggers.html` with
explicit radio buttons: one for entry mode (specific dates vs. age/years of service), one for
employment status (actively employed vs. terminated), with Employee Group moved to be the first
field alongside employment status. When actively employed, the separation field reads "Planned
Date of Separation"; when terminated, "Date of Separation".

**Files.** `triggers.html`: reordered Section 01 inputs (group → employment status → entry mode →
DOB/hire rows → separation), added `.radiogrp`/`.hidden` CSS, added `empStatus()`/`entryMode()`
getters, `syncModeVisibility()`/`syncSepLabel()` toggles, and rewired `render()` to read dob/hire
strictly from the active entry mode and to use the explicit `isActive` flag (not date-guessing)
for all "(planned)"/"at separation" wording.

**Also.** The design hook flagged em-dash overuse post-edit; caught that the CLAUDE.md financial-copy
standard explicitly bans em-dashes in user-visible copy, which the initial build violated
throughout (68 instances). Rewrote all of them (title, labels, table, footer, and every JS-generated
string) to periods/commas/colons/parentheses, matching the "·" convention used elsewhere in the guide
set. CHANGE_LOG entry covers both changes together.

**Validated in preview:** default state, both radio toggles in each direction, and a full
exact-date/terminated-status render all confirmed correct; grep for em-dash returns 0; console
clean; no mobile overflow.

## 2026-07-20 — Financial Trigger Finder page (triggers.html)

**Task.** New interactive tool page: advisor enters client DOB (or age), date of hire (or years
of service), date of separation (actual or planned), and employee group (Union/Bargained,
Management Legacy Non-Bargained, Mobility), and gets the dated list of financial triggers to
review: catch-up at 50, Rule of 55, 59½ penalty end, super catch-up 60–63, Social Security
62/FRA/70 (FRA by birth year), IRMAA two-year lookback beginning at 63, Medicare IEP and 65,
QCDs at 70½, RMD age 73/75 by birth year, plus plan-specific Mod 75 milestone dates and a
separation-date checklist (retiree-medical eligibility by group, COBRA-to-Medicare gap math,
pension commencement, rollover/Rule-of-55 interplay, 401(k) loan, NUA, Roth-conversion window).

**Files.** New `triggers.html` (same visual system as the three guides). Nav link added to
`index.html`, `non-bargained.html`, `mobility.html` (new "Tools" navlabel). `ANNUAL-TAX-FIGURES.md`
updated so the yearly checklist covers the new page's indexed figures (catch-up amounts, IRMAA
thresholds). TODO/CHANGE_LOG per workflow.

**Sources/rules reused from the guides (already SPD-verified there):** Mod 75 combos any/30,
50/25, 55/20, 65/10; NB early-reduction 0.5%/mo (<30 yrs) vs 0.25%/mo (30+), gone at 55; union
threshold age 55 West/Craft, 56 Southeast, unreduced only at 30+ yrs; Mobility has no pension
Mod 75 but the Medical Program's own Rule-of-75 test gates retiree medical; management retiring
on/after 1/1/2022 gets access only (no subsidy); bargained pre-65 subsidy may still exist;
Medicare-side subsidy ended for last day on/after 1/1/2021; 2026 figures: catch-up $8,000,
super catch-up $11,250, IRMAA $109,000/$218,000 five tiers, 2-yr lookback.

**Risks.** Statutory birth-year rules must be right: FRA 66+2mo/yr for 1955–59, 67 for 1960+;
RMD 73 for born 1951–1959 (note the 1959 drafting-glitch footnote, IRS proposed regs say 73),
75 for 1960+; Rule of 55 keys on separation in/after the calendar YEAR of the 55th birthday.
Tool is educational-estimate only — carry the standard "verify in NetBenefits/SPD" warning.

**Next steps.** Build page → wire nav links → verify in static preview (inputs exercised,
console clean) → push → CHANGE_LOG.

## 2026-07-14 (2) — Remove implication that Mod 75 yields subsidized healthcare (non-bargained Section 08/09)

**Task.** User flagged Section 08 of `non-bargained.html` as implying management employees can
still get *subsidized* retiree healthcare once Mod 75 is met. Verified against
`ATT Benefit changes 12-2020.pdf` (pp. 3–5) and `Medical SPD 2021.pdf` (pp. 51–52): Mod 75 gates
*coverage eligibility* only. Subsidy is gone for anyone retiring now — pre-Medicare subsidy
eliminated for management with last day on payroll on/after 1/1/2022 regardless of hire date;
Medicare-side subsidy eliminated for last day on/after 1/1/2021. Hire-date/legacy rules now only
matter for those who retired by the cutoffs.

**Files.** `non-bargained.html`: Section 08 gold + warn callouts (Part B/D reimbursement line,
"only pre-2001 hires may qualify" line), Mod 75 trap #2 wording, Section 09 calculator intro,
calculator card label ("Retiree healthcare subsidy" → eligibility) and result text.
`case-studies-nb.html` already teaches this correctly — no change.

**Risks.** Don't erase the real value: Mod 75 access to unsubsidized group coverage is still a
material pre-Medicare bridge. Keep the historic cutoffs for context.

**Next steps.** Edit → verify in preview (incl. calculator output) → push → CHANGE_LOG.

## 2026-07-14 — Fix inaccurate "match excludes after-tax" claim (Section 09/11)

**Task.** User flagged the Section 09 claim that "the employer match applies only to pre-tax and
Roth deferrals, not to after-tax (bucket ③) contributions" as possibly inaccurate. Verified against
`ATT-Retirement-Savings-Plan_78-63233.pdf`: the claim is wrong. The SPD (p. 22–24) defines matched
Basic Contributions (first 6% of Compensation) as before-tax, Roth, after-tax, or any combination,
and the default spillover election exists specifically so contributions continue as after-tax and
"continue to receive Company Match" after the 402(g) limit. Only catch-up contributions and amounts
above the 6% matched cap never earn match.

**Files.** `index.html` (Matching Formula callout + front-loading callout), `non-bargained.html`
(front-loading callout). Case-study pages verified clean.

**Risks.** Keep the front-loading warning coherent — it's real only when spillover is opted out of
or contributions are suspended; don't overstate or erase it.

**Next steps.** Edit both files → verify in preview → push → CHANGE_LOG.

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
