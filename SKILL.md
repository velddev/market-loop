---
name: market-loop
description: Run five rival engineering subagents in separate Git worktrees, benchmark their submissions, allocate finite research runway, penalize stagnation, and share approved releases. Use for competition or market-style research loops and their stock, funding, pivot, or release decisions; not ordinary parallel coding or real financial research.
---

# Market Loop

Run rival companies toward the user's measurable product goal. Each aims to become and remain market leader. The parent is the benchmark operator, integration owner, investor and referee. Default to five companies with persistent identities and separate branches/worktrees. Competitors may change specialties or pursue complete alternative designs.

Make competition affect decisions: funding, scarce test slots, integration effort, mandatory pivots and retirement of unsuccessful approaches. Roleplay alone is not an incentive mechanism. Keep financial values fictional and technical measurements independently auditable.

## Establish a runnable market

Inspect the existing market, goal, company worktrees and pending experiments. Resume them rather than creating duplicates. Use subagents for companies, not user-owned app tasks unless requested. Preserve the user's correctness, resource, authorization and time boundaries.

Before dispatch, freeze:

- The primary product metric, workloads, correctness gate, resource limits, timing boundaries and qualification needed to claim a win.
- A common source/build reference and an actually runnable control. If admission or the evaluator fails, repair the shared evaluation setup first. Declare changed conditions prospectively; do not compare incompatible runs.
- A finite quarter budget: implementation time, shared hardware slots, screening cutoff and time reserved for integration and decisive tests. A quarter is a bounded work cycle, not elapsed calendar time.
- The roster, company states, technical scoring policy, financial policy version, effective quarter and restructuring reserve. Use [economics.md](references/economics.md) when initializing, migrating, allocating or settling a market.

Use one shared evaluator, admission policy and hardware queue. Extend it narrowly when a candidate needs something new. Companies should not rebuild the same benchmark infrastructure independently. If the control is unusable or all companies are waiting on the referee, record a program-level failure and fix that bottleneck; do not manufacture five company failures.

### Comparisons against a normal goal

When benchmarking this skill against a normal goal, the parent is strictly a referee. It may freeze the goal and evaluator, measure submissions, mechanically integrate qualified releases, settle the market, and report results. It must not write optimizations, suggest implementation strategies, repair competitors' solutions, or coach either arm.

Run the market and normal goal in completely separate project environments, with independent repositories, working directories, baseline copies, evaluator copies, and result stores. Give the normal goal a fresh agent context containing only the frozen goal, starting source, evaluation contract, and budget; never share market code, hypotheses, results, or conversation history with it. Keep company worktrees inside the market environment. Identical immutable starting inputs are the only intentional shared material. Document whether separation is filesystem/context isolation or an actual process/container boundary; do not claim a stronger boundary than exists.

Freeze the same correctness gates, workloads, resource limits, and stopping rule for both arms. Match the normal goal's wall-time allowance to the measured market optimization window, excluding shared setup and final reporting. Serialize hardware-sensitive measurements, record actual elapsed time and agent effort separately, retain every turn's market, and show per-turn KPI movement independently from financial valuations. Label time-based checkpoints as checkpoints rather than pretending they are conversational turns. Do not treat a time-matched multi-agent comparison as a compute-matched comparison.

Keep Markdown/JSON ledgers in the project under study. Store hypothesis IDs, raw receipts, company finances, decisions and release history there, not in this reusable skill. Keep documentation sufficient to reproduce decisions; repeated manifests and ceremonial reports are not progress.

## Dispatch competing theses

Start each company brief with its valuation rank, technical result and comparability status, runway, stagnation/delivery streaks, and required action. Include the four competitors' results, shared release and available budget. Where no technical leader has a comparable qualified result, say so; do not invent a performance gap from share prices.

Require each company to choose a thesis with:

1. The bottleneck and expected effect on the full product metric, with a simple cost or time budget. Account for overlap and Amdahl limits. Incremental improvements remain eligible; a large target should also attract designs capable of larger changes.
2. A cheap falsifiable test, a failure criterion, and the next decision that either outcome would change. Freeze a hypothesis ID and milestone before results.
3. An integration owner, dependencies, memory/traffic costs, and a route from component evidence to a complete contender. A promising component with no integration plan is unfinished work.
4. A bounded submission: changed source and identities, runnable checks, expected mechanism, proposed benchmark and what remains unmeasured. Freeze inputs while queued; preserve failed attempts in distinct versions.

Let companies diverge from their original lanes. A lagging company must explain how its next approach can improve its position after rivals' approved changes become shared. Renaming the same mechanism, repeating a disproven idea without a new cause, or inheriting another company's code earns no new evidence credit.

## Screen, integrate and decide

Parallelize source work; serialize tests that contend for CPU, GPU, RAM or disk. Worktrees do not isolate hardware. The parent owns the shared queue and checks admission, output paths and cleanup. Company allocation never expands the user's actual time, resource or spending budget.

Give each funded company a feasible screening opportunity, then allocate remaining effort by evidence and current financial status. Default to reserving at least half the available quarter time for integration and decisive comparisons; adapt this before the quarter to the task's costs. Protect correctness and cleanup time. Do not spend the entire quarter preparing packets or close early merely because everyone has a component report.

