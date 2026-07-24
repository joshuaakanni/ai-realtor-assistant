# Testing Guide

## Email validation
- Reject incomplete domains
- Reject spaces
- Reject multiple `@` symbols
- Accept a corrected address
- Confirm lowercase storage

## Tour requests
- Reject a past preferred date
- Accept a future preferred date
- Validate the requested timezone
- Calculate preferred UTC
- Accept or omit an alternative time
- Reject a partially supplied alternative date/time
- Confirm the assistant does not claim the tour is booked

## Contact requests
- Accept phone-only submissions
- Accept email-only submissions
- Reject requests with no usable contact detail
- Confirm preferred contact method matches supplied contact detail
- Verify callback timezone and UTC values

## Incentives
- Store available and unavailable information states
- Route follow-up requests correctly
- Avoid exposing internal data sources

## Data storage
- Confirm every mapped Google Sheets column receives the correct value
- Confirm request IDs are unique
- Confirm request statuses are correct
- Confirm timestamps use the configured timezone

## Conversation routing
- Confirm completed flows do not restart when the user says “No thanks”
- Confirm previously supplied information is reused
- Confirm internal tool names are not exposed
