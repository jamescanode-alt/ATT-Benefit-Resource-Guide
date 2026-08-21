# TODO

## Open

- [ ] **Rewrite the Sept 2026 Roth-split subsection after the event.** The `#roth-split` block on
      `index.html`, `non-bargained.html`, `mobility.html` and the client-facing callout in
      `triggers.html` are written in future tense against a Sept 14–22, 2026 blackout. After
      Sept 22, 2026: confirm the dates held, switch to past tense, drop the countdown framing, and
      keep only the durable mechanics (two BrokerageLink accounts, separate Roth elections, what
      had to be re-established).
- [ ] **Southeast/BellSouth savings-plan coverage needs a second pass beyond `index.html`.**
      The BSSP is now documented in `index.html` §09 and Part 6 of the union consolidated MD, but
      `case-studies.html` still assumes every bargained client is in the ARSP. Rosa Alvarez is a
      West CWA client so she is correctly in the ARSP, but any Southeast-flavored case study needs
      the plan gate applied. Also worth adding: a BSSP-specific client example, since the
      band-capped match and the $0 catch-up are the two most counterintuitive facts in the set.
- [ ] **Advisor authorization is an ops task, not just a page.** Third-party (advisor) access does
      not carry to the new BrokerageLink Roth account. Pulling the list of AT&T clients with
      BrokerageLink authorization and re-papering it lives outside this repo; the guides flag it,
      but someone has to own the list.

- [ ] **The Management Cash Balance Program's own SPD is still missing from the library.**
      Its *coverage* and its **Dec 31, 2014 closure** are now documented (transcribed from the
      program roster in the Jan 2025 Southeast SPD) in `non-bargained.html` §02 and Part 2 of the
      management consolidated MD, which is enough to route a client correctly and to explain the
      2015 pension/match cliff. What is still missing is the program's own benefit mechanics:
      credit rates, interest crediting, and annuity conversion factors. Get the SPD itself.
- [ ] **Frozen cash-balance detail.** The age-credit-factor schedule for the frozen Nonbargained
      cash-balance formula is not published in the SPD (directs to Recordkeeper). Left as a
      historical/interest-only balance by design; revisit only if source detail becomes available.

