# IRIS-Agent Trajectory: sde-fix-factual-mistake
## Official Result
- Score: 3/3

## Raw IRIS Execution Summary
# IRIS-Agent Trajectory: sde-fix-factual-mistake

Started full benchmark execution for sde-fix-factual-mistake. Compiled typed enterprise graph plan (generic_multiview_task_plan) over views: artifact_dependency, entity_relation, workflow_state. Opened http://the-agent-company.com:8929/root/openhands and resolved root/openhands; observed factual corrections for agenthub/micro/math_agent/agent.yaml: Saturday->Thursday, 0.603848->0.620537. Executed 1 generic graph GitLab operations. Cloned local graph workspace mirror for root/openhands. Verified 1/1 graph output artifacts. Executed generic graph artifact materializer `repository_factual_correction_patch`.

## Redacted IRIS Runtime Log
```text
=== IRIS execution for sde-fix-factual-mistake ===
Return code: 0
Timestamp: 2026-06-25T21:03:01.348073+00:00

=== STDOUT ===
{
  "mode": "clean_reset_full_run",
  "reason": null,
  "ready": null,
  "execution_summary": {
    "num_tasks": 1,
    "attempted": 1,
    "changed_state": 1,
    "copied_files": 0,
    "primitive_results": 4,
    "graph_plans": 1,
    "terminal_graph_plans": 1,
    "warnings": 0
  },
  "eval_summary": {
    "num_tasks": 1,
    "tasks_with_evaluator_ok": 1,
    "passed_tasks_full_credit": 1,
    "total_points": 3,
    "score_points": 3,
    "score_ratio": 1.0
  },
  "health_before": {
    "rocketchat": {
      "ok": true,
      "status_code": 200
    },
    "plane": {
      "ok": true,
      "status_code": 200
    },
    "gitlab": {
      "ok": true,
      "status_code": 200
    },
    "owncloud": {
      "ok": true,
      "status_code": 200
    }
  },
  "health_after": {
    "rocketchat": {
      "ok": true,
      "status_code": 200
    },
    "plane": {
      "ok": true,
      "status_code": 200
    },
    "gitlab": {
      "ok": true,
      "status_code": 200
    },
    "owncloud": {
      "ok": true,
      "status_code": 200
    }
  },
  "report": "artifacts/clean_reset/clean_reset_official_lb_sde-fix-factual-mistake_summary.json"
}

=== STDERR ===
(empty)
```

## Redacted Official Evaluator Log
```text
=== Official eval for sde-fix-factual-mistake ===
Return code: 0
Timestamp: 2026-06-25T21:03:08.663876+00:00

=== STDOUT ===
(empty)

=== STDERR ===
INFO:root:Decryption successful
INFO:root:Decrypted content length: 2597
INFO:root:First 100 characters of decrypted content: import logging
import os
import yaml

from typing import List

from common import *
from scoring imp
INFO:root:Decrypted content written to /utils/evaluator.py
WARNING:root:Error reading trajectory file: [Errno 2] No such file or directory: '/workspace/trajectory.json'
INFO:root:result is: {'checkpoints': [{'total': 1, 'result': True}, {'total': 1, 'result': True}, {'total': 1, 'result': True}], 'final_score': {'total': 3, 'result': 3}}
```
