# CHANGE_LOG

## 2026-08-21 (4) — New section: crossing between union and management (bridging rules)

**Summary.** Added a section on what happens when an employee moves between a bargained job and
management, to both primary guides plus a cross-reference in the third, and expanded the
corresponding subsection in both consolidated Markdown references. The material is sourced from the
*Break in Service Rules*, *Effect of Rehire*, *Moving Between Members of the AT&T Controlled Group*,
and *Promotions / Demotions* sections of six SPDs.

### The framing fact

**Termination of Employment** means terminating with **all members of the AT&T Controlled Group**. A
union/management transfer keeps the client inside that group, so it is **neither a termination nor a
break in service**, and **Term of Employment (seniority / NCS) runs uninterrupted**. Because Mod 75
and the retiree-healthcare eligibility riding on it are measured against Term of Employment,
**crossing the line does not reset Mod 75 progress.** Clients frequently believe it does.

### The finding that justifies the section

Three SPD provisions combine into a conclusion none of them states alone:

1. Moving into the **Nonbargained Program** bridges prior bargained service into Pension Calculation
   Service after **3 years**, offset by the prior benefit — **"unless the service was earned under a
   cash balance formula."**
2. Anyone hired into a bargained job **after Aug. 8, 2009** is in **Bargained Cash Balance Program
   #2**, which is a cash-balance formula. So their union service **bridges nowhere**.
3. The **Management Cash Balance Program closed** to entrants after **Dec. 31, 2014**.

Therefore: **a union employee hired after 2009 and promoted today stops accruing a union pension,
gains no management pension, and bridges no service.** Their BCB#2 account keeps earning 4.5% and
their defined-benefit accrual ends. Both guides state this plainly and immediately balance it — the
enhanced **133⅓% / 100%** match (up to **7% of pay**, available immediately, reaching anyone
*"hired, rehired, or **transferred** on or after Jan. 1, 2015"*) usually more than compensates, and
the raise typically dwarfs both. The point is to quantify the trade at the decision, not to argue
against promotions.

### What each guide gained

**`index.html` — new Section 09, "Crossing between union and management"** (between Payment options
and the Savings Plan group; sections 09–16 renumbered to 10–17). Covers: the transfer-is-not-a-
termination rule; a what-travels table; pensions stacking rather than merging; the three-year bridge
and its cash-balance carve-out; a hire-date table showing where a promoted union employee actually
lands; demotion mechanics including the **band freeze** and the **5th-anniversary** protection for
demotions following permanent medical restriction or force surplus; the **one-year** temporary-
promotion test and the **18-month** rule for a promotion to reach the band calculation; the savings
plans' rule that the **account never follows the client**; the **ARSP/BSSP asymmetry** on inbound
former managers; **loan aggregation** across plans; a union-vs-management break-in-service comparison;
and the **lump-sum repayment trap** that silently restarts a Mod 75 clock.

**`non-bargained.html` — new Section 11, "Crossing between management and union"** (sections 11–18
renumbered to 12–19). Same substance written from the management side, leading with the bridge and
its carve-out since that is the management reader's actual question, and noting the eligibility
mechanic that makes the bridge reachable at all: Nonbargained requires employment on Dec. 31, 2006,
**not** management status on that date, which is why its SPD carries a special rule for *"Employees
Who Have Been Promoted From Bargained Positions."*

**`mobility.html`** — a cross-linking callout rather than a full section, since the Mobility Program
covers both bargained and legacy management populations within one program.

### Consolidated Markdown

- **Union reference §3.8** was a one-line stub on exactly this topic; expanded in place into eight
  subsections rather than appended as a new §3.13, which keeps numbering stable and puts the content
  where a reader already looks. Includes the effect-of-rehire rules (opening balance resets to $0
  after a prior lump sum or annuity; annuity **permanently suspended** on rehire except for a
  post-NRA rehire working under 40 hours/month).
- **Management reference** — the *Moving between members* paragraph expanded in place with the
  carve-out, the landing table, the demotion freeze, the savings-plan and loan-aggregation rules, and
  the break-in-service threshold mismatch.

### Bug found and fixed while verifying

`non-bargained.html` **never defined the `.tscroll` CSS rule** — only `index.html` has it. The new
section's two tables were therefore rendering with `overflow-x: visible` and pushing the page into
horizontal scroll at 375px. Added the canonical rule
(`.tscroll{overflow-x:auto;margin:20px 0}` / `.tscroll table{margin:0;min-width:540px}`) to that
page. Caught only because the responsive check tests the actual computed style rather than trusting
the markup; a tag-balance or anchor check would have passed it.

### Files changed

`index.html` · `non-bargained.html` · `mobility.html` ·
`AT&T Union-Bargained Pension - Consolidated SPD & SMM Reference.md` ·
`Management SPDs/_CONSOLIDATED-Management-Pension-SPDs.md` · `PLAN_LOG.md` · `CHANGE_LOG.md`

### Validation

- HTML tag-balance across all **7** pages — pass.
- Section numbering verified **sequential 01–N** on every page after renumbering (index 17 sections,
  non-bargained 19), with before/after cross-reference counts asserted programmatically rather than
  inspected: refs 1–8 (index) and 1–10 (non-bargained) unchanged, refs above the insertion point
  shifted by exactly one, the single delta being an intentional new cross-reference.
- Internal anchors on all 7 pages — **0 broken**. Markdown internal links — **0 broken**.
- Cross-page links from `mobility.html` to `#bridging` on both guides confirmed to resolve.
- Responsive at 375px via per-page iframe measurement: **no horizontal overflow on any guide**; all
  new tables confirmed scrolling inside `.tscroll` with computed `overflow-x: auto`.
- **0 em-dashes** in the new user-visible copy (two were caught and removed).
- **0 console errors.**

### Status

Complete across all three guides and both consolidated references.

## 2026-08-21 (3) — Bargained Cash Balance Program #2 SPD acquired; the flagged gap is closed

**Summary.** The document flagged this morning as missing has been supplied. It **confirms every
figure** the guide had been carrying and that the previous commit had flagged as unsourced, so this
pass reverses that caution and upgrades the content with scope detail the guide never had.

### What the two supplied PDFs are

| File | Identity | Verdict |
|---|---|---|
| `AT&T_Bargained Cash Balance_2_20250711.pdf` | **Bargained Cash Balance Program #2 SPD, NIN 78-74506, July 2025** | **Fills the gap completely.** Added to the library. |
| `Southeast_SPD (1).pdf` | **Southeast Program SPD, NIN 78-30077, July 2014** | Superseded by the Jan 2025 SPD already in the library. Filed for edition history, marked SUPERSEDED. |

### The guide was right; the library was incomplete

The BCB#2 SPD confirms, verbatim, every figure the previous commit had demoted to "illustration":

- Age Credit Factor **1.77 / 2.27 / 2.78 / 3.28 / 4.04%** at ages <30 / 30–36 / 37–43 / 44–49 / 50+.
- The guide's worked example **is the SPD's own**: age 40, $4,000 Pension Compensation, 2.78%
  → **$111.20**.
- Interest: a monthly rate compounding to a flat **4.5%** annual, applied to the **prior month-end
  balance before** the current credit is added. SPD example $10,000 × 0.367% = **$36.70**,
  new balance **$10,236.70** — again the guide's exact numbers.
- Supplemental Pay Credit **2%** on Pension Compensation above the Social Security Wage Base, with
  the SPD's example ($173,600 YTD vs a $168,600 wage base → **$100**).

The previous commit's caution was accurate about the *library* and wrong in what it implied about
the *content*. It has been removed rather than softened.

### What the SPD adds that the guide never had

- **The alternate ladder now has scope.** 1.75 / 2.25 / 2.75 / 3.25 / 4.00% applies to two distinct
  populations: **always** to Mobility Orange/Purple/Black/Blue and IBEW Local 1547 (Alascom); and to
  **earlier service** under a dozen named contracts with changeover dates of **Jan 1, 2013**
  (AT&T Corp. Core, Midwest Core, COS, Southeast D3, West D9, IBEW 1269), **Jan 1, 2014** (Southwest
  D6, IBEW Locals 21/58/134, IBEW SC T-3 Midwest and Corp. National, West Appendix D), and
  **Jan 1, 2015** (National Internet Tiers 1 and 2). A long-tenured client can carry **both**
  ladders across their history. The guide previously had this as an unscoped parenthetical.
