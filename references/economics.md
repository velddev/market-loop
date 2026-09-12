# Runway and stagnation policy

Use these defaults for a new market, or an existing market whose user has authorized this economic-policy change. Freeze overrides before the affected quarter. Record the policy as `runway-v2`; retain earlier policies and settlements.

## Migrate without rewriting history

Keep all previous prices and measured results. If an old share price was a performance index, preserve it as `legacy_technical_score` with its original formula/reference. Start the new fictional valuation from the last published price (or $100 for a new company). Never present the new valuation as a throughput ratio.

Set `effective_quarter` to the next unstarted quarter, initialize runway to 3 and the new policy's operational streaks to zero. Retain historical delivery gaps separately. Do not retroactively burn runway, reprice old quarters or claim prior evidence as a new contribution. Applying this skill is not itself execution of the next quarter.

## Separate three measures

- **Technical result:** the audited product metric and any existing performance index, including workload, reference, uncertainty and qualification status. Preserve the project's scoring formula; a rejected/noisy submission does not improve it. Withdraw invalidated technical credit and recompute affected settlements transparently.
- **Share price:** a fictional valuation incorporating delivery and stagnation under this policy. Highest current valuation is the market leader; initial ties are unvalidated. Technical leadership requires comparable measured performance and may differ.
- **Runway:** finite simulated research capital, measured in quarter units. This controls eligibility and priority; it is not money, tokens or permission to exceed real resource limits.

Credit a measured contribution once, using a unique contribution ID and matched-control receipt. Inherited changes do not earn another delivery, technical credit, runway grant or price gain. For a new delivered contribution, `g` is its independently validated product-rate ratio to the matched common control (invert for lower-is-better metrics). Require `g > 1`; do not reuse an absolute ratio containing earlier or inherited gains. If the product cannot be expressed by this ratio, predeclare a task-specific delivery reward instead.

Freeze the aggregation rule before dispatch. Default to the geometric mean of the paired candidate/control ratios across all declared qualification trials; do not select only winning workloads or test orders. A favorable aggregate still requires the agreed correctness and variability gates.

## Classify the quarter

The parent decides from evidence against the frozen milestone, not company rhetoric.

| Outcome | Required evidence | Runway grant | Valuation factor | Next discretionary-slot weight |
| --- | --- | ---: | ---: | ---: |
| Delivery | New, qualified product improvement adopted into the shared release | 2 | `g` | 2 |
| Learning | A new reproducible result resolves a declared hypothesis or passes a named integration gate and changes the next engineering decision; positive or negative | 0.5 | 0.95 | 1 |
| Stagnant | Neither delivery nor qualifying learning despite a feasible funded opportunity | 0 | 0.80 | 0.5 |
| Opportunity-blocked | Parent queue, common baseline or external failure prevented the declared opportunity, with receipts | No burn or grant | 1 | Protected retry |

Learning credit is once per unique hypothesis/gate, with a linked next action. Rewritten reports, duplicate tests, inherited improvements, arbitrary refactoring, unacted-on observations and inconclusive timing alone do not qualify. A later quarter that ignores the evidence can be stagnant. Unfunded/retired companies do not accrue another operating quarter merely because a press note is published.

For mixed evidence, apply this precedence: qualified delivery; otherwise opportunity-blocked if the promised decisive opportunity was denied; otherwise learning; otherwise stagnant. Preserve useful side results from a blocked quarter without a financial grant, and do not repackage them as new evidence later. Freeze the promised opportunity before dispatch so companies cannot invent a missing gate after receiving an unfavorable result.

For each funded, nonblocked quarter, calculate in this order:

```text
runway_after = min(3, max(0, runway_before - 1 + grant))
price_after = price_before * valuation_factor
stagnant_streak = previous + 1 if stagnant, otherwise 0
delivery_drought = 0 if delivery, otherwise previous + 1
```

Clamp runway after combining burn and grant, not before. Store unrounded prices for subsequent calculations; round only display values. Opportunity-blocked preserves both streaks. If a company received its promised opportunity but spent it on avoidable local failures, it is not opportunity-blocked. If partial access was insufficient, record the referee's allocation error and protect the missing opportunity.

## Enforce pivots and restructuring

