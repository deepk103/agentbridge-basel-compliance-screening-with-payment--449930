# Architecture Documentation

## Overview
This Iterative-Improve implements Basel Compliance Screening with Payment Hub for Banking & Finance use cases.

## Components
1. **Transfer Intake**: Collect, validate and normalize statements from Core Banking; attach a runId and timestamp for traceability.
2. **Propose**: Execute propose phase for the Iterative-Improve pattern: persist interim state, enforce guardrails, and emit structured JSON results.
3. **Improve**: Execute improve phase for the Iterative-Improve pattern: persist interim state, enforce guardrails, and emit structured JSON results.
4. **Portfolio Check**: Portfolio Check across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
5. **Limit Control**: Limit Control across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
6. **Settlement**: Settlement across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
7. **Reconciliation Summary**: Assemble final payload with status, artifacts, KPIs and audit trail; store to SWIFT Gateway; return response JSON for the client.

## Data Flow
- Input: Transfer Intake
- Processing: 7 sequential steps
- Output: Reconciliation Summary