- **A frozen group:** Mobility Blue (IBEW 1547), all titles except Cell Site Technician and Cell Site
  Tech Foreman, **accruals frozen Jan 1, 2020**, interest only thereafter.
- **Coverage:** bargained employees hired **after Aug 8, 2009** across essentially every core
  contract, plus groups eligible regardless of hire date (National Internet Tier 1, IBEW SC T-3
  Midwest Sales Consultants, BellSouth Utility Operations CWA D3, named appendices).
- **NRA = 65 or the 3rd anniversary of participation**, the lowest service threshold of the seven
  programs. Vesting 3 years; participation after 1 year; **5 years** to file suit; $7,000 cash-out.
- **Lump sum is contract-gated** to 14 named contracts, not universal.
- Pension Compensation includes **target incentive payments for leveraged job titles** in the major
  core contracts.

### index.html

- The sourcing caution is replaced by a **three-engine comparison table** (BCB#2 age-graded /
  Southeast band-driven / Mobility flat 5%, plus East, Legacy Bargained, Nonbargained), keyed on the
  **Aug 8, 2009** hire-date line, which is the decision the advisor actually has to make.
- The age-graded subsection is restored as sourced BCB#2 content, with the full Pension Compensation
  definition and the leveraged-job-title rule.
- New callouts for the **alternate ladder and its two-population scope** and for the **frozen Blue
  Contract group**.
- Interest section now states BCB#2's **fixed 4.5%** (noting it is the only cash-balance program
  without a Treasury-linked rate, so the most predictable to project) alongside Mobility's
  quarterly-reset rate.
- The **Marcus Bell** example is restored to a real calculation, correctly placed in BCB#2, with the
  step-up arithmetic ($111.20 → $161.60) and an IBEW-specific check that his pre-2014 service may
  fall under the 1.75% ladder.
- The "Don't confuse these two" callout is re-framed: the Supplemental Pay Credit and the
  Supplemental Monthly Pension Benefit belong to **different programs** and cannot appear on the same
  statement. The hire date is the tell.
- Glossary entries for `Age Credit Factor`, `Basic Benefit Credit`, and `Cash Balance Account`
  restored with per-program bases and both ladders.
- Source table gains BCB#2 (NIN 78-74506); the superseded list gains the 2014 Southeast SPD.

### Union consolidated Markdown

- New **§4.7 Bargained Cash Balance Program #2**: full coverage map (including the contract-specific
  eligibility dates for Mobility Purple/Orange/Black/Blue, National Internet Tier 2, Alascom,
  Southeast Wire Technicians, and former DIRECTV groups), core terms, all three credit types with
  both ladders, the freeze, forms of payment with the 14-contract lump-sum gate, and plan identifiers.
- Scope line, organization table, and edition warning updated from "six programs" to the six legacy
  programs **plus** BCB#2.
- **Deliberately left out of the Part 2 matrix**, with a note explaining why: BCB#2 has no Pension
  Band component and no Modified Rule of 75 subsidy, so most rows would read "n/a." A one-line
  summary and a link to §4.7 sit under the table instead.
- Appendix updated with both new documents and the BCB#2 SMM chain (NIN 78-58130, NIN 78-63767).

### Unchanged, deliberately

The rebuilt **Southeast Sam case study** stays as written. It is correct, sourced, and teaches the
band-driven mechanics that genuinely differ from BCB#2. The three-way engine distinction found
yesterday was a real finding and survives intact — only the "unsourced" framing was wrong.

### Files changed

`index.html` · `AT&T Union-Bargained Pension - Consolidated SPD & SMM Reference.md` · `PLAN_LOG.md` ·
`TODO.md` · `CHANGE_LOG.md`, plus two PDFs added to `Bargained SPDs/`.

### Validation

- HTML tag-balance across all **7** pages — pass.
- Internal anchors on all 7 pages — **0 broken**. Markdown internal links — **0 broken**
  (46 headings).
- Confirmed no "unsourced / source unverified / not in this library" language survives anywhere.
- Confirmed the restored §04 renders: three-engine table, both ladders, the frozen-group callout,
  and the BCB#2-labelled worked examples all present in the DOM.
- Mobile (375px): **no horizontal page overflow**; the new three-engine table sits in a `.tscroll`
  container.
- **0 console errors.**

### Status

Complete, and the **highest-priority open item from this morning is closed**. Every bargained
population now has verified pension mechanics in the library: pre-Aug-2009 hires through the six
legacy program SPDs, post-Aug-2009 hires through BCB#2. The remaining documented gap is the
**Management Cash Balance Program** SPD on the management side.

## 2026-08-21 (2) — Case-study consistency pass; unsourced cash-balance schedule scoped

**Summary.** Checked the three case-study decks against the morning's SPD updates. The decks were
inconsistent, but the cause sat upstream: the union guide has been teaching a cash-balance engine
that **cannot be sourced to any SPD in the project library**. Scoped it honestly, rebuilt the one
case study built entirely on it, and corrected the distractor rationales that were teaching it as
fact in a second deck.

### The finding

Full-text extraction of every PDF in `Bargained SPDs/` and `Management SPDs/` (`pdftotext -layout`,
then grep across the corpus) shows the phrase **"Age Credit Factor" occurs zero times**. Every hit
on `4.04` or `1.77` is a coincidental substring inside a pension **band dollar table** (`54.04`,
`21.77`, `51.77`), not a percentage. The same applies to the flat **4.5%** interest assumption and
the **2% Supplemental Pay Credit** on pay above the Social Security Wage Base.

What the library does document:

| Program | Basic Benefit Credit | Interest Credit |
|---|---|---|
| Southeast | 60 × Pension Band Amount, annual | prior-Nov 30-yr Treasury, annual, on the Jan 1 balance |
| Mobility | flat 5% of Pension Compensation, monthly | monthly rate compounding to the 30-yr Treasury from the second month of the prior quarter |
| East | Service Category table by compensation | prior-Nov 30-yr Treasury, min 4.00% |
| Legacy Bargained | Pension Band Credits, annual | prior-Nov 30-yr Treasury, min 3.75% |
| Nonbargained | frozen since Jan 14, 2005 | 30-yr Treasury, middle month of prior quarter |

The likely origin is the **Bargained Cash Balance Program**, whose SPD the guide's source list cites
but which **is not in the library**. That program covers bargained employees hired after
Aug 9, 2009, so the schedule may be correct for it. The defect was presenting it as the general
union design and applying it to programs that use something else.

**Self-correction:** this morning's §04 rewrite attributed the age-graded design to "the Mobility
Bargained and other cash-balance programs." Mobility Bargained is a Pension Band program and the
Mobility Program uses a flat 5%. That attribution was wrong and is fixed here.

### index.html

- New **sourcing caution** in §04 with the per-program table above, naming the missing SPD as the
  probable origin and stating plainly: do not quote these percentages, do not apply them to any
  program in the table.
- The age-graded subsection is retained but relabelled **"Illustration only"**; the Supplemental Pay
  Credit subsection relabelled **"source unverified"**.
- The pay-driven half of the two-designs callout now describes the **real Mobility design** (flat
  5%, quarterly-reset Treasury rate, SPD example of $32.70 on $10,000 at 4%).
- The §04 advisor's lens no longer asserts that cash balance "grows faster in later career years" as
  a general truth. It now distinguishes: true twice over in an age-graded design, true **only
  through compounding** under Southeast (the credit does not rise with age), and likewise under
  Mobility's flat 5%. Using the age-graded argument on those clients overstates the cost of leaving.
- The Marcus Bell example is re-scoped: hired 2012, so he is in the **Bargained Cash Balance
  Program** whose SPD is missing. Arithmetic kept but explicitly marked illustrative, with getting
  that SPD named as the action item.
- Glossary: `Age Credit Factor` flagged as not documented in the library; `Basic Benefit Credit` and
  `Cash Balance Account` rewritten to give the program-specific bases.

### case-studies.html (union deck)