- [ ] **Strip 4 remaining pre-existing em-dashes.** All in `non-bargained.html`: the 401(k) match
      paragraph (~line 839) and the "greatest of three" card headings (~425/430/435: "CAM — the
      usual winner", "Cash Balance — frozen", "PBM — narrow"). The `index.html` one was cleared on
      2026-08-12 while the match copy was being rewritten. `index.html` is now em-dash free.
- [ ] **Apply the same match treatment to the other two guides.** `index.html` now has a dedicated
      Section 10 (`#match`) with the SPD's real match tiers, the one-Year-of-Service eligibility
      rule, the AT&T Shares default, and a contract-aware calculator. `non-bargained.html` §11 and
      `mobility.html` §06 still have prose-only match content inside their 401(k) sections. Their
      tiers are correct but they lack the eligibility and AT&T-Shares-concentration points and have
      no calculator. Porting means renumbering those guides too (nb: 12–18 shift to 13–19;
      mobility: 07–12 shift to 08–13), so treat it as a deliberate pass, not a quick copy.
- [ ] **Currency formatting is only on the union guide's match calculator.** If any other dollar
      input is added, reuse the `formatComp`/`readComp` pair and the `.sr-only` hint from
      `index.html` rather than writing a second implementation.
- [ ] **415(c) target rate is wrong above roughly $1M of Compensation (now confirmed cosmetic).**
      Section 11 solves the "rate to fill 415(c)" with the closed form `(72000 - maxMatch) / comp`,
      which assumes the match is already at its cap. Above about $1M the numerator goes negative and
      the box reports "Match alone fills it", which is false. The July 2026 SPD settles how much this
      matters: the plan caps countable Compensation at **$360,000** (2026), so no real participant
      ever reaches the broken region, and the disclaimer now names that cap explicitly. Downgraded
      from latent bug to cosmetic. The exact fix is still the piecewise-linear segment solver in
      `../CONTRIBUTION-CALCULATOR-SPEC.md` §3, verified to return 1.54% at $2M against a
      133⅓%/100% ladder (exactly $72,000 of additions). Port it if this section is ever revisited.

- [ ] **Consider applying the $360,000 compensation cap in the Section 11 calculator.** Currently
      the tool ignores it and the disclaimer says so. Applying it would be more than a clamp: the
      SPD says contributions are **automatically suspended** on reaching the cap, so a client above
      roughly $360,000 on a level rate stops contributing (and stops earning match) partway through
      the year. Modelling that honestly means modelling the pay-period timeline, not just capping
      the input, which is why it is flagged rather than done.

- [ ] **The BSSP has no calculator.** Section 11 models the ARSP only and now says so. A BSSP
      client's matched contribution is a weekly dollar band, not a percentage, so the existing tool
      cannot represent them. The band table in §09 is currently the substitute. If it is worth
      building, the logic is small: weekly pay -> band amount -> x52 -> x the current match rate.
- [ ] **The contribution calculator hard-codes the 2026 IRS limits in JavaScript.** `PLAN_YEAR`,
      `DEFERRAL_LIMIT`, `ADDITIONS_LIMIT`, `CATCHUP`, and `CATCHUP_SUPER` live in a constants block
      in `index.html` Section 11 and must be updated with the annual pass.
      `ANNUAL-TAX-FIGURES.md` now carries the step and the exact code, so this is a pointer, not a
      second checklist.
- [ ] **Recheck match tiers at the next ARSP SPD.** Verified row by row against the July 2026 SPD
      (NIN 78-74968) on 2026-08-21: the tiers themselves were unchanged from the 2022 edition; only
      Mobility Blue's eligibility timing moved (1 Year of Service -> upon hire, effective 1/1/2024).
      Tiers are still set by collective bargaining, so recheck at the next edition. The
      `#match-calc` option values and the formulas table in `index.html` are the two places to
      update. Note the BSSP match rate is reset **annually** on corporate performance (71% effective
      4/1/2026), so that one needs a yearly check regardless of SPD cadence.
- [ ] **RMD age for those born 1959+ is unresolved, and the SPDs are silent.** The July 2026 ARSP
      and BSSP SPDs both stop their RMD-age table at "73 if born on or after January 1, 1951, and on
      or before December 31, 1958" and state **no age at all** for 1959 or later. That silence is
      consistent with the open question rather than resolving it, so the hedge in `triggers.html`
      (and its `by<=1959` branch) stays as written. Revisit when IRS final regulations land.

- [ ] **Cash-balance mechanics are program-specific and the guide now says so, but only in §04.**
      The Jan 2025 Southeast SPD confirms Southeast uses a **band-driven** credit (60 x Pension Band
      Amount, credited annually) with **no Age Credit Factor and no Supplemental Pay Credit**, while
      the pay-driven age-graded design belongs to other programs. `index.html` §04 was corrected to
      present both and label which is which. Still to check: `case-studies.html`, whose worked
      examples may assume the pay-driven design for a Southeast-shaped client.

- [ ] **Verify Pension Band Amounts against Attachment 3 of the current SPD.** The Jan 2025
      Southeast SPD updated the Pension Band Tables per bargaining, and the guide's examples now use
      $57.23 for Band 111 (the SPD's own 2024-termination example) rather than the older $51.81.
      Band amounts vary by termination year, so any client-facing figure should be pulled from
      Attachment 3 for that client's year, not reused from an example.

- [ ] **Client Milestones enhancements (triggers.html).** Possible follow-ups: a tax-filing-status
      input so the IRMAA line shows only the relevant tier ($109k vs $218k); a West/Craft vs
      Southeast sub-select for the union threshold age (55 vs 56); confirm the born-1959 RMD age
      (73) once IRS final regs land; severance-schedule integration from the Severance Pay Plan.

## Done (2026-07-01, second pass — new SPDs added)

- [x] **401(k) savings-plan specifics** — sourced from `ATT-Retirement-Savings-Plan_78-63233.pdf`.
      Section 11 now states the real match tiers (80% of first 6%; 133⅓%/100% for mgmt hired ≥1/1/15),
      match on first 6% only, upon-hire eligibility, 3-year vesting, no true-up in the SPD, and the
      confirmed after-tax + Roth In-Plan Rollover mega-backdoor path.
- [x] **Retiree healthcare** — sourced from `Medical SPD 2021.pdf`. Mod 75 confirmed as the gate to
      retiree (Post-Employment) medical eligibility; corrected "subsidized" to "eligible to enroll,
      subsidy varies by group/hire date (up to 100% of cost)"; added the pre-Medicare-bridge nuance.

## Design hook (Impeccable) — intentional, not defects

- The `side-tab`, `border-accent-on-rounded`, and `overused-font` (Helvetica) findings on
  `index.html`, `non-bargained.html`, `mobility.html`, `case-studies.html`, `case-studies-nb.html`,
  `case-studies-mobility.html`, and `triggers.html` are deliberate: every page in the set mirrors
  the established union guide's visual system. Not changing unless the user wants the whole set
  restyled together.
