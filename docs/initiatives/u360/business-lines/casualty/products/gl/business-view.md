# GL - Business View

## Purpose
GL is a casualty product capability within U360 that supports GL-specific underwriting workflow and controls.

## Business Objective
Provide GL-specific workflow, validations, and decision support while using shared U360 platform services.

## Targeted Users
| User Group | Role | Usage |
|---|---|---|
| GL Underwriters | Primary user | Review and progress GL submissions |
| Operations | Support user | Resolve exceptions and support workflow |

## Key Business Capabilities
- GL submission intake
- GL-specific review and validation
- referral and approval support
- activity visibility and traceability

## Workflow Summary
1. GL submission is created.
2. Producer and account data are validated.
3. Review and referral logic is applied.
4. Action and outcome are logged.

## Product-Specific Rules
| Rule | Description | Trigger | Outcome |
|---|---|---|---|
| GL Required Fields | Certain product attributes must be present before progression | Submission validation | Submission proceeds or exception created |

## Dependencies
| Dependency | Type | Purpose |
|---|---|---|
| Producer Hub | Shared capability | Producer validation |
| Account Hub | Shared capability | Account data |
| Audit Trail | Shared capability | Event logging |