- **Sam** rebuilt on sourced Southeast mechanics. His premise was already consistent (hired 2004 →
  Southeast-eligible, no pre-99 service → cash-balance only), so only the engine changed. New
  checkpoints: 60 × $57.23 = **$3,433.80** credited Dec 31; interest **$3,600** on the **Jan 1
  balance of $80,000** (with $3,754.52 called out as the classic error of applying the rate after
  the credit); a raise and heavy overtime move the credit **not at all**, only a higher band does;
  and credits stop at termination while **interest keeps accruing**. Distractors now name the
  Mobility flat-5% and age-graded designs as the wrong answers rather than teaching them as true.
- **Gloria** named as Southeast; band amount refreshed $51.81 → **$57.23** (the 2025 SPD's own
  worked-example figure), so her Basic Monthly Pension Benefit moves $933.62 → **$1,031.28** and the
  Pre-99 total to **$1,041.48**; added the reminder that band amounts are renegotiated and vary by
  termination year. Her Age Incentive Factor of 1.06 was verified **correct** as written (age 65
  falls in the 62-or-older tier) and left alone. The dangling Supplemental Pay Credit cross-reference
  is replaced with the sum-not-greater-of point.

### case-studies-mobility.html

The deck's Mobility content is accurate and well sourced and was left intact. Four **distractor
rationales** asserted the age-graded schedule and the wage-base credit were "the union cash balance"
— teaching a false fact about the union plan as the reason a wrong answer is wrong. Reworded to
describe those mechanics generically without attributing them to the union plan.

### case-studies-nb.html

Checked; **no changes needed**. Greatest-of-three, the Jan 14 2005 cash-balance freeze, and the
CAM-still-accruing contrast are all correct and unaffected by the new SPDs.

### Files changed

`index.html` · `case-studies.html` · `case-studies-mobility.html` · `PLAN_LOG.md` · `TODO.md` ·
`CHANGE_LOG.md`

### Validation

