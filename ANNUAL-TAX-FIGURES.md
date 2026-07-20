# Annual Tax-Year Figures — Update Checklist

> **Purpose.** Every figure in the three advisor guides (`index.html`, `non-bargained.html`,
> `mobility.html`) and the trigger-finder tool (`triggers.html`) that is **indexed and changes
> each tax year** is catalogued here with its current value, where it appears, and the
> authoritative source to check. Update these each year
> (typically late October–November, when the IRS COLA notice and the CMS/Medicare IRMAA figures
> for the coming year are released).
>
> **Current tax year in the guides:** 2026
> **Last verified:** 2026-07-02 (against the sources linked below)

---

## How to update each year

1. Pull the new figures from the **authoritative sources** in the tables below (don't rely on
   secondary/blog numbers for the final values).
2. Search each HTML file for the **old dollar value** and replace it. Suggested search per figure
   is in the "Find in code" column.
3. Re-check the **derived totals** (e.g., 402(g) + catch-up), they are hard-coded, not computed.
4. Update the **"Last verified"** date above and the year in each page's IRMAA sentence
   ("For reference, 20XX IRMAA begins above…").
5. Re-run the local preview and spot-check the 401(k) limits table and IRMAA paragraph on all
   three pages, plus `triggers.html` (timeline copy, the summary line under the inputs, and the
   Section 04 reference table carry the catch-up, 402(g), and IRMAA figures).

---

## 1. IRS retirement-plan limits (401k)

Authoritative sources:
- IRS annual COLA news release (fastest plain-language confirmation):
  https://www.irs.gov/newsroom/401k-limit-increases-to-24500-for-2026-ira-limit-increases-to-7500
  *(URL changes each year, search "IRS 401(k) limit increases for <year>")*
- IRS COLA limits table: https://www.irs.gov/retirement-plans/cola-increases-for-dollar-limitations-on-benefits-and-contributions
- IRS 401(k) contribution-limits topic page: https://www.irs.gov/retirement-plans/plan-participant-employee/retirement-topics-401k-and-profit-sharing-plan-contribution-limits
- Official COLA notice (technical): IRS Notice 2025-67 (for TY2026) — https://www.irs.gov/pub/irs-drop/n-25-67.pdf

| Figure | 2026 value | Appears in (all 3 pages, 401(k) section; catch-up figures also in `triggers.html`) | Find in code |
|---|---|---|---|
| 402(g) elective deferral limit (under 50) | **$24,500** | limits table + glossary + `triggers.html` | `$24,500` |
| 415(c) total additions limit | **$72,000** | limits table + glossary | `$72,000` |
| Catch-up (ages 50–59 & 64+) | **$8,000** | footnote + catch-up copy | `$8,000` |
| Super catch-up (ages 60–63) | **$11,250** | footnote | `$11,250` |
| Elective + catch-up total (50–59/64+) | **$32,500** | limits table | `$32,500` |
| Elective + super catch-up total (60–63) | **$35,750** | limits table | `$35,750` |
| 415(c) + catch-up total (50–59/64+) | **$80,000** | limits table | `$80,000` |
| 415(c) + super catch-up total (60–63) | **$83,250** | limits table | `$83,250` |
| SECURE 2.0 Roth-catch-up FICA wage threshold | **~$150,000** (indexed) | catch-up callout | `$150,000` |

> **Note on the super catch-up:** it is **not** simply 150% of the regular catch-up. Under SECURE
> 2.0 it is the greater of $10,000 or 150% of the 2024 base, indexed; for 2026 the IRS set it at
> **$11,250** (unchanged from 2025 even though the regular catch-up rose to $8,000). Verify against
> the IRS notice each year rather than computing it.

---

## 2. Medicare IRMAA thresholds

Authoritative sources:
- Medicare.gov costs / IRMAA: https://www.medicare.gov/basics/costs/medicare-costs
- SSA Medicare premiums (has the full IRMAA table): https://www.ssa.gov/benefits/medicare/medicare-premiums.html

Appears in the **IRMAA section of all 3 pages** ("For reference, 2026 IRMAA begins above …") and
in **`triggers.html`** (IRMAA-lookback timeline entry, the note under the inputs, and the
Section 04 reference table).

| Figure | 2026 value | Find in code |
|---|---|---|
| IRMAA first-tier threshold, single / MFS | **$109,000** | `$109,000` |
| IRMAA first-tier threshold, married filing jointly | **$218,000** | `$218,000` |
| Number of surcharge tiers | **5** (five-tier) | `five-tier` |
| Top-tier threshold, single | ≥ **$500,000** | *(not currently shown; add if needed)* |
| Top-tier threshold, MFJ | ≥ **$750,000** | *(not currently shown)* |
| Lookback | **2 years** (2026 premiums set by 2024 MAGI) | `Two-year lookback` |

> Reminder to keep in copy: IRMAA is a **cliff** (one dollar over a tier triggers the full
> surcharge) and is **per person** for a married couple. These features don't change yearly; only
> the dollar thresholds do.

---

## 3. Social Security wage base (union guide only)

Authoritative source:
- SSA Contribution and Benefit Base: https://www.ssa.gov/oact/cola/cbb.html

Appears in `index.html` only — the **Supplemental Pay Credit** section (Section 04) and its worked
example. The Non-Bargained and Mobility guides do not use this figure.

| Figure | 2026 value | 2025 (prior) | Find in code |
|---|---|---|---|
| Social Security Wage Base (taxable maximum) | **$184,500** | $176,100 | `$184,500` |

> When updating, also fix the **worked example** so year-to-date pay stays above the new wage base
> (currently "$189,500 as of Nov 30; wage base $184,500. Excess = $5,000").

---

## 4. Figures that are statutory (do NOT change yearly)

These appear in the guides but are set by statute/plan, not annually indexed, so they are **not**
part of the yearly update (still confirm if the law changes):

- Mandatory **20%** federal withholding on non-rollover lump sums.
- Mandatory cash-out thresholds: **≤ $1,000** (auto lump sum), **> $1,000 to ≤ $5,000** (auto IRA
  rollover). *(SPD-specific; some plans use $7,000 — verify per SPD, not per tax year.)*
- Pension formula factors (age credit factors, CAM 1.6%, PBM 1.2%, J&S percentages, annuity
  factors): these are **plan/SPD** values, updated only when a new SPD is issued, not yearly.
