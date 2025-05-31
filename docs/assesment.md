# Architecture Alignment Assessment

- Overview
- Requirements
  - Alignment Legend
  - Requirements Evaluated


## Overview

In order to ensure alignment with enterprise and local standards for the products or solutions being developed at a subsidary entity a local auditing process is required. The audit will be conducted by the local architecture team. It is also an opportunity for having local architects review the design and implementation of the solution to provide feedback, identify potential issues, and suggest improvements.

## Requirements

### Alignment Legend

| ALIGNMENT | MEANING | VALUE |
|-----------|---------|--------|
| FULL | The expected architecture outputs exist. Expectation has been met. | 2 |
| PARTIAL | Some of the expected architecture outputs exist. Expectation minimally has been met. | 1 |
| NONE | No evidence of the expected architecture outputs. Expectation have not been met. | 0 |

### Requirements Evaluated

#### ARCHITECTURE PROCESS (cross referencing)

**ANALYSIS-01**: Domain Architecture Alignment  
_Is this an existing solution, a net new solution, a solution migration, or other? Checking here for the High Level Design being aligned to the business domain._  
- Where: High Level Design Diagram  
- Architecture: Solution Architecture  
- Activity: Design Overall Solution  
- Outputs:
  - Overall Solution Architecture

**ANALYSIS-02**: Gap Analysis  
_Is there a definition of the discrepancies between the current and desired state? Is this an innovation and is there intellectual property associated with this solution? Looking for a value statement on a Lean Canvas._  
- Where: Lean Canvas Slide  
- Architecture: Solution Architecture  
- Activity: Assess Strategic Architecture Gateway  
- Tasks:
  - Understand Business Context
  - Understand Overall Value Streams
  - Understand Innovation and Intellectual Property for CGSI  
- Outputs:
  - Strategic Architecture Acceptance (or Lean Canvas)
  - Innovation and Intellectual Property Proposal (if applicable)

**ANALYSIS-03**: Non-Functional Requirements  
_Non-Functional Requirements are documented._  
Simple NFR Template from SAFE Arch:  
<https://scaledagileframework.com/nonfunctional-requirements/>

```
Name: << quality.sub-quality >>
Scale: << units >>
Meter: << measurement method >>
Target: << success level >>
Constraint: << failure level >>
Baseline: << current level >>
```

**Example NFR**

```
Name: Performance - Efficiency
Scale: Number of Claims Per Second (CPS)
Meter: Average request / response time
Target: 200 claims per second
Constraint: <100 claims per second
Baseline: 100 claims per second
```

- Where: Confluence or Jira  
- Architecture: Application Architecture  
- Activity: Manage Risks and NFR's  
- Outputs:
  - NFR's Management Plan
  - Risk Mitigation Plan

---

**VISION-01**: Architectural Principles  
Architectural Guiding Principles (Enterprise) being followed:  
1. Reuse  
2. Microservices  
3. Event based Architectures  
4. Loose coupling/Tightly Cohesive  
- Evidence: Adhoc  
- Activity: Design Overall Solution  
- Tasks:
  - Decompose Solution in Modules  
- Outputs:
  - Overall Solution Architecture
  - Application Architecture
  - Data Architecture

**VISION-02**: Stakeholder Map  
- What to Check: Identify stakeholders, their influence, and key questions or concerns  
- Where: Confluence  
- Activity: Manage Stakeholders  
- Outputs:
  - Stakeholder Communication Plan

**VISION-03**: Value Chain  
- What to Check: High-level organisational and functional context  
- Where: Value Chain Diagram  
- Activity: Design Overall Solution  
- Tasks:
  - Fulfil Overall Value Streams

**VISION-04**: Solution Concept  
- What to Check: Future state High Level Design  
- Where: High Level Design Diagram  
- Activity: Assess Strategic Architecture Gateway  
- Tasks:
  - Understand Business Context  
- Outputs:
  - Strategic Architecture Acceptance

---

**BUSINESS-01**: Business Controls  
Business policy areas as applicable:

    - Security
    - Data protection
    - Availability
    - Change management
    - Incident management
    - Accessibility
    - Compliance
    - Business Continuity/DR
    - Vendor management
    - Knowledge management
    - Quality assurance
    - Service level agreements
    - Budget and cost management
    - Intellectual property

- Where:  ITSM, CHG Tickets, DR Plan  
- Architecture: Application Architecture  
- Activity: Design Overall Solution  
- Tasks:
  - Review Adherence to Enterprise Standards