- HTML tag-balance across all **7** pages — pass.
- Internal anchors on all 7 pages — **0 broken**.
- The decks are **JavaScript data**, so tag-balance is not sufficient; executed them in the browser:
  `CASES.length` = 6, question total **30** (matches the deck's own "30 checkpoints" header), every
  question carries a guide `ref`, every multiple-choice has exactly one `correct` option.
- Drove the rebuilt Sam case through the real UI: correct multiple-choice registers and renders its
  explanation plus the guide link; advanced to checkpoint 2; numeric entry of `3433.80` validates
  and shows the right explanation.
- Verified the new arithmetic: 60 × 57.23 = 3,433.80 · 80,000 × 4.5% = 3,600 ·
  57.23 × 17 × 1.06 = 1,031.28 · (600 × 0.001) × 17 = 10.20 · 1,031.28 + 10.20 = 1,041.48.
- Mobile (375px) and desktop: no horizontal page overflow; the new caution table sits in a
  `.tscroll` container with `overflow-x: auto`.
- **0 console errors** on the union guide and the case-study deck.

### Status

Complete. The remaining gap is external to the repo and now explicit in the guide, the TODO, and
here: **the Bargained Cash Balance Program SPD is not in the library**, so bargained employees hired
after Aug 9, 2009 have no verified pension mechanics in this project. Obtaining it is the highest-
value next acquisition.

## 2026-08-21 — Three new authoritative SPDs folded in (ARSP Jul 2026, BSSP Jul 2026, Southeast pension Jan 2025)

**Summary.** Three newly-supplied SPDs were treated as authoritative and reconciled against the whole
guide set and both consolidated Markdown references. The largest finding was not a changed figure but
a **missing plan**: legacy Southeast bargained employees are in the **BellSouth Savings and Security
Plan**, not the ARSP, and the union guide's savings sections had been describing the wrong plan for a
substantial share of their own audience.

### Sources treated as authoritative

| Document | NIN | Effective | Supersedes |
|---|---|---|---|
| AT&T Retirement Savings Plan (ARSP) SPD/Prospectus | 78-74968 | July 2026 | `ATT-Retirement-Savings-Plan_78-63233.pdf` (2022) |
| BellSouth Savings and Security Plan (BSSP) SPD/Prospectus | 78-74971 | July 2026 | *nothing — new to the library* |
| Southeast Program of the AT&T Component Part, AT&T Pension Benefit Plan SPD | 78-74516 | Jan 1, 2025 | `202011---SPD---Southeast-Program...-49755.pdf` (2020) |

The ARSP PDF is filed in both `Management SPDs/` and `Bargained SPDs/` and was confirmed
**byte-identical** (md5 `3cf9a323…`), so it is one document, not two.

### New: the BSSP, and a plan-selection gate

- `index.html` §09 opens with a new **"First: which savings plan is this client in?"** block. The two
  plans are mutually exclusive by their own terms (each SPD disqualifies anyone eligible for the
  other). ARSP covers Southeast CWA D3 hired **on or after** Aug 9, 2009; BSSP covers the legacy
  Southeast/BellSouth units hired **before** that date.
- New `#bssp` subsection with a 13-row ARSP-vs-BSSP comparison and the full **weekly Basic
  Contribution band table** ($15 at ≤$299/wk up to **$67** at $1,300+/wk), annualized and costed at
  the April 2026 match rate.
- The BSSP differs in ways that void much of the standard playbook: **no Roth, no BrokerageLink, no
  Roth In-Plan Rollover** (so no mega-backdoor), contributions in whole dollars capped by pay band,
  match of **71% of Basic Contributions** (reset annually on corporate performance; 25% flat for
  Utility Operations), two general-purpose loans only, one General Withdrawal per 6 months, LifePath
  as QDIA, **120 days** to file suit.
- Highest-impact consequence, now flagged in three places: because the BSSP has no Roth and the law
  requires high earners' catch-up to be Roth, a BSSP participant age 50+ with 2025 FICA wages over
  $150,000 has a **catch-up limit of $0** — locked out entirely.
- **ASSP consolidation** documented: Southwest CWA participants hired/rehired before Aug 9, 2009 have
  been in the ARSP since **Jan 1, 2026** (SMM NIN 78-74837).

### Corrected: Roth catch-up is live, not pending

The guide previously hedged that bargained plans have until 2029 and that adoption was unconfirmed.
Both July 2026 SPDs state the rule as **currently in force** with no deferral. Removed the hedge
rather than softening it (leaving it would understate a rule now in effect) across `index.html` §09,
its calculator card and glossary, `non-bargained.html`, and `mobility.html`; added a plain-language
row to the `triggers.html` age table.

### Corrected: cash-balance mechanics were the wrong program's

`index.html` is Southeast-shaped, but §04 described a **pay-driven, age-graded** credit
(Pension Compensation × Age Credit Factor, monthly, plus a Supplemental Pay Credit on pay above the
Social Security Wage Base). The Jan 2025 Southeast SPD contains **no Age Credit Factor, no
Supplemental Pay Credit, and no wage-base credit** anywhere. Southeast is **band-driven**:

- **Basic Benefit Credit = 60 × the Pension Band Amount** for the highest band held that year,
  credited **annually** on Dec 31.
- **Interest Credit** = prior-November 30-year Treasury rate, applied to the **Jan 1 balance before**
  that year's credit is added, credited annually and **continuing after termination**.
- Opening balance for pre-1999 participants = greater of existing accruals or **$3,000**.

§04 now presents both designs, labels which programs each belongs to, and carries the SPD's own
worked example ($10,000 + $3,000 credit at 4.5% → **$13,450**). The pay-driven content was retained
and scoped rather than deleted, since it remains correct for other programs.

### Corrected: the Age Incentive Factor is not a constant

The guide treated it as a flat 1.06. It is age-graded (1.01 at 57 → 1.06 at 62+) and inverts on
Mod 75 status: **1.06 regardless of age if Mod 75 is *not* satisfied**, **1.00 if it *is* satisfied at
age 56 or younger**. Added the table plus an explanation of why it runs backwards (it offsets the far
larger 0.5%/month early-retirement subsidy), and a caution against comparing clients on it. The Rosa
Alvarez example was recomputed: at 56 with Mod 75 satisfied her factor is **1.00**, not 1.06, giving
$57.23 × 9 × 1.00 = **$515.07/mo**, with a sensitivity line showing **$545.97** at 62.

### Added: Southeast forms of payment, including the $75,000 Partial Lump Sum

New table in §08 mapping form availability to source and Mod 75 status. Two items newly surfaced:
every Southeast J&S carries a **pop-up**, and a Mod 75 satisfier may take a **fixed $75,000 Partial
Lump Sum** with the remainder as a residual annuity (not available to Special Represented Employees).
Also flagged that a Pension Band benefit **without** Mod 75 has **no lump-sum option at all**.

### Added: the 2015 management cliff

The Southeast SPD's program roster is the most current description of the **Management Cash Balance
Program** in the library, and it states the program **closed to hires/rehires after Dec 31, 2014**.
`non-bargained.html` §02 gained a hire-date routing table and a callout: management hired on or after
Jan 1, 2015 has **no pension at all**, which is precisely why that group receives the enhanced
133⅓%/100% match. The match is the pension's replacement, not a supplement.

### Other verified updates

- **Mobility Blue (IBEW 1547)** match eligibility moved from 1 Year of Service to **upon hire**
  effective Jan 1, 2024. Updated in the §10 table, the eligibility callout, `mobility.html`, and the
  calculator's option value (`flat100|1|shares` → `flat100|0|shares`).
- **Match tiers otherwise unchanged** from the 2022 edition — verified row by row, not assumed.
- **$360,000 annual compensation limit** and **$160,000 HCE threshold** added to all three guides,
  including the SPD's operational detail that contributions are **automatically suspended** on
  reaching the compensation cap (a second route into the per-pay-period match trap).
- **Mandatory cash-out $1,000 → $7,000** in both savings plans; new **Domestic Abuse Withdrawal**
  (lesser of $10,500 or 50% of vested account); loan and withdrawal rules for both plans; the 15-day
  hold on distributions after an address change.
- **Match investment exceptions** corrected to four groups — **AT&T Investment Operations I, LLC** was
  missing.
- **Plan identity** corrected throughout: the plan reverted to **AT&T Pension Benefit Plan** effective
  Jan 1, 2021 with **AT&T Inc.** as sponsor; Southeast is Plan Number **017**; savings-plan trustee is
  **The Bank of New York Mellon**.
- Two **internal inconsistencies in the ARSP SPD** are documented rather than silently resolved:
  Purple Contract shown as District 3 in one rule and District 6 in the summary; District 5 present in
  the eligibility list but absent from the immediate-match list.
- Source tables in all three guides rebuilt with NIN/effective/governs columns and an explicit
  **"superseded, do not cite"** note for the 2022 ARSP and 2020 Southeast SPDs.

### Consolidated Markdown references

- **`AT&T Union-Bargained Pension - Consolidated SPD & SMM Reference.md`** — §4.2 Southeast fully
  rewritten from the 2025 SPD (sum-not-greater-of structure, band-driven cash balance, Age Incentive
  Factor, forms of payment, disability eligibility difference, $25,000 retiree death benefit cap,
  break-in-service change, plan identifiers). Comparison matrix corrected in three rows. Edition
  warning added at the top, since five of six programs still rest on 2020 SPDs. **New Part 6** covers
  both bargained savings plans (coverage map, difference table, ARSP match ladder, BSSP band table,
  2026 limits, the Roth-catch-up consequence); old Part 6 renumbered to Part 7. Appendix rebuilt with
  the current-editions table and the incorporated-SMM chains.
- **`Management SPDs/_CONSOLIDATED-Management-Pension-SPDs.md`** — retitled to **AT&T Pension Benefit
  Plan**; sponsor/administrator/plan-number corrected with the historical names retained as such;
  program roster updated to the 15 current programs; **new Part 2 subsection** on the Management Cash
  Balance Program and the 2015 cliff with a hire-date routing table; Part 4 gained the $7,000
  mandatory cash-out and the $25,000 retiree death benefit cap; **new Part 5** documents the ARSP as
  the management 401(k) (identifiers, auto-enrollment, match tiers, 2026 limits, Roth catch-up,
  BrokerageLink/loans/withdrawals/distributions, RMDs, the Sept 2026 Roth split).

### Files changed

`index.html` · `non-bargained.html` · `mobility.html` · `triggers.html` ·
`AT&T Union-Bargained Pension - Consolidated SPD & SMM Reference.md` ·
`Management SPDs/_CONSOLIDATED-Management-Pension-SPDs.md` · `PLAN_LOG.md` · `TODO.md` ·
`CHANGE_LOG.md`

### Validation

- HTML tag-balance check across all **7** pages — all pass.
- Internal anchor check on all four guide pages — **0 broken anchors**.
- Local server render at desktop (1265px) and mobile (375px): **no horizontal page overflow**; all
  five wide new tables confirmed inside `.tscroll` containers with `overflow-x: auto`.
- **0 console errors** on `index.html` and `triggers.html`.
- Section 11 calculator re-tested after the option-value change: Mobility Blue at **0 years of
  service** now correctly returns match ($5,700 on $95,000 at 6%) instead of zero.
- No stale `78-63233` citations remain outside the deliberate "superseded" notes.

### Status

Complete. Three open TODO items closed (Roth catch-up adoption date; bargained savings-plan
identification; Management Cash Balance coverage), one downgraded from latent bug to cosmetic (the
415(c) target rate above $1M, now provably unreachable given the $360,000 compensation cap), and six
new items opened, most notably that `case-studies.html` has not yet been checked against either the
BSSP plan gate or the corrected Southeast cash-balance mechanics.

## 2026-08-13 — Portable build spec for the contribution calculator (written outside this repo)

Wrote `C:\Users\james\Projects\CONTRIBUTION-CALCULATOR-SPEC.md`, a standalone spec for rebuilding
the Section 11 calculator in other employers' resource guides. It lives outside this repo at the
user's request; no page in this project changed.

The spec generalizes the AT&T implementation in one significant way: match formulas are expressed
as a **tier ladder** (`[{upTo, rate}]`) rather than the named-formula enum used here, which covers
flat and multi-tier formulas with the same code path, and the "rate to fill 415(c)" is solved with
a **piecewise-linear segment solver** instead of this repo's closed-form shortcut.

Verified rather than asserted: a standalone page was assembled purely from the spec's CSS, HTML,
and JS blocks and driven through the documented test vectors. All five formula cases reproduce this
project's live output exactly ($95k and $200k across flat 80%, flat 25%, and the 133⅓%/100%
ladder), along with catch-up across six birth years, the empty-compensation, zero-rate,
not-yet-eligible, and unvested states, and the exact-fill boundary at $200,000. The generalized
solver also returns 1.54% at $2,000,000 of compensation, which checks out to exactly $72,000 of
additions, where this project's shortcut fails.

**Only change inside this repo:** a TODO entry recording that 415(c) limitation, with a pointer to
the corrected approach.

**Files:** `TODO.md`, `CHANGE_LOG.md` (this repo); `CONTRIBUTION-CALCULATOR-SPEC.md` (outside).
**Status:** complete.

## 2026-08-12 (4) — Calculator becomes Section 11, gains DOB and 402(g)/415(c) limit tracking

**The calculator is now its own section**, "Contribution & limits calculator", directly after the
match section. It reuses the existing `#match-calc` id (previously on its `<h3>`) as the section id
so any saved links still resolve. Sections after it shift by one again: IRMAA 11→12, strategy
12→13, protections 13→14, glossary 14→15, contacts 15→16. Nav now carries 16 items.

**New: date of birth.** Drives catch-up eligibility only. The SPD ties catch-up to age at the
**end of the calendar year**, not the birthday, so the tool computes `2026 − birth year`: under 50
none, 50–59 $8,000, 60–63 $11,250, 64+ back to $8,000.

**New: three IRS limit cards** in a second results row.

- **402(g) elective deferrals** — reads "Maxed" or the dollar amount with the shortfall. When the
  contribution rate pushes past $24,500 the card explains that the remainder continues as
  after-tax under the spillover election.
- **415(c) total additions** — contributions plus match against $72,000, with the remaining
  headroom called out as the after-tax room that feeds the mega-backdoor Roth.
- **Catch-up available** — the dollar capacity, the client's year-end age, and a reminder that
  catch-up sits outside both limits, is never matched, and is exempt from 415(c).

**New: two target-rate boxes** using the existing `.calc .out` component:

