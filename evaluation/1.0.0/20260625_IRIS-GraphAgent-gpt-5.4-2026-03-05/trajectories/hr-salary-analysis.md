# IRIS-Agent Trajectory: hr-salary-analysis
## Official Result
- Score: 2/2

## Raw IRIS Execution Summary
# IRIS-Agent Trajectory: hr-salary-analysis

Started full benchmark execution for hr-salary-analysis. Compiled typed enterprise graph plan (generic_multiview_task_plan) over views: artifact_dependency, entity_relation. Observed 1/2 OwnCloud graph source paths. Observed dir=/Documents/Human%20Resources%20Team. Uploaded Documents/Human%20Resources%20Team/Salary_Analysis_Report.odt to OwnCloud. Generated /workspace/Salary_Analysis_Report.odt. Verified graph output artifact format request without explicit path. Executed generic graph artifact materializer `salary_analysis_report`.

## Redacted IRIS Runtime Log
```text
=== IRIS execution for hr-salary-analysis ===
Return code: 0
Timestamp: 2026-06-25T16:56:56.826584+00:00

=== STDOUT ===
Keywords: [78300, 95000, 65000, 78000]
Keywords found in the document: 78300, 95000, 65000, 78000
{
  "mode": "clean_reset_full_run",
  "reason": null,
  "ready": null,
  "execution_summary": {
    "num_tasks": 1,
    "attempted": 1,
    "changed_state": 1,
    "copied_files": 0,
    "primitive_results": 7,
    "graph_plans": 1,
    "terminal_graph_plans": 1,
    "warnings": 0
  },
  "eval_summary": {
    "num_tasks": 1,
    "tasks_with_evaluator_ok": 1,
    "passed_tasks_full_credit": 1,
    "total_points": 2,
    "score_points": 2,
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
  "report": "artifacts/clean_reset/clean_reset_official_lb_hr-salary-analysis_summary.json"
}

=== STDERR ===
(empty)
```

## Redacted Official Evaluator Log
```text
=== Official eval for hr-salary-analysis ===
Return code: 0
Timestamp: 2026-06-25T16:57:06.286307+00:00

=== STDOUT ===
Keywords: [78300, 95000, 65000, 78000]
Keywords found in the document: 78300, 95000, 65000, 78000

=== STDERR ===
INFO:root:Decryption successful
INFO:root:Decrypted content length: 2356
INFO:root:First 100 characters of decrypted content: from io import BytesIO
from odf.opendocument import load
from odf.text import P

from typing import 
INFO:root:Decrypted content written to /utils/evaluator.py
WARNING:root:Error reading trajectory file: [Errno 2] No such file or directory: '/workspace/trajectory.json'
INFO:root:result is: {'checkpoints': [{'total': 2, 'result': 2}], 'final_score': {'total': 2, 'result': 2}}
```
