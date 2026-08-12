# TODO

## Open

- [ ] **Rewrite the Sept 2026 Roth-split subsection after the event.** The `#roth-split` block on
      `index.html`, `non-bargained.html`, `mobility.html` and the client-facing callout in
      `triggers.html` are written in future tense against a Sept 14–22, 2026 blackout. After
      Sept 22, 2026: confirm the dates held, switch to past tense, drop the countdown framing, and
      keep only the durable mechanics (two BrokerageLink accounts, separate Roth elections, what
      had to be re-established).
- [ ] **Confirm which savings plan bargained clients are in.** The Roth-enhancement notice names
      the AT&T Retirement Savings Plan (ARSP). `index.html` currently tells the advisor to verify
      the client's plan in NetBenefits before applying the dates. Resolve the caveat once a
      bargained savings-plan SPD lands in the library.
- [ ] **Advisor authorization is an ops task, not just a page.** Third-party (advisor) access does
      not carry to the new BrokerageLink Roth account. Pulling the list of AT&T clients with
      BrokerageLink authorization and re-papering it lives outside this repo; the guides flag it,
      but someone has to own the list.

- [ ] **Add the Management Cash Balance Program SPD to the library.** Most management employees
      hired after the mid-2000s cutoffs fall under this program, which is not yet documented in
      `Management SPDs/`. Until then, `non-bargained.html` Section 02 flags the gap and the
      Mobility summary is the closest available model.
- [ ] **Frozen cash-balance detail.** The age-credit-factor schedule for the frozen Nonbargained
      cash-balance formula is not published in the SPD (directs to Recordkeeper). Left as a
      historical/interest-only balance by design; revisit only if source detail becomes available.
- [ ] **Roth catch-up (SECURE 2.0) adoption date.** The Savings Plan SPD in the library is a 2022
      edition and predates the SECURE 2.0 Roth-catch-up specifics. Section 11 states management gets
      the standard (non-delayed) timing; confirm the plan's actual adoption when a current SPD lands.
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
- [ ] **Recheck match tiers when a newer ARSP SPD lands.** The SPD in the library is a 2022 edition
      and match tiers are set by the collective bargaining agreement, so a newer contract can move
      them. The `#match-calc` option values and the formulas table in `index.html` are the two
      places to update.
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