- **Rate to max the 402(g) limit** = $24,500 ÷ Compensation.
- **Rate to fill the 415(c) limit** = ($72,000 − match) ÷ Compensation. The match is fixed at its
  cap for any rate at or above 6%, so this is exact rather than circular. Both clamp to the plan's
  **50% cap on Basic Contributions**, and when 415(c) needs more than 50% the box reports "Not
  reachable" with the actual ceiling instead of printing an impossible rate. A third case covers
  Compensation so high the match alone fills 415(c).

The contribution-rate slider went from 0–20% to **0–50%** to match the plan's Basic Contribution
cap, otherwise the suggested rates were unreachable in the UI.

**Guardrail on the target rates.** A rate high enough to fill 415(c) collides with the
per-pay-period match trap, so the calculator's note now states that the spillover election must be
on, or deferrals stop mid-year and every remaining paycheck forfeits its match. The section's
advisor's lens repeats it and frames the output as arithmetic against an IRS ceiling rather than a
recommendation about what a client can afford.

**`ANNUAL-TAX-FIGURES.md` updated.** The four indexed limits are now hard-coded in JavaScript as
well as prose, which prose search-and-replace would miss. The checklist gained a step for the JS
constants block and a warning under the 401(k) limits table showing the exact code to edit.
`PLAN_YEAR` must move with the dollar figures because it drives catch-up eligibility.

**Files:** `index.html`, `ANNUAL-TAX-FIGURES.md`, `PLAN_LOG.md`, `CHANGE_LOG.md`, `TODO.md`.
**Validation:** limit math hand-checked at $95,000 and $200,000 across 6%, 26%, 36%, and 50%
contribution rates, including the exact-fill case ($200,000 at 31.2% reaches $72,000) and the
unreachable case ($95,000, where 415(c) would need 71% against a 50% cap). Catch-up verified at
birth years 1990 (none), 1970 (age 56, $8,000), 1964 (age 62, $11,250), 1962 (age 64, back to
$8,000), and with the field cleared. All 16 sections and nav items in order, no broken anchors, no
duplicate ids. No console errors; zero horizontal overflow at 867px and 375px, with both results
grids and the target-rate panel collapsing to one column on mobile. Screenshots were again
unavailable (the preview pane is not compositing), so verification was structural and by
measurement.
**Status:** complete.

## 2026-08-12 (3) — The company match becomes Section 10; Compensation input formats as currency

**The match is now its own section.** All employer-match material moved out of §09 into a new
`#match` section, "The company match", with its own sidebar entry. This is the first change in the
project that renumbers sections, so everything downstream shifted by one:

| Section | Before | After |
|---|---|---|
| The 401(k) plan (`#savings`) | 09 | 09 |
| **The company match (`#match`)** | — | **10 (new)** |
| IRMAA planning | 10 | 11 |
| Strategy playbook | 11 | 12 |
| Protections & rules | 12 | 13 |
| Glossary | 13 | 14 |
| Contacts & sources | 14 | 15 |

The new section carries, in order: the match intro and Matching Formula callout, the
formulas-by-contract table, the match-eligibility warning, the AT&T Shares default, the
per-pay-period match trap, the calculator and its disclaimer, an advisor's lens, and Rosa's match
example. Two headings promoted from `<h4>` to `<h3>` now that they sit at section top level.

**Consequences handled with the move:**

- Body cross-references updated: Rosa's full-picture summary now cites Section 10 for the match and
  Section 11 for IRMAA, and the match-eligibility callout's "(Section 09 above)" became a working
  link back to `#savings`.
- `#savings` lost its client example when Rosa's match example moved, so it gained a new one
  covering what that section still owns: unused 415(c) headroom for after-tax contributions, the
  Rule of 55, and handling a 401(k) loan before a rollover. The match example dropped its trailing
  pre-tax/Roth clause so the two don't duplicate each other.
- `case-studies.html` links only to guide sections 04–08, all upstream of the insertion point, so
  it needed no changes.

**Compensation input now formats as currency.** The field displays `$95,000` instead of `95000`.
It changed from `type="number"` to `type="text"` with `inputmode="numeric"` (a number input cannot
render a currency mask), reformatting on every keystroke and restoring the caret by counting the
digits before it, so editing mid-number doesn't jump the cursor to the end. Non-digits are
stripped, leading zeros collapse, and input is capped at 9 digits. A `readComp()` helper is the
single place the value is parsed back to a number. Added a guard for empty or zero Compensation,
which previously showed a misleading "capturing the full match" banner with $0 in every card; it
now reads "Enter an annual Compensation amount". A visually hidden `.sr-only` hint describes the
formatting behavior for screen readers.

