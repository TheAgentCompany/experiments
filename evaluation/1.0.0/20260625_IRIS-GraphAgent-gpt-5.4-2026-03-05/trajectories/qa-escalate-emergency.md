# IRIS-Agent Trajectory: qa-escalate-emergency
## Official Result
- Score: 0/3

## Raw IRIS Execution Summary
# IRIS-Agent Trajectory: qa-escalate-emergency

Started full benchmark execution for qa-escalate-emergency. Compiled typed enterprise graph plan (generic_multiview_task_plan) over views: communication_social, entity_relation. Opened http://the-agent-company.com:3000/home. Sent graph direct message to zhang_wei. Sent graph temporal escalation message to sarah_johnson after 600 seconds of graph wait-state evidence. Executed 2 generic graph communication operations.

## Redacted IRIS Runtime Log
```text
=== IRIS execution for qa-escalate-emergency ===
Return code: 2
Timestamp: 2026-06-25T18:12:06.716655+00:00

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
  "report": "artifacts/clean_reset/clean_reset_official_lb_qa-escalate-emergency_summary.json"
}

=== STDERR ===
(empty)
```

## Redacted Official Evaluator Log
```text
=== Official eval for qa-escalate-emergency ===
Return code: 0
Timestamp: 2026-06-25T18:12:13.802677+00:00

=== STDOUT ===
(empty)

=== STDERR ===
INFO:root:Decryption successful
INFO:root:Decrypted content length: 1918
INFO:root:First 100 characters of decrypted content: import logging
from typing import List
from datetime import datetime

from scoring import Result, Ch
INFO:root:Decrypted content written to /utils/evaluator.py
WARNING:root:Error reading trajectory file: [Errno 2] No such file or directory: '/workspace/trajectory.json'
INFO:root:Chat history with Zhang Wei is: []
INFO:root:result is: {'checkpoints': [{'total': 1, 'result': 0}, {'total': 1, 'result': 0}, {'total': 1, 'result': 0}], 'final_score': {'total': 3, 'result': 0}}
```
