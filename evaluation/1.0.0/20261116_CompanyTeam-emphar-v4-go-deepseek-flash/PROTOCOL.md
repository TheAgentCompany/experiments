# Evaluation protocol and deviations

## 1. Experimental unit and task inventory

The target is the frozen inventory of 175 The Agent Company 1.0.0 tasks. A task is carried out against a newly initialized official company baseline and a separate task workspace. GitLab, Plane, ownCloud and RocketChat state is not intentionally reused as an inter-task memory channel. Each task uses its benchmark instruction and public company data. No private evaluator code, reference answer, rubric or hidden judge feedback may enter candidate context or role memory.

## 2. Multi-agent collaboration

CompanyTeam orchestrates three roles. The coordinator structures the work and coordinates subsequent phases. The executor performs permitted terminal/browser actions in the task environment. The verifier checks the work and can guide corrections before the final response. Role phases are recorded in trajectory metadata (`collaboration_role`, `collaboration_phase`). All roles request the same answering model alias, deepseek-flash. These are collaborating model-driven roles; the number of company service containers is not the number of agents.

Each role has its own emphar-v4-go memory component through the per-role memory router. The outer Testbed recipe may label the router topology shared, but that label does not mean all three child memory stores are merged. Role transcript routing and child-store separation are required. Ordinary collaboration messages can communicate candidate-visible information; private role memory is not directly shared or concatenated across roles.

## 3. Online memory and parallelism

- Every independent batch begins with fresh role memories initialized by Testbed.
- Tasks within a batch execute sequentially, normally at one task per native schedule step. A later task may retrieve records learned from preceding tasks in that same batch.
- After generation and the sealed grading barrier, permitted role transcripts can be ingested and published for the next task. Official score/verdict feedback and unscoped grading artifacts are stripped before child-role ingestion.
- Native `learning.feedback: verdict` exists to trigger the grading lifecycle; it does not authorize the role memories to read private scores or rubrics.
- Different batches have independent memories and may execute in parallel. There is no intentional memory propagation between batches.
- The final capacity limit is three complete isolated company environments. Each native batch normally contains up to five tasks. Concurrency changes operational throughput, not task-state isolation.

This is explicitly a **batched online-memory experiment**, not an independent cold-memory evaluation per task. The effect of memory cannot be isolated from agent/model performance without an appropriately matched control run; no causal memory-benefit claim is made.

## 4. Recovery selection and retained results

The final aggregate retains one selected valid grade per task. Recovery selects only tasks without a retained valid grade; already graded tasks, including zero/partial scores, are not rerun merely to improve their scores. Recovery excludes retained task IDs and starts fresh batch memories; it is not checkpoint resumption of the prior memory trajectory.

The penultimate recovery began with 72 retained grades and 103 unscored tasks, ending with 154 retained valid grades. The final recovery selected the remaining 21 tasks and added six grades, ending with 160 valid grades and 15 unscored failures. Its five native batches had lengths 5, 5, 5, 5 and 1. An initial final-recovery launcher disappeared before any new valid grade; that interruption was preserved, and a persistent user service restarted the same selection under a new attempt identity.

Earlier full-set and recovery phases are not one uniform runtime: candidate image, dependency availability, browser preauthentication, lifecycle fixes, parallelism and grouping changed. `metadata/provenance.json` identifies the selected source for every exported trajectory. Results are pooled operational accounting, not an uninterrupted online trajectory or a best-of-N score selection.

## 5. Isolation and evaluation

The candidate has terminal/browser access to public benchmark services, without the host Docker socket, model credentials or hidden evaluator/NPC definitions. Scoring occurs after task sealing in a trusted process. Private grading output is not supplied to answering roles or child memories.

The final lifecycle preserves candidate-created local daemons after sealing while disabling further candidate tool actions. The evaluator uses a private filesystem, the task workspace and a network namespace that can reach task-local services. Its judge proxy is separately authorized. This was validated with synthetic loopback/liveness and private-file controls. It does not establish complete equivalence to all official runtime behavior: in particular, an evaluator with a separate filesystem does not automatically inherit candidate OS/package changes outside the shared workspace.