**Files:** `index.html`, `PLAN_LOG.md`, `CHANGE_LOG.md`, `TODO.md`.
**Validation:** all 15 sections and all 15 nav items verified in order with zero broken anchors.
Currency field tested for typing, retyping, letters, leading zeros, over-length input, empty state,
and caret position on a mid-string edit that forces regrouping. Calculator re-checked end to end
after the move (tiered formula at $140,000 and 3% returns $5,600, the SPD's 4%-of-pay result). No
console errors; zero horizontal overflow at 1280x900 and 375x812. Screenshots were unavailable this
session (the preview pane stopped compositing), so verification was structural and by measurement
rather than visual.
**Status:** complete.

## 2026-08-12 (2) — Union guide §09: documented match formulas and a match calculator

Replaced the union guide's generic company-match copy with the actual formulas from
`Bargained SPDs/ATT-Retirement-Savings-Plan_78-63233.pdf`, and added an interactive calculator
built on the same pattern as the Section 07 Mod 75 calculator. `index.html` only.

**Match formulas by contract family** (new 13-row table). The SPD's baseline is 80% of the first
6%, with special rules for Mobility Orange / Purple / Black / Blue, National Internet Tier 1,
Technical Services, AT&T Corp. Core CWA, AT&T National Contract IBEW, Teamsters Local 959, and
BellSouth Utility Operations. Max match ranges from **1.5% to 7.0% of pay**, a four-fold spread
between groups contributing the identical 6%, which the page calls out explicitly.

**Two corrections to what the guide previously said:**

- **Match eligibility is not generally upon hire.** Only Management, Mobility Orange, Purple,
  Black, and National Internet Tier 1 are eligible upon hire. Every other group waits **one Year
  of Service**, so a newly hired union client's first year of contributions earns no company
  money. Added as a warn callout.
- **The match lands in the AT&T Shares Fund by default** for most groups (exceptions: Technical
  Services, Legacy T-IBEW hired on or before 8/8/2009, Cricket/AIO). Diversification is immediate
  and unlimited, so a long-tenured client can be carrying a large concentrated position nobody
  chose. Added as a gold callout with an NUA-before-rollover pointer.

**Company match calculator** (`#match-calc`): contract-family select, Compensation, contribution
rate slider, and years of service. Returns a status banner (full match / leaving $X on the table /
not yet eligible / contributing nothing), three result cards (annual match, match left on the
table, vesting), and a note line that switches on where the match is invested and warns when the
contribution rate crosses the 402(g) limit. Reuses the Mod 75 calculator's `.calc`,
`.status-banner`, `.results`, and `.rcard` markup so the two tools look and behave the same.

**Also updated:** the section's "verify the specifics" callout now names the SPD and states its two
limits (2022 edition, tiers set by bargaining); the "Company match" confirm-card now lists formula,
eligibility, and vesting as three separate checks; and Rosa Alvarez's example is tied to the
baseline 80% tier with the calculator walkthrough, the BellSouth contrast, and the AT&T Shares
concentration point.

**Supporting CSS:** new `.tscroll` wrapper so the 4-column table scrolls inside its own container
instead of the page body, and `min-width:0; max-width:100%` on `.calc select` so long option
labels cannot force horizontal overflow. The second fix also removed a pre-existing overflow: the
guide now measures zero horizontal page overflow at 375px, where it previously had some.

Also tightened one sentence in the spillover callout ("generally the first 6% of pay" is now "the
first 6% of Compensation") and removed the em-dash in it, clearing one item from the TODO list.

**Files:** `index.html`, `PLAN_LOG.md`, `CHANGE_LOG.md`, `TODO.md`.
**Validation:** every one of the 13 contract options was driven programmatically and its output
checked against the SPD, including the SPD's own worked example for the tiered formula (3% → 4% of
pay, 6% → 7% of pay). Banner and card logic exercised at 0%, 4%, and 6% contribution rates and at
0.5, 2, and 22 years of service. No console errors. No horizontal page overflow at 1280x900 or
375x812.
**Status:** complete.

## 2026-08-12 — ARSP Roth / non-Roth investing split and BrokerageLink blackout

Added the September 2026 AT&T Retirement Savings Plan change to the site, sourced from
`Roth-Investing-Account-Notice_Pages_1-21.pdf` (Fidelity SMM/Prospectus Supplement and ERISA
blackout notice, issued against the July 2026 SPD).

**New subsection `#roth-split`** inside the existing Savings Plan section of all three guides
(`index.html` §09, `non-bargained.html` §11, `mobility.html` §06). No section or nav renumbering:
the block sits inside `#savings` rather than becoming a new numbered section. It covers:

- What changes on **Sept 21, 2026**: separate Roth and non-Roth investment elections in the
  Standard Plan Options, and BrokerageLink splitting into **BrokerageLink** (non-Roth) and
  **BrokerageLink Roth**.
- The **blackout**, ~4 p.m. ET Sept 14 to ~9:30 a.m. ET Sept 22, 2026: no purchases and no
  exchanges into or out of BrokerageLink, sell orders still allowed into Fidelity Government Cash
  Reserves, open orders canceled Sept 14 and not re-established, and the knock-on risk to a
  distribution funded from BrokerageLink. Standard Plan Options unaffected.
- A four-row **key dates table** (online/paper account-opening restriction, the 4 p.m. Sept 14
  cutoff, implementation Sept 21, blackout lift Sept 22).
- **Three client situations** as pillars (core lineup only / BrokerageLink without Roth /
  BrokerageLink with Roth), plus the NetBenefits Sources-chart method for telling them apart.
- **What does not carry over**: third-party authorization including advisor access, automatic
  investment of payroll contributions, dividend reinvestment elections, and cost basis.
- **The split methodology**: Roth percentage proration, excluded security types, rounding rules,
  the $100 true-up in core cash, the second proration above $100, odd lots, trailing dividends,
  and sub-one-share liquidation.
- **The forced-liquidation deadline**: if the client has not acted by Sept 14, 2026, AT&T has
  directed Fidelity to sell BrokerageLink assets on their behalf, in the stated order.
- The two **NetBenefits paths** for setting Roth elections (future contributions vs current
  balance), and an advisor's-lens framing that separates the asset-location opportunity from the
  operational deadline. The notice's own "this is not a recommendation" position is stated rather
  than an allocation being suggested.

**Also on all three guides:** four glossary terms (Standard Plan Options, BrokerageLink /
BrokerageLink Roth, blackout period, SMM), a Fidelity BrokerageLink contact line (800-890-4015,
Mon–Fri 8:30 a.m.–8 p.m. ET), and the SMM added to the source-documents line.

**`triggers.html`:** a plain-language, second-person version of the same notice in the timeline
section, matching the page's client-facing voice.

**Population-specific wording.** The union guide adds a caveat that the notice names the ARSP
specifically, so the advisor must confirm which savings plan a bargained client participates in
before applying the dates. The management guide ties the change to clients running the
mega-backdoor Roth through the plan's Roth In-Plan Rollover. The Mobility guide notes the
younger-skewing Roth runway.

**Files:** `index.html`, `non-bargained.html`, `mobility.html`, `triggers.html`, `PLAN_LOG.md`,
`CHANGE_LOG.md`, `TODO.md`.
**Validation:** all four pages rendered in preview at 1280x900 and 375x812. No console errors. No
new horizontal overflow (the only elements exceeding the viewport at 375px are the pre-existing
hero `.gear` decoration and the nav `select`). Date cells given `white-space:nowrap` so the
key-dates table does not break a date across lines at narrow widths; step-body `<strong>` replaced
with `<em>` because `.step .sc strong` is `display:block` and was orphaning the following
sentence. Nav, section numbering, and all calculators untouched.
**Status:** complete. Source PDF left untracked, consistent with the other SPDs in the library.

## 2026-08-11 — Tool renamed to "Client Milestones"

The "Financial Trigger Finder" is now called **Client Milestones** everywhere on the site.

- **`triggers.html`:** browser tab title, hero `<h1>`, the sidebar "Viewing" selector option
  ("Tools · Client Milestones"), the footer title line, and two internal JS comments.
- **Sidebar link on the three plan guides** (`index.html`, `non-bargained.html`, `mobility.html`):
  "Financial trigger finder" is now "Client Milestones".
- **Email export:** the pasted table's heading is now "AT&T Retirement Timeline: Your Upcoming
  Milestones" and its third column header is "Milestone" instead of "Trigger" (both the rich-HTML
  and plain-text versions). The popup-fallback tab title changed to match.
- **Not changed:** the `triggers.html` filename and all links to it, so the published URL and any
  saved bookmarks still work. Ordinary verb uses of "trigger" in the guides (withholding, IRMAA
  cliffs, 401(k) loan defaults) were left alone, they are correct as written.

**Files:** `index.html`, `non-bargained.html`, `mobility.html`, `triggers.html`, `PLAN_LOG.md`,
`CHANGE_LOG.md`, `TODO.md`.
**Validation:** rendered in preview, no console errors; title/heading/footer/selector confirmed;
calculator still produces result cards; no logic, dates, dollar figures, or disclaimers touched.
**Status:** complete.

## 2026-07-23 (3) — Trigger Finder: rewritten in plain, client-facing language

Reworked all copy on `triggers.html` so it speaks directly to the client in simple language,
instead of to the advisor.

