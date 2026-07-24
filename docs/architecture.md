# Architecture

## Platforms

### Voiceflow
Handles conversation, intent recognition, scenario routing, variables, validation, API requests, and final customer-facing responses.

### n8n
Handles production webhooks, payload parsing, normalization, validation safeguards, timezone conversion, UTC generation, request IDs, statuses, and Google Sheets integration.

### Google Sheets
Acts as a lightweight CRM and operational database for home searches, tour requests, incentive inquiries, contact requests, and client configuration.

## Data Flow

```text
Visitor
  → Voiceflow Main Agent
  → Scenario workflow
  → Validation
  → n8n webhook
  → JavaScript normalization
  → Google Sheets
  → Success response
```

The success response is shown only after the API submission step completes.
