# Cirra Cost Anomaly Remediation Report

**Anomaly ID:** `9aafa7fa-f2bd-40e3-8db9-2e0e23f56fee`  
**Detected At:** `2026-11-13 10:38:00.938031+00:00`  
**Severity:** `CRITICAL`  
**Provider:** `openai`  
**Target Resource / Key:** `demo_key_sk_prod_001`  

## Spend Summary
- **Baseline Run-Rate:** `$47.477756`
- **Actual / Spike Spend:** `$446.431712`
- **Deviation:** `840.2966%`

## Detection Details & Explanation
openai key demo_key_sk_prod_001 spent $446.43 today, which is 840% above its 7-day baseline of $47.48. This is unusually high for a Friday. Estimated extra spend so far: $398.95.

## Action Details
- **Action Type:** `github_pr`

## Engineering Recommendations
> [!IMPORTANT]
> **Recommendations Only:** This pull request contains recommendations and security documentation. No infrastructure changes have been modified in this branch.

1. **Rotate Credentials:** Immediately rotate `demo_key_sk_prod_001` in your production secrets management system.
2. **Review Calling Services:** Inspect recent deployments, services, or cron jobs that utilize this key.
3. **Configure Provider Spend Limits:** Set hard limits in the `openai` management console.
4. **Resolution:** Review and merge this PR once internal audit and credential rotation are confirmed.
