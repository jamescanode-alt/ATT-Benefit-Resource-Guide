# PLAN_LOG

## 2026-08-21 (4) — New section: crossing between union and management (bridging)

**Task.** User asked for a section explaining the bridging rules for an employee moving from union to
management or the reverse.

**Research first.** The term "bridging" appears in the SPDs only in the narrow vesting sense ("prior
Years of Vesting Service will be determined under the applicable bridging rules"). The substance the
user is asking about is spread across four differently-named sections in every SPD: *Break in Service
Rules*, *Effect of Rehire Within the AT&T Controlled Group*, *Moving Between Members of the AT&T
Controlled Group*, and the *Promotions / Demotions* subsections. I read all four in the Southeast
(78-74516), Bargained Cash Balance #2 (78-74506), Nonbargained (78-49754), Mobility (78-49752), ARSP
(78-74968), and BSSP (78-74971) SPDs before writing.

**The organizing insight.** *Termination of Employment* is defined as terminating with **all members
of the AT&T Controlled Group**. A union/management move therefore is **not** a termination and **not**
a break in service, so **Term of Employment (seniority/NCS) runs straight through** — which means
**Mod 75 progress is preserved**. Clients routinely believe the opposite. That fact anchors the whole
section; everything else is a list of what does and does not follow it.

**What the SPDs actually say, and the two findings worth the section's existence.**

1. **Pensions stack, they do not merge.** Every program: *"you will be eligible to receive a
   distribution of your available vested Pension Benefit from **both** this Program and any other
   applicable Plan program."* A cash-balance account left behind *"will remain in this Program and
   will continue to earn Interest Credits"* — compounding continues, pay credits stop.

2. **The Nonbargained three-year bridge, and the carve-out that guts it.** Prior bargained service
   joins Pension Calculation Service after 3 years in the program, offset by the prior benefit,
   **"unless the service was earned under a cash balance formula."** Since anyone hired after
   Aug. 8, 2009 is in BCB#2 (cash balance), **their union service bridges nowhere**. Combined with
   the Management Cash Balance Program closing after Dec. 31, 2014, this produces a concrete and
   increasingly common client: a post-2009 union hire promoted today stops accruing a union pension,
   gains no management pension, and bridges no service. That is the single most useful thing in the
   section and it is not stated in any one SPD — it falls out of combining three of them.

**Other sourced detail worth capturing:** the demotion band-freeze (higher band frozen until the new
band catches up; **5th anniversary** protection where the demotion follows permanent medical
restriction or force surplus and Mod 75 was already met); the **18-month** rule for a promotion to
reach the band calculation; the **one-year** test for temporary/acting promotions (employee stays in
the union savings plan); the savings-plan rule that the **account never follows the client** (frozen
old account + new account, loans aggregated across both); the ARSP/BSSP **asymmetry** on inbound
former managers; and the union/management **break-in-service threshold mismatch** (3 vs 5 years to
restore service; 5- vs 2-year layoff window).

**Placement decisions.**
- `index.html`: new **Section 09**, between Payment options and the Savings Plan group, because it
  spans both. Renumbers 09–16 → 10–17.
- `non-bargained.html`: parallel **Section 11** written from the management side (different emphasis:
  leads with the bridge and its carve-out, since that is the management reader's question).
  Renumbers 11–18 → 12–19.
- `mobility.html`: a cross-linking callout rather than a full section. Mobility covers both bargained
  and management populations in one program, so the crossing question is less acute there.
- Both consolidated MDs: the union reference's **§3.8** was a one-line stub on exactly this topic, so
  it is expanded in place rather than appended as a new §3.13 — keeps numbering stable and puts the
  content where a reader already looks. Management MD's *Moving between members* paragraph likewise
  expanded in place.

**Risks.** (1) Renumbering two guides is the main mechanical risk; mitigated by descending-order
replacement and by asserting before/after reference counts rather than eyeballing. (2) The
"promotion may cost you your pension" framing is genuinely important but must not read as advice
against promotions — the enhanced 7% match usually more than offsets it, and the section says so
explicitly in both guides.

**Next steps.** Write → renumber with assertions → insert → verify anchors and sequence in-browser →
responsive check → MDs → push.

## 2026-08-21 (3) — The missing SPD arrives: Bargained Cash Balance Program #2

**Task.** User supplied two PDFs and asked whether either fills the gap flagged this morning.

**Answer: one does, completely.**

- `AT&T_Bargained Cash Balance_2_20250711.pdf` = **Bargained Cash Balance Program #2 SPD,
  NIN 78-74506, July 2025.** This is exactly the document named as missing. It **confirms every
  figure** the guide had been carrying and that I had flagged as unsourced.
- `Southeast_SPD (1).pdf` = **Southeast Program SPD, NIN 78-30077, July 2014.** An older edition,
  superseded by the Jan. 2025 SPD already in the library. Adds nothing authoritative; filed for
  edition history only.

**What the BCB#2 SPD confirms, verbatim.**
- Age Credit Factor ladder **1.77 / 2.27 / 2.78 / 3.28 / 4.04%** at ages <30 / 30-36 / 37-43 /
  44-49 / 50+, measured at the **end of the month** the credit is applied.
- The guide's worked example is the **SPD's own**: age 40, $4,000 Pension Compensation, 2.78%
  → **$111.20**.
- Interest is a monthly rate compounding to a flat **4.5%** annual, applied to the **prior
  month-end balance before** the current credit is added. SPD example: $10,000 × 0.367% =
  **$36.70**, new balance **$10,236.70**. Again the guide's exact numbers.
- Supplemental Pay Credit = **2%** on Pension Compensation above the Social Security Wage Base.

So the guide was **right all along**; the material simply had no supporting document in the folder.
My "unsourced" flag was accurate as a statement about the library and wrong as an implication about
the content. Correcting that is the bulk of this pass.

**What the SPD adds that the guide did not have.**
- **The alternate ladder is real and I now have its scope**: 1.75 / 2.25 / 2.75 / 3.25 / 4.00%,
  applying (a) always, to the Mobility Orange/Purple/Black/Blue contracts and IBEW Local 1547
  (Alascom), and (b) to *earlier service* under a dozen named contracts with changeover dates of
  Jan. 1, 2013, Jan. 1, 2014, or Jan. 1, 2015. A long-tenured client can carry **both** ladders.
  The guide's old parenthetical ("some bargaining units use a slightly different schedule") was
  directionally right but gave no scope.
- **A frozen group**: Mobility Blue (IBEW 1547), all titles except Cell Site Technician and Cell
  Site Tech Foreman, accruals **frozen Jan. 1, 2020**, interest only after.
- **Coverage**: bargained employees hired **after Aug. 8, 2009** across essentially every core
  contract, plus several groups eligible regardless of hire date. This is the program the
  post-2009 population lands in, which is what made the gap material.
- **NRA = 65 or the 3rd anniversary of participation** (lowest service threshold of the seven).
  Vesting 3 years, participation after 1 year, 5 years to file suit, $7,000 mandatory cash-out.
- **Lump sum is contract-gated**: available to 14 named contracts, not to all.
- Pension Compensation includes **target incentive payments for leveraged job titles** in the major
  core contracts.

**Approach.** Reverse this morning's caution rather than merely soften it, and upgrade the content
in the process: the guide can now state the mechanic *and* its scope, which it never could before.
Keep the three-way program distinction (BCB#2 age-graded / Southeast band-driven / Mobility flat
5%), because that was a genuine finding and remains correct and useful.

**Decisions.**
- Replace the "sourcing caution" callout with a **three-engine comparison table** keyed on the
  Aug 8, 2009 hire-date line, which is the actual decision the advisor has to make.
- Restore the Marcus Bell example to a real calculation, now correctly placed in BCB#2, and add the
  IBEW-specific check that his early service may fall under the 1.75% ladder (changeover
  Jan. 1, 2014 for IBEW contracts).
- Keep the rebuilt Southeast Sam case study as-is. It is correct, sourced, and teaches the
  band-driven mechanics that genuinely differ. No reason to revert it.
- Add **§4.7** to the union consolidated MD as a full program subsection, and leave BCB#2 **out of
  the Part 2 matrix** deliberately, since it has no Pension Band component and no Mod 75 subsidy so
  most rows would read n/a. A pointer note explains the omission.

**Risks.** (1) Re-reversing published copy twice in one day is confusing if the reasoning is not
recorded; hence the detail here and in CHANGE_LOG. (2) The alternate-ladder scope is intricate
(two populations, three changeover dates) and is the most likely thing to be misread, so it gets its
own callout rather than a footnote.

**Next steps.** Restore §04 → add §4.7 to the union MD → refresh source tables → re-verify → push.

## 2026-08-21 (2) — Case-study consistency pass, and an unsourced schedule found

**Task.** Check the three case-study decks against the same-day SPD updates.

**What the check turned up.** The decks were inconsistent, but the root cause was not in the decks.
The union guide has been teaching a cash-balance engine that **cannot be sourced to any SPD in the
project library**: an age-graded *Age Credit Factor* schedule (1.77% / 2.27% / 2.78% / 3.28% /
4.04%), a flat **4.5%** annual interest assumption (0.367%/month), and a **2% Supplemental Pay
Credit** on pay above the Social Security Wage Base.

Verification method: extracted all 20+ PDFs in `Bargained SPDs/` and `Management SPDs/` with
`pdftotext -layout` and grepped the full corpus. **"Age Credit Factor" occurs zero times.** Every
hit on `4.04` / `1.77` is a coincidental substring inside a pension *band dollar table*
(`54.04`, `21.77`, `51.77`). What the library actually documents:

| Program | Basic Benefit Credit | Interest Credit |
|---|---|---|
| Southeast | **60 × Pension Band Amount**, annual | prior-Nov 30-yr Treasury, annual, on the Jan 1 balance |
| Mobility | **flat 5% of Pension Compensation**, monthly | monthly rate compounding to the 30-yr Treasury from the second month of the prior quarter |
| East | Service Category table by compensation | prior-Nov 30-yr Treasury, min **4.00%** |
| Legacy Bargained | Pension Band Credits, annual | prior-Nov 30-yr Treasury, min **3.75%** |
| Nonbargained | **frozen** since Jan 14, 2005 | 30-yr Treasury, middle month of prior quarter |

**Most likely origin.** The guide's own source list cites a *Bargained Cash Balance Program #2 SPD*
that **is not present in the library** (`find -iname '*.pdf' | grep -i cash.balance` → nothing).
That program is real and is where post-Aug-2009 bargained hires land, so the schedule may well be
correct *for it*. The defect is that it was presented as the general union design and applied to
programs that demonstrably use something else.

**I propagated part of this earlier today.** In the morning's §04 rewrite I attributed the
age-graded design to "the Mobility Bargained and other cash-balance programs." Mobility Bargained is
a **Pension Band** program, and the Mobility Program uses a **flat 5%**. That attribution was wrong
and is corrected in this pass.

**Approach.** Do not delete the age-graded material (it may be right for the missing program, and
the mechanic is worth teaching). Instead: demote it to a clearly labelled illustration, add a
sourcing caution with the table above, and rebuild anything that presented it as a client's actual
benefit.

**Decisions.**
- `case-studies.html` Sam: rebuilt on **sourced Southeast** mechanics rather than deleted. Hired
  2004 → Southeast-eligible with no pre-99 service → genuinely cash-balance-only, so the case works
  unchanged in premise. New checkpoints teach the real counterintuitive points: the credit is
  band-driven so a raise/overtime moves nothing, interest is figured on the **Jan 1 balance before**
  the year's credit is added, and interest keeps accruing after termination.
- `case-studies.html` Gloria: named as Southeast, band amount refreshed $51.81 → **$57.23** (the
  2025 SPD's own worked-example figure), and the dangling cross-reference to the Supplemental Pay
  Credit replaced with the sum-not-greater-of point. Her Age Incentive Factor of **1.06 is correct**
  as written (age 65 → the 62-or-older tier), so it stays.
- `case-studies-mobility.html`: the deck's own Mobility content is **accurate and well sourced**
  (flat 5%, 0.327%, correct Pension Compensation definition). But four distractor rationales
  asserted the age-graded schedule and the wage-base credit were "the union cash balance," teaching
  a false fact about the union plan as the *reason a wrong answer is wrong*. Reworded to describe
  the mechanics generically without attributing them to the union plan.
- `case-studies-nb.html`: checked, **no changes needed**. Its greatest-of-three framing, the
  Jan 14 2005 cash-balance freeze, and the CAM-still-accruing contrast are all correct.

**Risks.** (1) Softening the age-graded content could read as making the guide less useful; the
mitigation is that the mechanic is retained and the *replacement* Southeast content is stronger
because it is sourced. (2) The real gap is now visible and unfixable from inside the repo: the
Bargained Cash Balance Program SPD has to be obtained, and until it is, clients hired after
Aug 9, 2009 have no verified pension mechanics anywhere in this library.

**Next steps.** Scope §04 and the glossary → rebuild Sam → fix Gloria → fix the Mobility distractors
→ re-verify the decks actually execute (they are JS data, so tag-balance alone is insufficient) →
push.

## 2026-08-21 — Three new authoritative SPDs: ARSP (Jul 2026), BSSP (Jul 2026), Southeast pension (Jan 2025)

**Task.** Fold three newly-added SPDs into the guide set and both consolidated Markdown references.
The PDFs supersede everything currently cited for their subject matter:

| Source | NIN | Effective | Supersedes |
|---|---|---|---|
| `Management SPDs/20260710---SPD---ATT-Retirement-Savings-Plan` (also filed under `Bargained SPDs/`, byte-identical) | 78-74968 | July 2026 | `ATT-Retirement-Savings-Plan_78-63233.pdf` (2022) |
| `Bargained SPDs/20260710---SPD---BellSouth-Savings-and-Security-Plan` | 78-74971 | July 2026 | nothing — new plan, absent from the guide |
| `Bargained SPDs/20250711---SPD---Southeast-Program-...-ATT-Pension-Benefit-Plan` | 78-74516 | Jan 1, 2025 | `202011---SPD---Southeast-Program-of-the-ATTWarnerMedia...-78-49755.pdf` (2020) |

**What actually changed (verified against the PDFs, not assumed).**

*ARSP (78-74968).*
- Roth catch-up for high earners is now live and unconditional: age 50+ with **>$150,000 of 2025 FICA
  wages** must make catch-up **Roth only**. This retires the guide's "bargained plans have until 2029"
  hedge — ARSP has adopted it. Closes a TODO.
- Match-eligibility timing moved for one group: **Mobility Blue (IBEW 1547) is immediately eligible
  as of Jan. 1, 2024**; the guide still shows "after 1 Year of Service."
- Mandatory cash-out **$1,000 → $7,000** (>$1,000–$7,000 auto-rolls to an IRA rather than paying out).
- New **Domestic Abuse Withdrawal**: lesser of $10,500 or 50% of vested account.
- 2026 figures confirmed: 402(g) $24,500 · 415(c) $72,000 · catch-up $8,000 / $11,250 · HCE $160,000 ·
  **IRS annual compensation limit $360,000, and contributions auto-suspend on reaching it.**
- Trustee is now **The Bank of New York Mellon**. Plan number 009, EIN 43-1301883.
- **ASSP balances consolidated into ARSP** Jan. 1, 2026 for Southwest CWA hired/rehired before
  Aug. 9, 2009. Partially closes the "which savings plan is my bargained client in?" TODO.
- Match tiers themselves are **unchanged** from the 2022 edition — the table in `index.html` §10
  verified row by row and holds.

*BSSP (78-74971) — the significant gap.* Legacy BellSouth / Southeast CWA District 3 bargained
employees hired or rehired **before Aug. 9, 2009** are in the **BellSouth Savings and Security Plan,
not the ARSP**, and the two plans are explicitly mutually exclusive. Since `index.html` is a
Southeast-shaped union guide, its entire savings section has been describing the wrong plan for a
large share of its own audience. BSSP differs on nearly every axis that matters:
**no Roth at all** (so a high earner's catch-up limit is **$0** — they are locked out of catch-up
entirely), **no BrokerageLink**, no after-tax→Roth conversion (no mega-backdoor), contributions in
**whole dollars per week capped by a pay-band table** ($15–$67/wk) rather than a percent of pay,
match of **71% of Basic Contributions effective Apr. 1, 2026** (reset annually on corporate
performance; 25% flat for Utility Operations), two general-purpose loans and no residence loan,
one General Withdrawal per 6 months, LifePath (not AT&T Age-Based) as the QDIA, 120 days to sue.

*Southeast pension (78-74516).*
- Plan renamed **AT&T Pension Benefit Plan** eff. Jan. 1, 2021; sponsor is AT&T Inc.; plan number **017**.
- **Age Incentive Factor** documented: 1.01 at 57 → 1.06 at 62+; **1.06 regardless of age if Mod 75 is
  not satisfied**, 1.0 if Mod 75 is satisfied at 56 or younger. Not currently in either guide or MD.
- **Basic Benefit Credit = 60 × Pension Band Amount** (highest band held that year).
- The benefit is a **sum, not a greater-of**: Pre-99 Pension Band Benefit (service frozen at
  Dec. 31, 1998 × Age Incentive Factor) **plus** the Cash Balance Account from 1999 forward.
- **$75,000 Partial Lump Sum** with residual annuity, Mod-75 satisfiers only, not Special Represented.
- Pension mandatory cash-out **$5,000 → $7,000**; **$25,000 retiree death benefit cap** for retirees
  who terminated on/after Jan. 1, 1992; rehire within 5 years on/after Aug. 9, 2015 is not a break.
- Program table gives the **Management Cash Balance Program** description and, importantly, that it
  **closed to hires/rehires after Dec. 31, 2014** — so management hired 2015+ has no pension at all,
  which is exactly why that group gets the 133⅓%/100% match. Closes a TODO.

**Files.** `index.html` (§09/§10/§11 + pension sections), `non-bargained.html`, `mobility.html`,
`triggers.html`, `Management SPDs/_CONSOLIDATED-Management-Pension-SPDs.md`,
`AT&T Union-Bargained Pension - Consolidated SPD & SMM Reference.md`, `TODO.md`, `CHANGE_LOG.md`.

**Risks.** (1) The BSSP finding reframes part of the union guide rather than just adding to it; the
fix has to be a plan-selection gate the advisor hits *before* the savings content, not a footnote.
(2) The $360,000 compensation limit interacts with the §11 calculator's stated assumption that the
comp limit is not applied — the disclaimer has to change, and it makes the open ">$1M target-rate"
TODO cosmetic rather than latent. (3) Compliance-sensitive copy: the Roth-catch-up hedge must be
removed rather than softened, since leaving it in would understate a rule now in force.
(4) Two internal inconsistencies in the ARSP itself (Purple Contract shown as District 3 in one
special rule vs. District 6 in the summary; District 5 present in the eligibility list but absent
from the immediate-match list) — carry them as noted discrepancies, do not silently pick a side.

**Next steps.** Plan-selection gate + BSSP block in `index.html` → ARSP corrections across all three
guides → Southeast pension detail → both consolidated MDs → responsive/preview check → push.

## 2026-08-12 (4) — Calculator becomes Section 11; adds DOB, 402(g)/415(c) status, and target rates

**Task.** (1) Move the calculator out of the match section into its own section, immediately after
it. (2) Add date of birth. (3) Report whether the client is maxing the 402(g) and 415(c) limits.
(4) Compute the deferral rate that would max each limit, given the employer contribution.

**Renumbering.** New `#match-calc` section at 11, so irmaa 11→12, strategy 12→13, protections
13→14, glossary 14→15, contacts 15→16. Reusing the existing `#match-calc` id (currently on the
calculator's `<h3>`) as the section id keeps any saved links working; the `<h3>` loses its id so
there is no duplicate.

**What DOB buys.** Catch-up eligibility is age at the *end of the calendar year*, per the SPD
("You must be age 50 by the end of the calendar year"). So ageAtYearEnd = PLAN_YEAR − birthYear:
under 50 → none; 50–59 → $8,000; 60–63 → $11,250; 64+ → back to $8,000. Catch-up is a separate
election, is never matched, and is exempt from 415(c), so it must be reported as its own number,
not folded into the contribution-rate math.

**The limit math.**
- employeeTotal = comp × rate/100, plan-capped at 50% of Compensation (Basic Contribution limit).
- 402(g) counts the first $24,500 of that; with spillover on, the remainder continues as after-tax.
- 415(c) total additions = employeeTotal + match. Catch-up is excluded.
- Rate to max 402(g) = 24,500 / comp × 100.
- Rate to fill 415(c) = (72,000 − match) / comp × 100. Match is fixed at its cap for any rate at or
  above 6%, so it is not circular at any realistic Compensation. Both rates clamp to the plan's 50%
  ceiling, and when 415(c) needs more than 50% the tool must say it is unreachable rather than
  print an impossible rate.
- The rate slider must extend from 0–20 to 0–50 or the suggested rates are unreachable in the UI.

**2026 figures used** (all four already catalogued in `ANNUAL-TAX-FIGURES.md`): 402(g) $24,500;
415(c) $72,000; catch-up $8,000; super catch-up $11,250. These are now *hard-coded in JavaScript*
as well as in prose, which is a new maintenance surface, so `ANNUAL-TAX-FIGURES.md` has to be
updated to point at the JS constants block.

**Risks.** Suggesting a rate that fills 415(c) implies a very high deferral percentage, which
collides with the per-pay-period match trap: front-loading to that rate without the spillover
election on can stop contributions early and forfeit match. The output has to carry that warning
next to the number, not leave it two sections away. Also: this is arithmetic against published IRS
limits, not a contribution recommendation, and the copy should read that way.

**Next steps.** Script the section split with assertions → rebuild the calculator inputs and
outputs → verify limit math at several ages and compensations, including the unreachable-415(c)
case → responsive check → push.

## 2026-08-12 (3) — Promote the match to its own section; currency-format the Compensation input

**Task.** Two requests. (1) Move the employer-match material out of §09 into its own numbered,
nav-linked section so it is easier to find. (2) Format the calculator's "Annual eligible
Compensation" field as currency.

**Approach for the split.** New `#match` section between `#savings` and `#irmaa`, so this is the
first change in the project that actually renumbers sections. Everything downstream shifts by one:
irmaa 10→11, strategy 11→12, protections 12→13, glossary 13→14, contacts 14→15. Nav gains a
"10 The company match" item under the existing "The Savings Plan" label.

Content moved into the new section: the Employer Contributions intro and Matching Formula callout,
the formulas-by-contract table, the match-eligibility and AT&T-Shares callouts, the per-pay-period
match trap, and the whole calculator with its disclaimer. Two `<h4>` headings promote to `<h3>`
now that they sit at section top level. The "Employer Contributions" `<h3>` is dropped, the section
`<h2>` replaces it.

**Things the split breaks that must be fixed with it:**
- Cross-references in body copy: "$4,560/year, Section 09" → Section 10; "IRMAA line (Section 10)"
  → Section 11; the JS section comment; and "(Section 09 above)" inside the moved eligibility
  callout, which becomes a real link back to `#savings`.
- `#savings` loses its client example when Rosa's match example moves. Project convention is one
  Client Example per teaching section, so `#savings` needs a new one covering what it still owns
  (415(c) headroom, Rule of 55, loan-before-rollover), and the match example loses its trailing
  pre-tax/Roth clause so the two do not overlap.
- Ordering: the per-pay-period trap has to land *before* the calculator, not after it, so the
  calculator and its disclaimer close the section.

**Approach for the currency input.** `type="number"` cannot display "$95,000", so the field becomes
`type="text"` with `inputmode="numeric"`. A `formatComp()` reformats on every input event and
restores the caret by counting digits before it (so mid-string edits do not jump to the end), and a
single `readComp()` is the only place the numeric value is parsed back out. Guard added for an
empty/zero Compensation, which previously produced a misleading "capturing the full match" banner
showing $0.

**Files.** `index.html` only.

**Risks.** Renumbering is the failure mode here: a missed `pn` div, nav number, or body
cross-reference leaves the guide internally inconsistent. Every renumber and cross-reference edit
is asserted in the migration script rather than done by hand. `case-studies.html` links to guide
sections 04–08 only, all upstream of the insertion point, so it is unaffected.

**Next steps.** Script the move with assertions → verify numbering, nav, and anchors → test the
currency field (typing, paste, letters, leading zeros, empty, caret) → responsive check → push.

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
