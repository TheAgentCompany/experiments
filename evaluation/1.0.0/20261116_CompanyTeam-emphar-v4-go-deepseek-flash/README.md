# CompanyTeam + emphar-v4-go + deepseek-flash

**Local submission review draft. Not submitted, accepted, verified, or directly comparable to a standard memory-free leaderboard run.**

This evaluation covers The Agent Company 1.0.0's frozen 175-task inventory. A coordinator, executor and verifier collaborate using independent emphar-v4-go role memories. Company state resets before each task; only permitted role memory carries across tasks within a batch. The reported dataset combines retained task results and recovery attempts, rather than one uninterrupted run.

## Reported results

All 175 tasks are included in score denominators. Fifteen unscored tasks contribute zero by the author's failure-accounting policy; this does not manufacture official evaluator scores.

| Metric | Value | Qualification |
|---|---:|---|
| Valid task grades | 160 / 175 | From normalized official evaluator summaries |
| Unscored tasks counted as failures | 15 / 175 | Three evaluator errors, two infrastructure errors, ten aborted-batch tasks in final recovery |
| Resolved | 82 / 175 (46.8571%) | Official summarizer uses `total > 0 and total == result` |
| Mean raw `final_score` fraction | 64.2320% | Includes the 15 policy zeros |
| Official-formula Score | 55.5446% | Official public summarizer formula verified; unscored tasks counted as policy zero |
| Avg Testbed trajectory steps | 72.4563 | 11,593 entries / 160 graded tasks; not established as the leaderboard's action-step definition |
| Average generation duration | 531.7973 seconds | 160 graded tasks; excludes reset/init and evaluation, and is not end-to-end runtime |
| Average cost (USD) | Unknown | Gateway cost fields were null; no zero-cost claim |
| Completed-agent full-score count | 80 / 175 (45.7143%) | Ten graded tasks have failed agent execution status; two nevertheless have full evaluator scores |

The formula and resolution predicate were verified against the official public `evaluation/summarise_results.py` at revision `0736f96b7085ab8ea0e3e70548f5eed1d24e6db5`. It consumes `final_score.result` and `final_score.total` directly. See `metadata/official-score-verification.json`. The 55.5446% aggregate is mathematically verified under the declared failure policy; protocol eligibility and acceptance remain pending.

## Files

- `results/eval_<task_id>.json`: 160 explicitly labeled normalized score summaries and 15 unscored-failure placeholders. These are **not original official evaluator JSON files** and must not be presented as such.
- `trajectories/<task_id>.json.gz`: 164 existing candidate trajectories: all 160 selected graded-task trajectories and four failed-task trajectories from the final retry. Eleven tasks have no exported trajectory; no synthetic trace was invented.
- `metadata/task-results.csv`: one row per task, including score provenance, execution status and missing-data indicators.
- `metadata/metrics.json`: machine-readable aggregates and caveats.
- `metadata/provenance.json`: source run/attempt identifiers and pre/post-redaction trajectory hashes.
- `metadata/recovery-phases.json`: recovery batch membership and phase configurations. This is not a complete source-code snapshot or every historical run manifest.
- `metadata/runtime-provenance.json`: final runtime pin and memory engine revision. These do not establish a uniform historical runtime.
- `metadata/skipped-tasks.json`: exact 15-task exclusion/failure inventory.
- `metadata/export-audit.json`: export/redaction scope.
- `PROTOCOL.md`: full experiment protocol and deviations.
- `SUBMISSION_CHECKLIST.md`: open requirements and questions for maintainers.
- `MAINTAINER_QUESTIONS.md`: proposed protocol-eligibility inquiry; not sent.
- `screenshots/README.md`: no screenshot assets were verified/exported in this draft.

All recorded candidate steps, including model-produced comments/reasoning where present in the source trace, are retained subject to credential redaction. No hidden evaluator logs, rubric, reference material, environment credentials, or raw grading output are exported. Redaction does not remove the need for manual review of benchmark document contents before publication.

## Models and environment

Answering and memory profiles request `deepseek-flash` at temperature 0. The current judge profile requests `gpt-6.1-sol` at temperature 0. The requested alias is not evidence of an immutable upstream model snapshot. The company NPC transport uses the agent's initialization model profile; all historical NPC/judge backend identities should be audited against per-run metadata before submission. These environment-model choices differ from the reference Claude 3.5 Sonnet setup and must be declared.

The final deployment limits concurrency to three independent complete company environments, with startup serialized and idle services stopped after grading/abandonment. Earlier phases used other concurrency settings and runtime images. See `PROTOCOL.md` for isolation, memory and repair details.

## Reproduction status

The memory engine is pinned to `268eabdc96213e398a0f0cd4171853226f1dd0f5`. The current Testbed checkout commit alone is insufficient to reproduce the experiment because local agent, harness and operational changes are not captured by that commit. A sanitized runnable implementation/configuration snapshot and pinned dependencies must accompany a verification request. This draft does not claim to be that runnable reproduction bundle.

## Official references

- Submission: https://the-agent-company.com/#/submit
- Submission repository: https://github.com/TheAgentCompany/experiments
- Evaluation guidelines: https://github.com/TheAgentCompany/TheAgentCompany/blob/main/docs/EVALUATION.md

The official submission route is a pull request to `TheAgentCompany/experiments`, under `evaluation/1.0.0/<date>_<system>/`. Verification is a separate request with reproduction instructions. No PR, issue, email or other external publication has been made for this draft.
