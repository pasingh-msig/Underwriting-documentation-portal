# Convr Service - Operational Controls

## Control Overview
Document the key preventive, detective, and support controls for Convr.

## Preventive Controls
| Control ID | Control Name | Description | Owner | Frequency | Evidence |
|---|---|---|---|---|---|
| PC-01 | Access Control | Only approved users and systems can access the application | <Owner> | Continuous | Access records |
| PC-02 | Release Control | Changes follow controlled release process | <Owner> | Per release | Change record |

## Detective Controls
| Control ID | Control Name | Description | Owner | Frequency | Evidence |
|---|---|---|---|---|---|
| DC-01 | Failure Monitoring | Failed processing or integration issues generate alerts | <Owner> | Continuous | Monitoring dashboard |

## Access Controls
- user access follows approved provisioning process
- elevated access is restricted and reviewable

## Change Controls
- production changes require review and approval
- emergency changes should be documented and reviewed afterward

## Interface / Batch Controls
- interface failures are detected through monitoring
- recovery actions are documented through support process

## Reconciliation Controls
- key status or processing counts should be reviewed where applicable

## Logging and Audit Trail Controls
Significant processing events, failures, and exception handling should be logged.

## Incident and Escalation Controls
Incidents are triaged by L1 and escalated to higher support tiers as needed.

## Control Exceptions
Exceptions should be approved, logged, and reviewed.

## Related Risks
- dependency outages
- incomplete evidence linkage
- support coverage gaps

## Evidence References
- monitoring dashboard
- change records
- access reviews
- incident tickets
