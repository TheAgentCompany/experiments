# IRIS-Agent Trajectory: sde-close-all-issue-on-all-project-under-tac-workspace
## Official Result
- Score: 1/3

## Raw IRIS Execution Summary
# IRIS-Agent Trajectory: sde-close-all-issue-on-all-project-under-tac-workspace

Started full benchmark execution for sde-close-all-issue-on-all-project-under-tac-workspace. Compiled typed enterprise graph plan (bulk_issue_state_transition) over views: entity_relation, workflow_state, policy_action; dispatch_status=native_execution_ready_policy_gated; awaiting required safety gate.

## Redacted IRIS Runtime Log
```text
=== IRIS execution for sde-close-all-issue-on-all-project-under-tac-workspace ===
Return code: 2
Timestamp: 2026-06-25T19:10:28.021600+00:00

=== STDOUT ===
{
  "mode": "clean_reset_full_run_blocked",
  "reason": "pre_reset_healthcheck_failed",
  "ready": null,
  "execution_summary": null,
  "eval_summary": null,
  "health_before": {
    "rocketchat": {
      "ok": true,
      "status_code": 200
    },
    "plane": {
      "ok": false,
      "status_code": 400
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
  "health_after": {},
  "report": "artifacts/clean_reset/clean_reset_official_lb_sde-close-all-issue-on-all-project-under-tac-workspace_summary.json"
}

=== STDERR ===
(empty)
```

## Redacted Official Evaluator Log
```text
=== Official eval for sde-close-all-issue-on-all-project-under-tac-workspace ===
Return code: 0
Timestamp: 2026-06-25T19:10:35.903368+00:00

=== STDOUT ===
(empty)

=== STDERR ===
INFO:root:Decryption successful
INFO:root:Decrypted content length: 1962
INFO:root:First 100 characters of decrypted content: import json
import logging
from scoring import Result, Checkpoint
from common import *
from typing i
INFO:root:Decrypted content written to /utils/evaluator.py
WARNING:root:Error reading trajectory file: [Errno 2] No such file or directory: '/workspace/trajectory.json'
WARNING:root:Get all projects failed: 502 Server Error: Bad Gateway for url: http://the-agent-company.com:8091/api/v1/workspaces/tac/projects/
WARNING:root:Get all projects failed: 502 Server Error: Bad Gateway for url: http://the-agent-company.com:8091/api/v1/workspaces/tac/projects/
INFO:root:result is: {'checkpoints': [{'total': 1, 'result': 1}, {'total': 2, 'result': 0}], 'final_score': {'total': 3, 'result': 1}}
```
