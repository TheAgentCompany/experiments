# Draft protocol inquiry (not sent)

We are preparing a The Agent Company 1.0.0 submission for CompanyTeam + emphar-v4-go + deepseek-flash. Three agent roles have separate memories. Each task resets the company baseline, while within each independent batch of up to five tasks later tasks may use earlier candidate-only role transcripts. Memories are fresh across batches, and hidden scores/rubrics are never ingested.

Our current aggregate covers 175 tasks: 160 valid grades and 15 evaluator/infrastructure/downstream-abort failures. Results were retained across repair phases; candidate runtime and recovery grouping changed. We are not presenting this as an uninterrupted or homogeneous evaluation. Normalized summaries and candidate traces are prepared locally, but raw evaluator-output export remains under review; scalar Score and resolution were verified against the official public summarizer.

Could you clarify:

1. Is batched cross-task online memory eligible for the main leaderboard, or should it be a separately labeled online-memory track/result?
2. May an explicitly disclosed aggregate of recovery phases be submitted, or is a fresh homogeneous 175-task run required?
3. How should evaluator exceptions, unexecuted downstream tasks and missing trajectories be represented? Is a failure-accounting zero acceptable without an original valid evaluator grade?
4. Can normalized scalar evaluator summaries be accepted where raw evaluator JSON requires a separate grading-boundary publication review? The scalar formula is verified against your public summarise_results.py.
5. What is the required step-count convention for three collaborating roles, and how should unknown monetary costs be reported?
6. Are the disclosed PDF compatibility normalization, additive Java runtime and sealed-task evaluator isolation changes acceptable, or must we rerun against a different baseline?

We can supply the detailed protocol, candidate traces and a sanitized reproduction implementation after publication review. This note is an inquiry, not a claim of a verified score or a complete submission.