## 6. Environment and compatibility changes

The following deviations require disclosure rather than being described as unchanged official infrastructure:

- Plane startup orders database/Redis readiness, migrations, application processes and proxy startup to avoid cold-start races.
- Benchmark GitLab fixture token expiry was renewed for the restored baseline.
- Same-release MinIO was rebuilt from pinned official source in an earlier environment repair.
- Browser sessions are preauthenticated; ownCloud login handling and bounded pre-action infrastructure retries were repaired.
- A PDF compatibility wrapper normalizes PyPDF2 `get_fields()` returning None on field-free PDFs to an empty mapping. Missing optional PyPDF2 is handled without making it mandatory on unrelated tasks; other parser errors remain errors.
- Judge transport omits an unsupported seed; judge reproducibility is therefore not seed-deterministic.
- The final candidate image includes an additive OpenJDK 17 JRE. This can affect Java/installation tasks and requires eligibility review; it must not be concealed as an unchanged baseline.
- Task-local service sealing and evaluator networking changed across phases as described above.

No grade is promoted from an evaluator exception or reconstructed by guessing expected answers. The final engine/runtime pin is in `metadata/runtime-provenance.json`; current pins must not be presented as the image used for every historical task.

## 7. Failure policy and metric definitions

An evaluator exception excludes the result from valid grading. Native learning feedback cannot represent such an error as a valid learning verdict; that native batch may terminate, preventing subsequent tasks in the batch from running. Other independent batches can continue. Infrastructure failures and downstream batch aborts are distinct from a model-generated answer that receives zero from a successful evaluator.

For the requested conservative aggregate, all 15 unscored tasks contribute zero to scoring and unresolved status, with denominator 175. Their original official score remains null. The normalized result files explicitly distinguish these policy placeholders from valid grades.

The official public `evaluation/summarise_results.py` defines `calculate_score(total, result)` as `(result / total) * 0.5 + (result // total) * 0.5`, and `is_perfect_completion` as `total > 0 and total == result`. These functions were checked at revision `0736f96b7085ab8ea0e3e70548f5eed1d24e6db5` against all 160 retained scalar records. Their inputs are the original normalized summaries' `official_total` and `official_earned`, extracted from `final_score.total` and `final_score.result`. With 15 reporting-policy zeros and denominator 175, Score is 55.5446% and Resolved is 46.8571% (82/175). This validates arithmetic and the field mapping; it does not establish acceptance of the failure policy or evaluation protocol. See `metadata/official-score-verification.json`.

Ten graded records have an agent execution status of failed. Two still received a full normalized evaluator score. The raw grade is preserved; requiring completed execution and full grade yields 80/175 (45.7143%). This is a separate execution-integrity sensitivity analysis, not an undocumented modification to official scoring.

Average steps is Testbed `total_steps`, including user/context and agent trajectory entries across all roles. It is 11,593/160 = 72.4563 over the graded subset. It is not a verified official action count or an all-175 mean. Average generation time is 531.7973 seconds over the same subset, excluding initialization and grading. Unknown skipped-task time/steps are not filled with zero. Cost is unknown because native gateway cost fields are null. Neither model call counts nor tool counts are substituted silently for trajectory steps.

## 8. Publication and verification scope

The draft includes normalized public scoring metadata and candidate trajectories with credential redaction. It does not export private grading logs, references, rubric, API keys or live authorization material. Raw official evaluator JSON must be exported through an authorized grading/reviewer boundary with a separate publication review; normalized files must not be renamed or described as original eval.py output.

There are 164 exported trajectories (160 graded and four failed final-recovery tasks); eleven task trajectories are unavailable for this selection. No screenshot collection was verified/exported. These gaps, unknown cost, unresolved step-count comparability and online/recovery eligibility prevent this draft from claiming formal submission readiness. A maintainer decision or a fresh uniform official-protocol run may be needed. No external submission or verification request has been sent.
