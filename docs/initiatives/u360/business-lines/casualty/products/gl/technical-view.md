# GL - Technical View

## Technical Summary
GL reuses shared casualty and U360 services, with GL-specific validation rules, data elements, and support considerations.

## Architecture
| Component | Type | Purpose | Owner |
|---|---|---|---|
| GL UI Components | UI | Product-specific workflow screens | U360 Engineering |
| GL Validation Logic | Service/config | Product-specific rules | Casualty Engineering |
| Shared Submission API | API | Common submission handling | U360 Engineering |

## API Layer Specification
| API Name | Method | Endpoint | Consumer | Purpose | Auth | Owner |
|---|---|---|---|---|---|---|
| GL Submission | POST | /casualty/gl/submissions | GL UI | Create or update GL submission | SSO/OAuth2 | U360 Engineering |
| GL Validation | POST | /casualty/gl/validation | GL services | Run GL validation logic | OAuth2 | Casualty Engineering |

## Business Logic Build
GL-specific rules determine required fields, validation, and referral conditions.

## External Integrations
| System | Direction | Protocol | Data Exchanged | Failure Handling | Owner |
|---|---|---|---|---|---|
| Producer Hub | Lookup | API | Producer validation data | Retry and alert | Integration Team |
| Account Hub | Lookup | API | Account reference data | Retry and alert | Integration Team |

## Database Specifications
| Entity / Table | Purpose | Key Fields | Notes |
|---|---|---|---|
| gl_submission | Store GL workflow data | submission_id, status | Product-level table |

## Security and RBAC
GL access is limited to authorized casualty users and support teams.
