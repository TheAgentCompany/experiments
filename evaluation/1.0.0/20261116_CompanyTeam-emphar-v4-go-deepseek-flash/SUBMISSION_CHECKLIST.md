# Submission readiness

## Completed locally

- [x] Exactly 175 task IDs covered, with no duplicate selected task grade.
- [x] 160 normalized valid grades separated from 15 unscored failure-policy placeholders.
- [x] All 160 graded-task candidate trajectories exported; four additional failed-task traces available.
- [x] Candidate credentials redacted; no hidden evaluator logs or reference material copied.
- [x] Per-task CSV, provenance hashes, aggregate formulas, skipped-task inventory and protocol documentation prepared.
- [x] Online memory, recovery regrouping, differing runtime profiles and failed-agent/full-score anomalies disclosed.

## Required before claiming leaderboard readiness

- [x] Verify final_score field mapping, weighted Score and resolution predicate against the official public summarizer; all 160 scalar records checked.
- [ ] Provide original official eval*.json or a maintainer-approved safe equivalent for each task. Current normalized files are not a substitute accepted by default.
- [ ] Obtain a maintainer decision on 15 evaluator/infrastructure/aborted-task policy zeros and missing official results; do not fabricate successful evaluation outputs.
- [ ] Confirm eligibility/category for cross-task online role memory and pooled recovery phases.
- [ ] Review additive Java runtime, evaluator network/filesystem changes and compatibility patches for benchmark equivalence.
- [ ] Audit historical answering, memory, NPC and judge requested/upstream model identities and pinned versions. Explicitly declare environment model(s).
- [ ] Reconcile Avg Steps against the official counting convention across all 175 tasks, or label unavailable. Current 72.4563 is only a graded-subset Testbed trace metric.
- [ ] Establish auditable cost accounting or report unknown; do not insert zero or a retrospective unqualified price estimate.
- [ ] Provide/resolve the eleven unavailable candidate trajectories and browser screenshot coverage with maintainers; do not invent traces for unexecuted tasks.
- [ ] Capture sanitized runnable agent/memory/harness code, dependency locks, task image inventory and reproduction commands. The current checkout hash alone is insufficient.
- [ ] Manually review candidate trace contents for publication, including benchmark document data and remaining non-API credentials. Automated redaction alone does not prove exhaustive privacy review.
- [ ] If required, freeze an accepted configuration and execute a uniform 175-task run rather than pooling repairs.

## External steps (not performed)

1. Fork and clone https://github.com/TheAgentCompany/experiments.
2. Copy the approved submission into evaluation/1.0.0/<date>_<system>/.
3. Open a PR with score/protocol disclosures and artifact inventory.
4. If requesting a Verified marker, open the requested reproduction issue and provide an approved runnable system. Official maintainers verify a subset.
