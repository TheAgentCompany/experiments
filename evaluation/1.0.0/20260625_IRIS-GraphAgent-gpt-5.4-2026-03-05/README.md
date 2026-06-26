# IRIS-Agent Submission

## Model
- **Agent**: IRIS-Agent (Graph-Native Planning and Verifiable Execution)
- **LLM Backbone**: GPT-5.4 (`gpt-5.4-2026-03-05`)
- **Architecture**: Graph-native enterprise agent with typed state graph, AMAC pruning, DLP certificates, and terminal GraphPlan execution

## Official Evaluation Result
- **Partial Score**: 451/776 (58.1%), counting all benchmark points including failed init/pull tasks as zero
- **Official evaluator observed denominator**: 451/750 (60.1%) over tasks whose evaluator returned checkpoint totals
- **Full Credit**: 81/175 (46.3%)
- **Evaluator**: Official TheAgentCompany encrypted `evaluator.py`, per-task Docker images, LLM judges via OpenAI-compatible endpoint

## Method Summary
IRIS-Agent represents the enterprise workplace as a layered typed state graph (EEAG), plans through task-induced subgraphs using Anchored Multi-frontier Convergence (AMAC), and executes typed GraphPlans whose preconditions, gates, effects, and provenance are auditable. Dual-Layer Proof (DLP) certificates verify both graph support and semantic alignment before execution.

## Key Features
- **Graph-native planning**: Tasks are compiled into typed GraphPlans over the enterprise state graph.
- **AMAC pruning**: Multi-anchor convergence reduces action-target space while preserving recall.
- **DLP certificates**: Dual-layer verification ensures graph support and semantic alignment.
- **Typed primitives**: Primitive types across GitLab, Plane, RocketChat, OwnCloud, and workspace operations.
- **No browser/UI interaction**: IRIS operates through typed API primitives rather than browser automation.

## Controlled Baselines (same GPT-5.4 backbone)
- Vanilla ReAct (8 steps): 262/776 (33.8%)
- Vanilla ReAct (25 steps): 349/776 (45.3%)
- ReAct + Entity Grounding: 308/776 (39.7%)


## Trajectory Format
Each file in `trajectories/` contains the raw IRIS execution summary plus redacted runtime and official evaluator logs for the same task. Redaction is limited to credentials and access tokens; task actions, scores, evaluator outputs, and error messages are otherwise preserved. The original unexpanded execution summaries are retained in `trajectories_raw/` for auditability.

## Screenshots
IRIS-Agent does not use browser automation or screenshot-based interaction during task execution. The `screenshots/` directory is included for submission completeness but is intentionally empty.
