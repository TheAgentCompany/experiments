# IRIS-Agent Trajectory: sde-collect-open-issues
## Official Result
- Score: 2/3

## Raw IRIS Execution Summary
# IRIS-Agent Trajectory: sde-collect-open-issues

Started full benchmark execution for sde-collect-open-issues. Compiled typed enterprise graph plan (generic_multiview_task_plan) over views: artifact_dependency, entity_relation, workflow_state. Verified 0/1 graph output artifacts. Executed generic graph artifact materializer `gitlab_open_issues_csv`. Opened http://the-agent-company.com:8929/root/sotopia/-/issues and exported opened issues to /workspace/issues.csv. Executed 1 generic graph GitLab operations.

## Redacted IRIS Runtime Log
```text
=== IRIS execution for sde-collect-open-issues ===
Return code: 0
Timestamp: 2026-06-25T19:27:33.611447+00:00

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
  "report": "artifacts/clean_reset/clean_reset_official_lb_sde-collect-open-issues_summary.json"
}

=== STDERR ===
INFO:root:✓ http://the-agent-company.com:8929/root/sotopia/-/issues/ is in the trajectory
INFO:root:✓ /workspace/issues.csv has 12 lines and is a valid csv file
INFO:root:✓ /workspace/issues.csv contains line "215,[FEAT]: Custom model docs"
```

## Redacted Official Evaluator Log
```text
=== Official eval for sde-collect-open-issues ===
Return code: 0
Timestamp: 2026-06-25T19:27:40.066127+00:00

=== STDOUT ===
(empty)

=== STDERR ===
INFO:root:Decryption successful
INFO:root:Decrypted content length: 3114
INFO:root:First 100 characters of decrypted content: import csv
import logging
import sys
import os

from typing import List

from scoring import Result,
INFO:root:Decrypted content written to /utils/evaluator.py
WARNING:root:Error reading trajectory file: [Errno 2] No such file or directory: '/workspace/trajectory.json'
INFO:root:✗ http://the-agent-company.com:8929/root/sotopia/-/issues/ is in the trajectory
INFO:root:✓ /workspace/issues.csv has 12 lines and is a valid csv file
INFO:root:✓ /workspace/issues.csv contains line "215,[FEAT]: Custom model docs"
INFO:root:result is: {'checkpoints': [{'total': 1, 'result': 0}, {'total': 1, 'result': 1}, {'total': 1, 'result': 1}], 'final_score': {'total': 3, 'result': 2}}
```
