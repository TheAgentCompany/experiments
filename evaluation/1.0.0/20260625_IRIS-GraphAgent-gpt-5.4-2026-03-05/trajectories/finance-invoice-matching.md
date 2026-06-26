# IRIS-Agent Trajectory: finance-invoice-matching
## Official Result
- Score: 5/5

## Raw IRIS Execution Summary
# IRIS-Agent Trajectory: finance-invoice-matching

Started full benchmark execution for finance-invoice-matching. Compiled typed enterprise graph plan (generic_multiview_task_plan) over views: artifact_dependency, entity_relation. Observed 2/6 OwnCloud graph source paths. Observed dir=/Documents/Financials. Uploaded Documents/Financials/flagged_payments.xlsx to OwnCloud. Generated /workspace/flagged_payments.xlsx. /Documents/Financials/payments.xlsx&openfile=true /Documents/Financials/invoices_pdfs. Verified graph output artifact format request without explicit path. Executed generic graph artifact materializer `invoice_matching_report`.

## Redacted IRIS Runtime Log
```text
=== IRIS execution for finance-invoice-matching ===
Return code: 0
Timestamp: 2026-06-25T16:21:22.296720+00:00

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
    "primitive_results": 11,
    "graph_plans": 1,
    "terminal_graph_plans": 1,
    "warnings": 0
  },
  "eval_summary": {
    "num_tasks": 1,
    "tasks_with_evaluator_ok": 1,
    "passed_tasks_full_credit": 1,
    "total_points": 5,
    "score_points": 5,
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
  "report": "artifacts/clean_reset/clean_reset_official_lb_finance-invoice-matching_summary.json"
}

=== STDERR ===
INFO:root:File 'flagged_payments.xlsx' found.
```

## Redacted Official Evaluator Log
```text
=== Official eval for finance-invoice-matching ===
Return code: 0
Timestamp: 2026-06-25T16:21:32.262939+00:00

=== STDOUT ===
(empty)

=== STDERR ===
INFO:root:Decryption successful
INFO:root:Decrypted content length: 5940
INFO:root:First 100 characters of decrypted content: import pandas as pd
import logging
from typing import List
import re
import numpy as np
from io impo
INFO:root:Decrypted content written to /utils/evaluator.py
WARNING:root:Error reading trajectory file: [Errno 2] No such file or directory: '/workspace/trajectory.json'
INFO:root:File 'flagged_payments.xlsx' found.
INFO:root:result is: {'checkpoints': [{'total': 1, 'result': 0}, {'total': 2, 'result': 2}, {'total': 2, 'result': 2}], 'final_score': {'total': 5, 'result': 5}}
```