Use staged gates: source checks, bounded correctness/component test, integrated product evaluation. Reject a clearly losing component without wasting a full-model run. Promote promising candidates into the shared evaluator during the same quarter where feasible. If a finalist cannot complete the declared qualification within its allocation, disclose the missing gate and why; screening results cannot be priced as product wins.

Measure the user's actual outcome. For inference, count actual accepted outputs per elapsed time, including drafting, rejected work, verification, transfers and state updates. Separate prefill and first-token latency. Synthetic, teacher-forced and component rates are research evidence. Default qualification requires at least two representative workloads, each tested in reversed order with fresh processes where state persists. Predeclare a different appropriate qualification when the task warrants it.

Preserve exactness or the user's agreed quality contract. Different exact speculative algorithms may visit different rejected branches: compare the same inputs and actual histories against the reference. Do not demand identical proposal schedules across different algorithms or weaken target validation to obtain speed. Changed semantics require a separately authorized comparison.

Judge full costs and variability. A small gain is useful if verified. A noisy observation, incomplete answer or component-only saving is not a qualified delivery. Multiple component gains require combined correctness and performance checks; they do not automatically add or multiply.

### Synthesize all research into the next turn

Each turn has two shared outputs: a cumulative research record and a validated runtime baseline. Preserve and distribute every company's hypotheses, source, tests, positive and negative results, tradeoffs, uncertainty, and unfinished work. Research remains available regardless of rank, funding, retirement, or runtime adoption. Before choosing its next hypothesis, each company must account for relevant shared findings and explain what its proposed experiment adds or which changed assumption justifies revisiting an earlier result.

Do not implement a top-1 or fixed top-K promotion rule. After screening, have the companies assess all submissions for overlap, compatibility, dependencies, and useful combinations. The companies choose and implement integration plans; in a comparison against a normal goal, the parent only administers this gate and evaluates the resulting candidates. Do not discard a compatible contribution simply because another company's standalone candidate is faster.

Combine compatible improvements and validate the complete release against the matched shared control. Evaluate competing replacements as alternatives, and retain the evidence from every alternative. A positive standalone result does not guarantee a positive combined result. Record each submission's disposition: adopted, incorporated in a combination, overlapping alternative, failed combined validation, research-only, or awaiting a named gate. If integration cannot finish within the reserved budget, preserve its plan and identify the missing gate rather than silently dropping it or claiming a combined gain.

Advance the runtime baseline only with a qualified complete release. Advance the shared research record every turn, including no-delivery turns. Credit original contributions once using matched evidence; do not award every contributor the whole combined gain or assume component gains add or multiply. Preserve joint attribution with unresolved marginal credit when the evidence cannot isolate individual effects.

## Settle consequences

Apply the predeclared [economic rules](references/economics.md) after the parent reviews evidence. Classify each company as delivery, decision-quality learning, stagnant, or opportunity-blocked. Record the supporting hypothesis/gate and receipts. Keep technical scores, fictional valuations and research runway in separate fields.

Qualifying negative evidence can earn limited runway, but it cannot reset the delivery drought. Two consecutive stagnant quarters require a substantial pivot. Three funded quarters without delivery, or exhausted runway, require restructuring of the approach. These are dispatch gates, not suggestions to append to a press release. Preserve company history, experiments and previously earned credit when replacing an approach.

The next allocation must reflect settlement. A required pivot gets only a new-thesis screen until accepted; a retired approach gets no further slots. If all companies stagnate, the parent must change the shared bottleneck, allocation or evaluation process before repeating the cycle. Falling fictional prices alone do not fix an ineffective program.

## Release and distribute

Every company must have an honest disposition at the quarter boundary: validated, rejected, inconclusive, opportunity-blocked, or unfinished. A source-only submission is not a completed benchmark. A quarter with no qualifying delivery is recorded as **no delivery**, even if it publishes valuable research. There is no guaranteed winner and no permission to invent one.

Close the cycle in this order:

1. Commit completed experimental source and evidence, including unsuccessful attempts. Preserve unfinished work separately; exclude model weights, binaries, secrets and unrelated user changes.
2. Complete the all-submission synthesis gate and merge the compatible improvements that pass combined runtime checks. Preserve evaluated alternatives and unresolved integration plans with explicit dispositions. The parent owns getting submissions to this decision, subject to the no-assistance boundary above. A no-delivery release shares research without promoting an unqualified candidate.
3. Record outcomes, technical results, before/after valuations, runway burn/grants, streaks, required pivots, next allocations and policy/reference identities. Publish only to an already authorized destination.
4. Rebase company branches onto the approved common release, preserving private research. Remove rejected patches from the active runtime only after preserving them in an experimental commit or packet. Verify selected source and required build identities, not merely Git ancestry. Do not force-push shared branches without existing authorization.
5. Publish one press note with stock updates and all competitor technical releases. Separate measured facts, financial assumptions, unresolved gates and hypotheses. Include what changed in the shared product and what each company must do differently.
6. Send each company its rank/status, runway and required action first, then the shared runtime, cumulative research from all companies, integration dispositions and next bounded mandate. Everyone inherits approved improvements and research, including negative and unfinished findings; only the original contribution earns credit.

Continue only within the user's active request and budget. Simulation credits do not authorize paid resources, external messages, deployment, extra quarters, goals or automations. At a deadline or cancellation, leave a clear queue and durable checkpoint. Completing a quarter or updating this skill does not complete the underlying product goal.
