---
name: market-loop
description: Run a competitive research loop where five subagents act as rival companies, develop in separate Git worktrees, submit benchmarked improvements, earn fictional stock prices, and inherit each approved shared release. Use when the user asks for this competition or market-style agent loop; ordinary parallel coding and real financial research are outside its scope.
---

# Market Loop

Run rival engineering companies toward the user's real objective. Their continuing objective is to become and remain market leader. The parent is the independent benchmark operator, integration reviewer, and market referee. Company identities and share prices make progress comparable; they never substitute for measured engineering results.

Default to five companies, each aware of its four competitors, with separate branches and worktrees and an initial fictional price of $100. Honor an existing roster, scoring contract, time budget, and release process. Keep company identities across rounds. They may pivot beyond their starting specialties.

## Establish the market

Inspect the repository and existing goal, agents, worktrees, studies, and outstanding tests before creating anything. Resume an existing market instead of duplicating it. Use subagents for companies, rather than creating user-owned app tasks unless requested. A skill invocation authorizes this research method within the user's task; it does not authorize unrelated deployment, external messages, paid resources, or changing the correctness contract.

Freeze a common base commit and benchmark contract before dispatch. Capture:

- The outcome, primary metric, workload, correctness checks, resource limits, and relevant product metrics.
- Baseline source and executable identities, measurement conditions, and known limitations.
- Company-to-agent, branch, and worktree mapping; current round, deadline or stopping condition, and hardware queue.
- The pricing formula and evidence needed to move a price. Preserve an existing formula; never change it after seeing results to favor a company.

Keep a compact durable ledger in the repository: rules, company state, submissions, raw benchmark receipts, release history, and press notes. Markdown plus JSON is sufficient; do not build a trading application or custom orchestration service to run the experiment.

## Company mandate

Tell every company its name, ticker, four rivals, price, shared base, assigned worktree, benchmark contract, and current standings. Give it a concrete first hypothesis while allowing later pivots. Instruct it to:

1. Choose an improvement capable of overtaking the leaders. A useful incremental gain is eligible even if it cannot reach the overall target alone.
2. Implement and check the smallest falsifiable candidate in its own worktree. Keep a short company log of thesis, evidence, rejected ideas, and next move.
3. Freeze a submission with changed paths and hashes, base commit, dependencies, runnable checks, benchmark command, expected mechanism, resource accounting, and success criteria. State what is still unmeasured.
4. Leave frozen inputs unchanged while queued. Put new experiments in separate versioned packets. Prepare source and lightweight checks while waiting; do not consume shared benchmark hardware without the referee's slot.
5. After results, write a short technical press release backed by receipts, study the rivals' releases, and choose a next move. Winning a round starts the work of defending leadership.

Competitive stakes are fictional ranking and earned performance credit. Failed experiments remain visible and motivate a pivot. Never reward fabricated gains, hidden costs, benchmark memorization, suppressed failures, or weaker correctness. Rivalry does not justify withholding an approved improvement from the next shared release.

## Benchmark and review

Parallelize independent implementation and analysis. Serialize measurements that contend for the same GPU, CPU, RAM, or storage through one parent-owned queue. Separate worktrees do not isolate hardware. Check resource admission and output paths before expensive work, and record cleanup before the next test.

Use staged gates: source checks, bounded correctness/component test, then realistic end-to-end trials for candidates that warrant them. Retain negative and failed receipts. A rejected component need not consume a full-model benchmark merely to complete the roster; mark its disposition explicitly.

Price the user's actual outcome. For inference this means accepted generated outputs per elapsed time, charging drafting, rejected branches, verification, transfers, and state updates. Report prefill and first-token latency separately when decode throughput is the pricing metric. Synthetic kernel rates, teacher-forced throughput, cache simulations, and theoretical ceilings are research evidence, not chat performance.

Run matched candidate/control measurements with multiple representative workloads, repeated in reversed order and fresh processes when state carries over. Record raw values, variability, useful work counts, correctness, memory and traffic, and timing boundaries. Keep conditions identical. Do not claim a noisy single observation is a validated win.

Preserve the agreed correctness contract. Exact speculative algorithms can visit different rejected branches: validate computations against the reference for the same inputs and actual branch histories, rather than demanding identical proposal schedules. Relaxed semantics require an explicitly authorized, separately scored experiment. Larger hardware budgets are a different comparison.

## Stock accounting

Shares are fictional engineering scores, not real securities or forecasts. Keep unvalidated prices unchanged and display the absence of a validated leader honestly.

If no pricing policy exists, use a $100 starting score and compound each company's independently validated, adopted gain: `new_price = previous_price * geometric_mean(candidate_rate / matched_control_rate)`. For a lower-is-better metric, invert the ratio. Require at least two representative workloads, each tested in reversed order, plus the agreed correctness gates. Publish each round's ratio separately from the cumulative score and actual performance.

Credit a contribution once. Receiving rivals' merged code gives everyone the same new technical starting point; it does not independently earn that gain again. Keep the prior valid score for a rejected or inconclusive submission. If evidence supporting a credited gain is invalidated, withdraw that credit and recompute from valid history. A cumulative score records earned contributions and must not be described as the company's current throughput ratio to another company.

Use the project's existing formula instead of these defaults when one is already agreed. In particular, do not silently switch an established baseline-relative price to cumulative scoring. Record the denominator's reference commit and whether it stays fixed or advances with releases. Label a carried-forward quote with the round and reference that earned it; settle the next round's reference policy before measuring that round.

## Close a cycle and distribute the release

Wait until every company has a benchmark disposition for its frozen submission: validated, rejected, inconclusive, or blocked with evidence. A source-only queue entry is not a completed benchmark. Carry a blocked or unfinished candidate forward explicitly; do not invent a result to close the round. Bound a round by its agreed time or work budget so new ideas cannot indefinitely move the finish line.

Then perform the shared release in this order:

1. Commit the completed submission evidence and experimental source. Preserve unsuccessful attempts; exclude model weights, binaries, secrets, and unrelated user changes.
2. Review and merge only approved runtime improvements. Resolve interactions and run meaningful combined correctness and performance checks; isolated gains do not automatically add or multiply. A cycle with no approved runtime change can still release valuable research evidence.
3. Record the release commit, approved and rejected changes, receipts, and stock calculations. Push to the already authorized destination when publishing was requested; a press note is otherwise a local artifact, not permission to send it externally.
4. Checkpoint each company's local work safely, rebase its branch onto the released common base, and resolve conflicts without deleting unfinished experiments. Remove rejected patches from the active runtime only after preserving them in an experimental commit or packet. Do not force-push shared branches without existing authorization.
5. Verify all five have the same approved runtime baseline, with private research changes clearly separated. Rebasing alone does not prove equality if an old candidate remains active. Update source manifests and required build identities for the new round; retain old frozen manifests with their original receipts.
6. Publish one press note with **stock updates** and **competitor technical releases**. Include prior/new price, measured gain, evidence status, what changed, what failed, what was merged, and the next research direction. Distinguish measured facts from company hypotheses and the overall target from current performance.
7. Send every company the shared release commit, standings, all five press releases, and its next bounded mandate. All receive the approved improvements and can build on their rivals' work in the next cycle.

## Continue and stop

Continue within the user's active goal and budget, treating corrections as steering. Do not create a persistent goal or scheduled automation unless requested. At a time limit, cancellation, resource block, or completion, leave a clean queue and durable checkpoint with pending work, branch states, and the next runnable experiment. Never mark the real objective achieved because a cycle, skill, or benchmark harness is complete.
