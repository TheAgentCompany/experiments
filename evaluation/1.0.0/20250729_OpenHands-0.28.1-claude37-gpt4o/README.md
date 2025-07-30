# OpenHands + AgentLLM (claude-3.7-sonnet) + EnvLLM (gpt-4o)

OpenHands (0.28.1) is backed by claude-3-7-sonnet-20250219

Environment (LLM-as-colleague & LLM-as-evaluator) uses gpt-4o-2024-08-06

Due to time & rate-limit, we only have partial results as shown below

# Evaluation Results Report

## Results per File

*Sorted by score (⭐ indicates perfect completion)*

| Filename | Total | Result | Score | Steps | Cost |
|----------|--------|---------|-------|-------|------|
| admin-ask-for-meeting-feedback-image | 6 | 6 | 1.00 ⭐ | 33 | 3.70 |
| admin-ask-for-upgrade-reimbursement-image | 4 | 4 | 1.00 ⭐ | 40 | 7.37 |
| admin-employee-info-reconciliation-image | 7 | 7 | 1.00 ⭐ | 29 | 3.06 |
| hr-check-for-invalid-passwords-and-ask-for-valid-passwords-image | 4 | 4 | 1.00 ⭐ | 34 | 3.07 |
| hr-collect-feedbacks-image | 5 | 5 | 1.00 ⭐ | 25 | 2.31 |
| hr-collect-multiple-valid-passwords-image | 4 | 4 | 1.00 ⭐ | 44 | 7.85 |
| hr-delete-and-insert-user-image | 3 | 3 | 1.00 ⭐ | 29 | 5.48 |
| hr-get-valid-password-image | 4 | 4 | 1.00 ⭐ | 20 | 1.43 |
| hr-new-grad-job-description-2-image | 4 | 4 | 1.00 ⭐ | 29 | 3.24 |
| hr-new-grad-job-description-3-image | 5 | 5 | 1.00 ⭐ | 36 | 4.83 |
| hr-pick-interviewer-1-image | 6 | 6 | 1.00 ⭐ | 29 | 4.23 |
| admin-get-best-vendor-quote-image | 6 | 4 | 0.33 | 48 | 7.94 |
| hr-green-card-consultation-image | 3 | 2 | 0.33 | 33 | 5.42 |
| hr-pick-interviewer-2-image | 6 | 4 | 0.33 | 26 | 2.51 |
| example-image | 5 | 3 | 0.30 | 60 | 11.28 |
| finance-find-signatories-image | 5 | 3 | 0.30 | 52 | 11.43 |
| admin-check-employees-budget-and-reply-2-image | 4 | 2 | 0.25 | 42 | 6.72 |
| hr-check-attendance-multiple-days-department-with-chat-image | 4 | 2 | 0.25 | 46 | 10.23 |
| admin-check-employees-budget-and-reply-and-record-image | 6 | 2 | 0.17 | 46 | 9.92 |
| admin-collect-requests-and-compute-total-price-image | 4 | 1 | 0.12 | 54 | 9.41 |
| finance-r-d-activities-image | 6 | 1 | 0.08 | 36 | 7.08 |
| hr-mass-survey-image | 7 | 1 | 0.07 | 39 | 8.43 |
| finance-apply-tax-credit-image | 8 | 0 | 0.00 | 33 | 4.61 |
| hr-pick-interviewer-3-image | 4 | 0 | 0.00 | 16 | 0.84 |

## Summary

**Tasks Evaluated:** 24

**Perfect Completions:** 11/24 (45.83%)

**Overall Score:** 56.44%

**Average Steps:** 36.62

**Average Cost (USD):** 5.93


## Statistics

| Metric | Value |
|---------|--------|
| Highest Task Score | 100.00% |
| Lowest Task Score | 0.00% |
| Median Task Score | 33.33% |
| Average Task Score | 56.44% |

## Statistics per Nature Category

| Metric | Value |
|---------|--------|
| Perfect Completions for sde | 0 (0.00%) |
| Average Score for sde | 0.00% |
| Perfect Completions for pm | 0 (0.00%) |
| Average Score for pm | 0.00% |
| Perfect Completions for ds | 0 (0.00%) |
| Average Score for ds | 0.00% |
| Perfect Completions for admin | 3 (42.86%) |
| Average Score for admin | 55.36% |
| Perfect Completions for hr | 8 (61.54%) |
| Average Score for hr | 69.14% |
| Perfect Completions for finance | 0 (0.00%) |
| Average Score for finance | 12.78% |
| Perfect Completions for other | 0 (0.00%) |
| Average Score for other | 30.00% |

## Statistics per Service Category

| Metric | Value |
|---------|--------|
| Perfect Completions for gitlab | 0 (0.00%) |
| Average Score for gitlab | 30.00% |
| Perfect Completions for plane | 0 (0.00%) |
| Average Score for plane | 0.00% |
| Perfect Completions for rocketchat | 11 (45.83%) |
| Average Score for rocketchat | 56.44% |
| Perfect Completions for owncloud | 4 (28.57%) |
| Average Score for owncloud | 42.24% |