- **Voice:** "the client / they" became "you" throughout; advisor coaching ("map the date before
  the client gives notice," "the decision to model," "before advising") became plain guidance or
  "talk with your advisor."
- **Plain words for jargon,** without changing the underlying rules or numbers: "Modified Rule of
  75 / Mod 75" is now just "Rule of 75"; the age/service combos read "age 50 with 25 yrs" instead
  of "50/25"; MAGI/IRMAA are described as "your income" and "the Medicare surcharge"; 402(g)/415(c)
  limits are "the standard limit"; segment rates are "the interest rates used to set a lump sum";
  deferred-vested/Appendix B factors are "bigger cuts"; "commence" is "start your pension"; NUA is
  "a special tax break for company stock."
- **Sections touched:** hero, the input form (labels, radios, help text, and the warning box), the
  timeline heading/intro, the reframed "Why your last day matters most" box (was "The advisor's
  lens"), the age-reference table and its footnote, and the footer/disclaimer. The sidebar section
  labels now read "Your information / Your timeline / When you leave / Milestones by age."
- **The interactive output too:** the four result cards, every timeline entry, the whole
  separation checklist, and the email-export text now use the same plain second-person voice. The
  export table keeps the columns Age · Approx. Date · Trigger · Description as before.
- Calculation logic, dates, dollar amounts, and all disclaimers are unchanged.

**Validated in preview:** no console errors; union, Mobility, and terminated "missed milestone"
scenarios all render correctly in plain language; the dynamic leaving-date label updates; the email
export still copies with the new wording; no horizontal overflow at desktop or mobile. **Status:
complete.**

## 2026-07-23 (2) — Trigger Finder: export future triggers as an email-ready table

Added a **"Copy future triggers as a table (for client email)"** link to `triggers.html` in the
Trigger timeline section.

- Clicking it copies every **future** trigger (dated today or later) to the clipboard as a
  formatted table with columns **Age · Approx. Date · Trigger · Description**, ready to paste into
  an Outlook/Gmail message. The table uses inline styles (email clients strip `<style>` and
  classes), a dark header matching the guide, zebra striping, a short title/context line, and a
  "planning aid, not advice, verify" footnote. A tab-separated plain-text version is copied
  alongside the HTML.
- Copy path: `navigator.clipboard.write` (rich HTML) → `execCommand('copy')` rich-selection
  fallback → open the table in a new tab for manual copy if the clipboard is blocked. A status
  line confirms how many triggers were copied, warns when the timeline isn't built yet, or notes
  when the client has no remaining future triggers.
- Implementation: the timeline `items` array (already built in `render()`) is exposed via
  module-scoped `lastItems`/`lastDob`; the exporter filters to `d >= today` and reuses the
  timeline's own age/date formatting so the email matches the on-screen timeline.

**Validated in preview:** default client copied 13 future triggers; captured clipboard HTML had
exactly the four columns and 13 rows; plain-text twin present; the age-92 "no future triggers"
guard fired correctly; no console errors; no horizontal overflow at desktop or mobile. **Status:
complete.**

## 2026-07-23 — Client Examples across all three guides + non-bargained nav fix

Two requests, modeled on the PGE Benefit Resource Guide.

- **Client Examples added to every teaching section of all three guides.** New CSS in each page:
  a `--client:#6E4B9E` variable plus `.callout.client{border-left-color:var(--client);
  background:#f2ecf8}` and `.callout.client .tag{color:var(--client)}`, the same violet callout the
  PGE guide uses. Each callout is `<div class="callout client"><span class="tag">Client example:
  NAME</span>…</div>` with worked numbers computed from that section's own formula. Recurring
  characters carried section to section:
  - **index.html (Union): 12 examples** — Rosa Alvarez (CWA D9/West, hired 1990, blended Pre-99 +
    cash balance) and Marcus Bell (IBEW, hired 2012, cash-balance only). Sections 01–12 (landscape
    intro, eligibility, two-formulas, cash-balance mechanics, Pre-99 band, Mod 75, calculator,
    payment, 401(k), IRMAA, strategy capstone, protections).
  - **non-bargained.html (Legacy Non-Bargained): 16 examples** — Karen Whitfield (legacy SBC mgmt,
    hired 1988, CAM controlling, $3,200/mo) plus Dennis Okafor (promoted from a Midwest band 2003)
    in the PBM section. Sections 01–16 (all substantive sections through protections).
  - **mobility.html (Mobility): 10 examples** — Tanya Brooks (CWA Orange, hired 2010, cash-balance
    only). Sections 01–10. Key teaching beat: staying to 55/20 unlocks retiree-medical access even
    though the pension has no Rule of 75.
  - Glossary and Contacts sections intentionally left without examples (definition/directory
    content, as in the PGE reference). Capstone "full picture" example closes each strategy section.
- **Left-rail nav fix (non-bargained.html).** The "Financial trigger finder" and "Case studies:
  test yourself" links were missing `class="navitem"`, so they rendered unstyled (no block padding,
  hover, or active state). Added the class to both; verified computed styles now match the other
  nav items (display:block, 26px padding, 3px transparent left border, Helvetica).

**Validated in preview (local http.server):** client-callout counts 12/16/10 (38 total) with the
correct `#6E4B9E` border / `#f2ecf8` background; nav links styled identically to siblings; no
console errors; no horizontal overflow at desktop (1280) or mobile (375). Em-dash grep found only
5 **pre-existing** dashes in unrelated copy (card headings, 401(k) match paragraphs); none in the
new examples. **Status: complete.**

## 2026-07-20 (4) — Trigger Finder: MOD 75 card, FRA relabel, radio order

Three UI requests on `triggers.html`:

- **Radio order:** "Enter using" now lists **Ages / years first**, Specific dates second (ages
  remains the default-checked option, unchanged).
- **Snapshot banner replaced with a MOD 75 card.** The old free-text status banner ("Snapshot:
  Age... yrs of service... group... separation...") is gone from normal flow; that same client
  summary is now folded into a new **first result card labeled "Mod 75"**, styled identically to
  the Rule of 55 / Retiree-medical gate / Birth-year cards, with exactly one of three values:
  **Met** (good/green), **On-Track to Meet** (neutral/blue), or **Not Met** (warn/red). The banner
  element still exists but is now used only for the two input-validation error states (future DOB,
  separation before hire); it renders empty otherwise.
- **Result-card grid** changed from 3 columns to **2 columns** (`.results` CSS) to hold the new
  4th card as a clean 2x2 instead of 3-then-1.
- **Birth-year rules card renamed to "Social Security FRA"**, and its description now spells out
  "Social Security full retirement age (FRA)" on first use instead of the bare abbreviation.

**Validated in preview:** radio order confirmed (Ages / years, Specific dates); grid renders 2
columns at desktop width, 1 column on mobile with no overflow; all three Mod 75 states exercised
(Met/green, On-Track to Meet/blue, Not Met/red) with correct snapshot text folded into each
description; FRA card description confirmed spelled out; console clean; zero em-dashes.

## 2026-07-20 (3) — Trigger Finder: employment status now drives eligibility logic

User flagged that toggling **Terminated** only changed labels; the cards and timeline still
treated the client as accruing service, so a milestone the client can no longer reach (Mod 75,
the age-55 subsidy) was still shown as reachable. Employment status now feeds the engine, not
just the copy.

**Rule applied (per the guides: Mod 75 is tested *at termination*).** A terminated client accrues
no further service, so the Modified Rule of 75 / Medical-Program Rule-of-75 is now resolved to
**met or missed as of the termination reference date** (the separation date, or today if none is
entered), never "on track". Age-based triggers (59½, Social Security, IRMAA, Medicare, RMDs) are
unaffected because they do not depend on employment.

**What now changes when Terminated is selected:**
- **Retiree-medical gate card** flips from "On track" to "Missed at sep." / "Not met at term."
  when the milestone was not reached by termination.
- **Rule of 55 card** shows "Needs sep. date" (with guidance) when terminated without a date,
  instead of the active-client "Opens Jan YYYY".
- **Mod 75 timeline item** renders as a red warn card ("NOT met at termination") instead of a
  neutral "on track" milestone.
- **Age-55 timeline item** explains the subsidized early-commencement schedule does not apply
  when Mod 75 was missed (steeper deferred-vested factors to 65 instead).
- **Vesting** is treated as lost if the client is terminated before the 3-year cliff even with no
  date entered.
- **Banner, separation checklist, Roth-conversion window, and 401(k)/Rule-of-55 step** all reword
  for the terminated case (service "at termination", counterfactual milestone framing, etc.).
- When entering **years of service in Ages mode for a terminated client**, the value is now
  anchored to the separation date (service *at termination*), not to today.

**Validated in preview:** toggling a 53-yr-old/20-yr union client between Active and Terminated
flips the retiree-medical gate (On track → Not met), the Rule of 55 card (Opens 2028 → Needs sep.
date), and the Mod 75 timeline item (neutral → red warn), with the banner updating in step;
a terminated mgmt client who separated in 2024 at 56/26 correctly shows Mod 75 met + Rule of 55
applies; a terminated union client who left at 52/22 shows all three missed with the reworded
age-55 item. Console clean; no em-dashes.

## 2026-07-20 (2) — Trigger Finder: explicit entry-mode/employment radios, em-dash cleanup

User asked for radio buttons instead of the implicit "date wins over number" input model:
**Employee group** moved to the first field; a new **Employment status** radio (Actively
employed / Terminated) sits with it; a new **Enter using** radio (Specific dates / Ages or
years) explicitly toggles the DOB and hire-date rows between date pickers and
age/years-of-service number fields (previously both were always visible with an "or" label).
The separation-date label now reads **"Planned Date of Separation"** when Actively employed is
selected, and reverts to **"Date of Separation"** for Terminated; the "(planned)" wording in the
banner/timeline/checklist is now driven by that explicit radio instead of guessing from whether
the entered date is in the future.

**Also fixed:** the design-hook flagged em-dash overuse (68 instances) introduced in the initial
build, which violates the explicit CLAUDE.md rule against em-dashes in user-visible copy. Rewrote
every instance in `triggers.html` (title, labels, table cells, footer disclaimer, and every
generated timeline/checklist/card string in the JS) using periods, commas, colons, or parentheses
instead, matching the "·" separator convention already used elsewhere on the site.

**Validated in preview:** default state confirmed (ages mode, date rows hidden, "Planned" label
shown for the default Actively-employed status); toggling both radios confirmed to flip row
visibility and label text correctly in both directions; a full render with exact dates and
"Terminated" selected confirmed the "(planned)"/"at separation" wording now tracks the radio
rather than the date; zero em-dashes remain (`grep` count 0); console clean; no mobile overflow.

## 2026-07-20 — Financial Trigger Finder tool (triggers.html)

New interactive advisor tool: enter a client's **DOB (or age), hire date (or years of service),
separation date (actual or planned), and employee group** (Union/Bargained, Management Legacy
Non-Bargained, Mobility) and get the dated financial triggers to review — rendered as a
chronological timeline (passed / next-up / flagged), three verdict cards (Rule of 55,
retiree-medical gate, birth-year FRA + RMD rules), a separation-date checklist, and a static
age-trigger reference table with authoritative source links.

**Trigger engine covers:** catch-up at 50 ($8,000) · Rule of 55 (calendar-year test, IRA-rollover
forfeiture warning) · 59½ · super catch-up 60–63 ($11,250) · Social Security 62 / FRA by birth
year / 70 · IRMAA two-year lookback from 63 ($109k/$218k 2026 tiers) · Medicare IEP (65 − 3 mo)
and 65 (COBRA-not-employer-coverage trap) · QCDs at 70½ · RMDs at 73/75 by birth year (born-1959
footnote) · 3-year vesting cliff · Mod 75 milestone dates (any/30, 50/25, 55/20, 65/10) with
group-specific reduction rules (union 0.5%/mo + 55/56 threshold ages; NB CAM/PBM 0.5 vs 0.25%/mo;
Mobility: medical-only Rule-of-75 test, no pension timing). Separation checklist adds COBRA-to-
Medicare gap math, group-specific retiree-medical copy (management access-only post-1/1/2022,
bargained subsidy note, Alight), pension commencement, 401(k) loan/NUA, severance interplay, and
the Roth-conversion window sized to FRA/RMD years. All rules reused from the SPD-verified guides.

**Also:** "Tools" nav link added to all three guides; `ANNUAL-TAX-FIGURES.md` updated so yearly
figure updates include the new page; TODO notes the design-hook waiver extension and follow-up
ideas (filing-status input, West/Southeast sub-select, 1959 RMD final regs).

**Validated in preview** (localhost static server): three scenarios exercised — union on-track
(age 52/22 defaults), management with exact dates (Mod 75 met Mar 2023 via 50/25, Rule of 55
applies, COBRA gap 58 months short of Medicare), and a union/Mobility missed-milestone case
(32 months short, warn flags throughout); mobile viewport collapses with no horizontal overflow;
console clean on all runs.

## 2026-07-14 (2) — Mod 75 no longer implies subsidized healthcare (non-bargained guide)

User flagged Section 08 of `non-bargained.html` as implying management employees can still get
subsidized retiree healthcare once Mod 75 is met. Verified against the **Dec 2020 Retiree Benefit
Changes** notice (pp. 3–5) and **Medical SPD 2021** (pp. 51–52): Mod 75 gates *eligibility to
enroll* only. For any management employee whose last day on payroll is on/after **1/1/2022**
there is **no Company subsidy**, regardless of hire date (pre-Medicare sunset announced
12/15/2020; the Medicare-side subsidy/HRA already ended for last days on/after 1/1/2021). The
old hire-date/legacy rules matter only for those who retired by the cutoffs.

**Fixes in `non-bargained.html`:**
- Subsidy callout retagged "For management retiring now, there is no subsidy" and restructured
  to lead with the bottom line; the "only pre-2001 hires may qualify" line reframed as history
  that creates no subsidy path today; added that Mod 75's healthcare value is guaranteed group
  access, not a discount.
- Gold "pre-Medicare bridge" callout: enrollment now noted as at the retiree's own cost, and the
  Medicare Part B/D premium-reimbursement mention corrected (that subsidy ended 1/1/2021).
- Mod 75 trap #2 clarified (pension subsidy + retiree-medical *enrollment eligibility*).
- Section 09 calculator: intro no longer says "candidate for subsidized retiree healthcare";
  result card renamed "Retiree healthcare eligibility"; eligible-state text now says access
  only, 100% of Cost of Coverage for management retiring on/after 1/1/2022; status-banner
  subtitle marks healthcare as unsubsidized for management retiring today.

**Validated in preview:** calculator exercised (55/25 → eligible card shows corrected label and
copy), old phrasing absent, no console errors. `case-studies-nb.html` already taught the rule
correctly (no change).

## 2026-07-14 — Correct "match excludes after-tax" claim (user-flagged; SPD-verified)

User flagged the Section 09 claim that the employer match applies only to pre-tax and Roth
deferrals, not after-tax contributions. Verified against
`ATT-Retirement-Savings-Plan_78-63233.pdf` — **the claim was wrong**: matched Basic
Contributions (first 6% of Compensation) "may be Before-tax Contributions, After-tax
Contributions, Roth Contributions, or a combination of any of the three" (p. 23), and the
default spillover election exists specifically so post-402(g) contributions continue as
after-tax and "continue to receive Company Match" (p. 24). Only catch-up contributions and
amounts above the 6% matched cap never earn match (pp. 24, 26).

**Fixes (all three guides for consistency):**
- `index.html` — Matching Formula callout no longer says "pre-tax or Roth contributions";
  front-loading callout rewritten: no true-up + per-period 6% cap stays, but spillover keeps
  the match alive after the deferral limit unless the client opted out or suspends; "Also
  note" paragraph replaced with the corrected rule (after-tax within 6% is matched; catch-up
  and >6% are not).
- `non-bargained.html` — same two-paragraph rewrite of the front-loading callout.
- `mobility.html` — same front-loading correction (its callout repeated the "contributions
  stop and so does the match" claim).

**Validated in preview** (localhost static server): old claim absent, new copy renders on all
three pages. Case-study pages checked — they don't repeat the claim.

## 2026-07-08 (3) — Mobility Program case studies (case-studies-mobility.html)

Completes the training set: **five client scenarios (24 checkpoints)** for the cash-balance-only
Mobility Program, same engine and visual system as the other two case-study pages. The plan is
simpler, so the quiz centers on NOT importing legacy-plan rules.

Coverage: (1) who's covered (Orange Contract bargained; legacy mgmt employed 12/31/2005) +
single-account structure, no greatest-of, no pension Mod 75, flat NRA 65, 3-yr vesting;
(2) mechanics (flat 5% credit → $300 on $6,000; broad Pension Compensation incl. §125/457/132(f)
and NQ deferrals; $120,000 × 0.327% ≈ $392.40 interest; no age-stepped factor, not frozen;
interest continues after termination); (3) annuity conversion ($100,000 ÷ 141.5292 = $706.57
SLA; 50/75% J&S only, no 100%; pop-up ALWAYS applies; 90%-of-SLA floor = $635.91 for pre-2006
participants; J&S cannot be waived by QDRO); (4) the timing game that is not there (lump sum =
account, not segment-rate-converted; only the quarterly Treasury crediting rate matters; 20%
withholding vs direct rollover; Rule of 55 forfeited by IRA rollover; $7,000 cash-out);
(5) the milestone that survived (Medical Program's own Rule-of-75-style test still gates retiree
medical for Mobility employees; 1 more year → 50/25 for a 53/24 client; post-2001 hire = 100% of
cost but group access still beats the individual market; no Retiree Death Benefit, survivor value
is the account, estate default). All facts mirror the SPD-verified `mobility.html`, including the
SPD's annuity-factor example; explanations deep-link its sections.

**Links:** "Training" nav item + Strategy Playbook callout in `mobility.html` (plain anchor, off
the `.navitem` observer); footer cross-links added in `case-studies.html` and
`case-studies-nb.html`; the new page's footer links back to both.

**Validated in preview:** no console errors on the quiz or the guide; wrong/right MC flow;
numeric wrong→hint→reveal-offer path; all 24 checkpoints solvable with the authored answer key
(every numeric accepted exactly); score 22/24 after two deliberate misses; every MC has exactly
one correct option; reset re-locks cases; all seven deep-link anchors exist in `mobility.html`;
its nav observer still runs; no horizontal overflow at desktop or 375px mobile. Design-hook
findings are the documented intentional visual-system exceptions (TODO.md note extended).

**Files:** `case-studies-mobility.html` (new), `mobility.html`, `case-studies.html`,
`case-studies-nb.html`, `PLAN_LOG.md`, `TODO.md`. Pushed as 5bdc354.

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