- At two consecutive stagnant quarters: `pivot_required`. Fund only a cheap screen of a materially different mechanism, architecture or resource plan. The parent records why it addresses the failed thesis. A new name or another tuning constant is insufficient.
- At three funded quarters without delivery, or zero runway: `restructuring_required`, which takes precedence over a pivot. Apply a one-time 0.5 valuation haircut for that restructuring event. Freeze further spending on the old approach and preserve its source/results.
- Restructuring replaces the approach, not its history. A successor plan must identify the failure, a different thesis and one quarter's delivery gate. Default to at most one funded successor per company during the user's current research budget, drawing one quarter unit from a finite, predeclared program reserve. No available reserve means the approach retires; do not create free capital.
- An approved successor retains valuation/history, starts a new strategy epoch with operational streaks zero and runway exactly 1, and enters one-quarter probation. No automatic restoration to $100 or runway 3. Only a qualified delivery passes a funded, nonblocked probation quarter; otherwise retire that approach, with no further automatic restart. A delivery settles normally and ends probation. Opportunity-blocked freezes probation and receives a protected retry within the existing real budget; it does not consume another successor grant.

Apply a restructuring haircut once per event ID, not again when resuming the same decision. A longer research horizon or larger reserve can be agreed before dispatch with explicit milestones; do not extend it after a miss just to avoid a consequence.

## Allocate actual effort

Before the quarter, declare the total real budget, shared evaluation overhead, a screening allowance per funded company, protected retries, and a bounded restructuring reserve (default: one quarter unit for the whole program). Split remaining discretionary slots in proportion to the table's weights, subject to runway/status, candidate readiness and actual test cost. Slots are finite time allocations, not a promise of simultaneous hardware access. Never borrow from correctness, cleanup or the user's total budget to fund a company.

Predeclare how scarce successor funding is awarded: default to strongest evidence of a different viable thesis, then feasibility of its delivery gate within one funded quarter, then expected product gain per test cost. Record the comparison together; break remaining ties by stable company ID, not submission or settlement order. Any successor still has to pass the plan-admission gate.

Require runway greater than zero and an actionable status before normal dispatch. Pivot/restructuring/probation rules override weights. Protected retries receive their denied opportunity before discretionary repeats. Unused time returns to the common pool. Document allocations and actual opportunity delivered; do not merely report financial penalties while assigning everyone the same work again.

Runway controls eligibility rather than converting directly to wall time. Any positive balance, including a final fractional balance, permits one bounded funded opportunity under the allocation rules above. Every completed nonblocked opportunity incurs the same one-unit burn; no additional real budget follows from a fractional balance.

## Settlement record and checks

Store policy/effective quarter, company and strategy epoch, pre/post price and runway, outcome, burn/grant, both streaks, status, contribution or hypothesis ID, receipts, next allocation and required action. Keep program reserve debits and funded successors in the same ledger. Existing Markdown plus JSON is enough; no exchange simulator is needed.

Use one settlement key per market/company/quarter, with the frozen policy version and a completed marker. Record the before/after balances and all effects together before carrying out the next dispatch. On resume, reuse the completed record: never repeat a burn, decay, grant, streak increment, haircut or reserve debit. If interrupted before completion, reconcile from the recorded starting balances and event IDs, not partially updated balances. Corrections append a superseding record and transparently recompute dependent balances; they are not another operating quarter.

Check these scenarios when adapting the policy:

- From $100/runway 3, two stagnant quarters yield $80/2 then $64/1 and a mandatory pivot. A third funded nondelivery reaches restructuring and receives its haircut once.
- Two distinct learning quarters yield $95/2.5 then $90.25/2. A third learning quarter still reaches the delivery-drought restructuring gate: useful evidence does not buy permanent immunity.
- A new qualified 1.10x delivery from $100/runway 3 yields $110/3 and resets both streaks. Receiving that code from a rival earns none of those rewards.
- A denied shared-queue opportunity changes neither price, runway nor streaks and gets a protected retry. Repeated shared failures require a program repair, not five company penalties.
- Resuming settlement or adopting a rival's code cannot apply the same grant, contribution gain or restructuring haircut twice. A missed probation cannot silently restart with fresh capital.