---

**DATA-01**: Data Security  
- What to Check: PHI/PII/PFI/GDPR, regulatory requirements, protection  
- Where: Cloud Infra reviews, Enterprise Policicies 
- Activity: Submit for Security Review  
- Tasks:
  - Submit Data Governance Report  
- Outputs:
  - Security Architecture Report

**DATA-02**: Enterprise Data Firewall  
- What to Check: Documented approach  
- Activity: Submit for Security Review  
- Outputs:
  - Data Governance Report

**DATA-03**: Data Flow  
- What to Check: Data flow diagram, schema, versioning/change management  
- Where: Data Flow Diagram  
- Activity: Design Overall Solution  
- Outputs:
  - Data Architecture

---

**SEC-01**: Access Control  
- What to Check: CISO - RBAC/PBAC/ABAC concerns  
- Where: Security Matrix  
- Activity: Submit for Security Review  
- Outputs:
  - Security Architecture Report

---

**APPLICATION-01**: Application Registration  
- What to Check: Enterprise Application Management
- Where: Application Identifiers  
- Activity: Manage Product Platform  
- Tasks:
  - Tag and Register Application  
- Outputs:
  - Application ID(s)

**APPLICATION-02**: API Specifications  
- What to Check: Swagger/OpenAPI, Interface Catalog  
- Where: API Specs  
- Architecture: Application Architecture  
- Activity: Design Features Solution Intent  
- Outputs:
  - Feature Solution Design Document

**APPLICATION-03**: CI/CD  
- What to Check: CI/CD setup, automation, testing  
- Where: Bamboo, EHDS, SonarCube, CheckMarx  
- Architecture: Application Architecture  
- Activity: Manage Product Platform  
- Outputs:
  - CICD Pipeline
  - DevOps Playbook
  - Test Automation Scripts
  - DevOps Infrastructure as Code

**APPLICATION-04**: Technology Matrix  
- What to Check: Tech stack documentation  
- Where: Confluence  
- Architecture: Technical Architecture  
- Activity: Design Overall Solution  
- Outputs:
  - Overall/Application Architecture

**APPLICATION-05**: Performance  
- What to Check: Performance test reports  
- Where: Test Reports  
- Architecture: Application Architecture  
- Activity: Manage Product Platform  
- Tasks:
  - Support Performance Engineering

**APPLICATION-06**: Architectural Artifacts  
- What to Check: Maintained architecture documents  
- Where: Confluence  
- Activity: Design Overall Solution  
- Outputs:
  - Overall Solution Architecture

**APPLICATION-07**: Reference Architecture Patterns

 - What to Check: Reference Patterns
 - Where: Eneterprise Reference Pattern Library
 - Activity: Design Overall Solution  
 - Outputs: Overall Solution Architecture

**APPLICATION-08**: Application Security  
- What to Check: Vulnerability scan results  
- Where: Prisma  
- Activity: Manage Product Platform  
- Tasks:
  - Monitor and Manage Violations  
- Outputs:
  - Security Scan Reports

**APPLICATION-09**: Observability and Monitoring  
- What to Check: Logs, dashboards, tracing  
- Where: Splunk, Datadog  
- Activity: Manage Product Platform  
- Outputs:
  - Dashboards / Logs / Traces

**APPLICATION-10**: Architecture Decision Records  
- Where: Application Documentation 
- Activity: Manage Architecture Decisions  
- Outputs:
  - ADRs

**APPLICATION-11**: BCM Mapping (Level 1)  
- Where:  Application Documentation 
- Activity: Assess Strategic Architecture Gateway  
- Tasks:
  - Understand Business Context  
- Outputs:
  - Strategic Architecture Acceptance

**APPLICATION-12**: Value Stream Mapping (Level 1)  
- Where: Application Documentation  
- Activity: Design Overall Solution  
- Tasks:
  - Fulfil Value Streams

---

**TECHNOLOGY-01**:   
- What to Check: Tech stack compliance  
- Where: Enterprise Technology Repository (If Exists)
- Activity: Manage Architecture Decisions  
- Outputs:
  - ADRs  
- Additional Activity: Design Overall Solution  
- Tasks:
  - Review Adherence to Standards

**TECHNOLOGY-02**: Environment Management  
- What to Check: Environment setups (DEV/SIT/UAT/PERF/PROD)  
- Where: Environment RACI   
- Activity: Manage Product Platform  
- Tasks:
  - Optimise Product Resources

