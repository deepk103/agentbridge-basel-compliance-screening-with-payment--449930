# API Documentation

## Endpoints
### Transfer Intake
- **Description**: Collect, validate and normalize statements from Core Banking; attach a runId and timestamp for traceability.
- **Type**: Processing

### Propose
- **Description**: Execute propose phase for the Iterative-Improve pattern: persist interim state, enforce guardrails, and emit structured JSON results.
- **Type**: Processing

### Improve
- **Description**: Execute improve phase for the Iterative-Improve pattern: persist interim state, enforce guardrails, and emit structured JSON results.
- **Type**: Processing

### Portfolio Check
- **Description**: Portfolio Check across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Limit Control
- **Description**: Limit Control across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Settlement
- **Description**: Settlement across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Reconciliation Summary
- **Description**: Assemble final payload with status, artifacts, KPIs and audit trail; store to SWIFT Gateway; return response JSON for the client.
- **Type**: Processing
