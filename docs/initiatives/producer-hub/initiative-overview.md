# Producer Hub - Initiative Overview

## Purpose
Producer Hub is a shared underwriting service used to validate and retrieve producer information needed by underwriting workflows and platform integrations.

## Business Objective
Provide a consistent producer data service that reduces manual validation, improves data quality, and supports downstream underwriting decisions.

## Strategic Alignment
Producer Hub supports the underwriting modernization roadmap by providing a reusable integration capability across standalone applications and U360.

## Status
**Current Status:** In Progress

## Scope
### In Scope
- producer lookup
- producer validation
- producer profile retrieval for underwriting workflows

### Out of Scope
- producer commission processing
- producer onboarding outside underwriting usage

## Initiative Type
- Shared Service
- Integration

## Target Operating Role
Shared service used by underwriting applications and U360 to retrieve and validate producer information.

## Relationship to Legacy Systems
Producer Hub standardizes access to producer information while source systems continue to own the data.

## Applications / Components
| Component | Type | Purpose | Owner |
|---|---|---|---|
| Producer Hub Service | Service | Producer validation and lookup API | Integration Team |

## Stakeholders
| Role | Name / Team | Responsibility |
|---|---|---|
| Business Owner | Underwriting Operations | Business sponsorship |
| Product Owner | Producer Hub Product | Prioritization |
| Technology Owner | Integration Engineering | Delivery ownership |
| Architecture Owner | Enterprise Architecture | Design oversight |
| Support Owner | Application Support | Production support |
| Control Owner | Risk and Controls | Control accountability |

## Dependencies
| Dependency | Type | Purpose | Criticality | Owner |
|---|---|---|---|---|
| Upstream producer source | System | Producer master/reference data | High | External owner |
| U360 | Platform | Consumer of producer data | High | U360 team |

## Roadmap
| Milestone / Phase | Description | Target Date | Status |
|---|---|---|---|
| API baseline | Core producer lookup and validation | 2026-Q2 | In Progress |
| U360 integration | Shared capability consumption | 2026-Q3 | Planned |

## Success Metrics / Expected Benefits
| Benefit | KPI | Baseline | Target | Owner |
|---|---|---|---|---|
| Reduced manual validation | % manual producer lookups | High manual effort | 50% reduction | Product Owner |

## Key Risks / Open Questions
| ID | Risk / Question | Impact | Owner | Mitigation / Next Step | Status |
|---|---|---|---|---|---|
| R1 | Source system response latency | Integration delays | Tech Owner | Add retry and timeout design | Open |

## Audit / Compliance References
- [Control Mapping](./audit/control-mapping.md)
- [Evidence Index](./audit/evidence-index.md)
