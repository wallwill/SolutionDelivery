Architecture Alignment Assessment
•	Overview
•	Requirements 
o	Alignment Legend
o	Requirements Evaluated
•	Review Process (Ireland) 
o	Review Board
o	Review Template
o	Assessments
Overview
In order to ensure alignment with enterprise and local standards for the products or solutions being developed at Carelon Global Solutions Ireland a local auditing process is required. The audit will be conducted by the local architecture team. It is also an opportunity for having local architects review the design and implementation of the solution to provide feedback, identify potential issues, and suggest improvements.
Requirements
Alignment Legend
ALIGNMENT 	MEANING	VALUE
FULL	The expected architecture outputs exist. Expectation has been met.	2
PARTIAL	Some of the expected architecture outputs exist. Expectation minimally has been met.	1
NONE	No evidence of the expected architecture outputs. Expectation have not been met.	0
Requirements Evaluated 
REQUIREMENT ID 	REQUIREMENT NAME	WHAT TO CHECK	WHERE TO CHECK 	Architecture
Scope	ARCHITECTURE PROCESS (cross referencing)
ANALYSIS-01	Domain Architecture Alignment	Is this an existing solution, a net new solution, a solution migration, or other? Checking here for the High Level Design being aligned to the business domain.	High Level Design Diagram	Solution Architecture
Application Architecture	Activity: Design Overall Solution
Outputs:
•	Overall Solution Architecture
ANALYSIS-02	Gap Analysis	Is there a definition of the discrepancies between the current and desired state? Is this an innovation and is there intellectual property associated with this solution? Looking for a value statement on a Lean Canvas. 	Lean Canvas Slide (distills down the essence relating to this product or solution.)	Solution Architecture	Activity: Assess Strategic Architecture Gateway
Tasks:
•	Understand Business Context
•	Understand Overall Value Streams
•	Understand Innovation and Intellectual Property for CGSI
Outputs:
•	Strategic Architecture Acceptance (or Lean Canvas)
•	Innovation and Intellectual Property Proposal (if applicable)
ANALYSIS-03	Non-Functional Requirements	Non-Functional Requirements are documented. 
Simple NFR Template from SAFE Arch (https://scaledagileframework.com/nonfunctional-requirements/) :
Name: << quality.sub-quality >>
Scale: << units >>
Meter: << measurement method >>
Target: << success level >>
Constraint: << failure level >>
Baseline: << current level >>
Example NFR
Name: Performance - Efficiency
Scale: Number of Claims Per Second (CPS)
Meter: Average request / response time
Target: 200 claims per second
Constraint: <100 claims per second
Baseline: 100 claims per second	Confluence or Jira	Application Architecture	Activity: Manage Risks and NFR's
Outputs:
•	NFR's Management Plan
•	Risk Mitigation Plan
VISION-01	Architectural Principles	Architectural Guiding Principles. (Enterprise)
What architectural principles are being follow in this solution:
1.	Reuse
2.	Microservices
3.	Event based Architectures 
4.	Loose coupling/Tightly Cohesive	Adhoc evidence. The documentation ideally should reference the principles being followed.		Activity: Design Overall Solution
Tasks:
•	Decompose Solution in Modules
Outputs:
•	Overall Solution Architecture
•	Application Architecture
•	Data Architecture
VISION-02	Stakeholder Map	Identify stakeholders, their influence, and key questions or concerns	Confluence		Activity: Manage Stakeholders
Outputs:
•	Stakeholder Communication Plan
VISION-03	Value Chain	The chain of activities performed to produce a product or service from start to finish. This chain helps identify where we can add the most value, improve efficiency and reduce costs. We are checking the high-level organisational and functional context in which this product or solution fits.	Value Chain Diagram		Activity: Design Overall Solution
Tasks:
•	Fulfil Overall Value Streams 
VISION-04	Solution Concept	Future state High Level Design.	High Level Design Diagram	 	Activity: Assess Strategic Architecture Gateway
Tasks:
•	Understand Business Context
Outputs:
•	Strategic Architecture Acceptance
BUSINESS-01	Business Controls	Thinking from the business perspective. Processes followed for business policies in following areas as applicable:
•	security
•	data protection
•	availability
•	change management
•	incident management
•	accessibility
•	compliance
•	continuity
•	vendor management
•	knowledge management
•	quality assurance
•	service level agreements
•	budget and cost management
•	intellectual property	TGOV, ITSM, CHG Tickets, DR Plan	Application Architecture	Activity: Design Overall Solution
Tasks:
•	Review Adherence to Enterprise Standards
DATA-01	Data Security	PHI/PII/PFI/GDPR, regulatory requirements, protection
https://eshare.elevancehealth.com/home/sites/cee/pages/Ethics_and_Compliance/Privacy/index.cfm
Elevance Health Policies and Standards
CIR review/tickets etc.	Application Architecture	Activity: Submit for Security Review
Tasks:
•	Submit Data Governance Report
Outputs:
•	Security Architecture Report 
DATA-02	Enterprise Data Firewall	Enterprise Data Firewall (not tech.)	Documented approach.		Activity: Submit for Security Review
Tasks:
•	Submit Data Governance Report
Outputs:
•	Data Governance Report
DATA-03	Data Flow	Data flow diagram, schema, versioning/change management	Data Flow Diagram		Activity: Design Overall Solution
Outputs:
•	Data Architecture
SEC-01	Access Control	CISO - RBAC/PBAC/ABAC concerns or other	Security Matrix		Activity: Submit for Security Review
Tasks:
•	Submit Security Architecture Report
Outputs:
•	Security Architecture Report
APPLICATION-01	Application Registration	Product or solution must exists in AppLab, and for the cloud platform requires the associated Central Intake Requests plus evidence of proper resource tagging.	Application Identifiers, Resource Tagging		Activity: Manage Product Platform
Tasks:
•	Tag and Register Application in Platform Management Repositories
Outputs:
•	AppLab entry
APPLICATION-02	API Specifications	APIs defined and managed, API docs (e.g. Swagger), Interface Catalog	Swagger or OpenAPI Specifications	Application Architecture	Activity: Design Features Solution Intent
Outputs:
•	Feature Solution Design Document
APPLICATION-03	CI/CD	What CI and CD is in place (scans clean, tests passing). Level of maturity, culture, level of automation, user empowerment and ownership.	Screenshot of Bamboo or other tool, EHDS, SonarCube, CheckMarx	Application Architecture	Activity: Manage Product Platform
Outputs:
•	CICD Pipeline
•	DevOps Playbook
•	Test Automation Scripts
•	DevOps Infrastructure as Code
APPLICATION-04	Technology Matrix	Technology Matrix i.e. the stack	Technology Matrix on Confluence	Technical Architecture	Activity: Design Overall Solution
Outputs:
•	Overall Solution Architecture
•	Application Architecture
APPLICATION-05	Performance	Performance testing evidence	Performance Test Reports	Application Architecture	Activity: Manage Product Platform
Tasks:
•	Support Performance Engineering
APPLICATION-06	Architectural Artifacts	Architecture diagrams/documents maintained, and local standards applied	Confluence		Activity: Design Overall Solution
Outputs:
•	Overall Solution Architecture
APPLICATION-07	Reference Architecture Patterns 	Relevant patterns followed from RAPL	High Level Design references usage		Activity: Design Overall Solution
Outputs:
•	Overall Solution Architecture
APPLICATION-08	Application Security	Application Security Scans	Prisma (vulnerability) listing		Activity: Manage Product Platform
Tasks:
•	Monitor and Manage Application Security Violations
Outputs:
•	Security Scan Reports
APPLICATION-09	Observability and Monitoring	Splunk, Datadog, Dashboards. The ability to correlate activities via tracing.	Screenshots, Tickets/Access Requests		Activity: Manage Product Platform
Outputs:
•	Product Dashboards / Logs / Traces
APPLICATION-10	Architecture Decision Records	Architecture Decisions Records	Architecture Decisions Records on Confluence		Activity: Manage Architecture Decisions
Outputs:
•	ADR's
APPLICATION-11	BCM Mapping (Level 1)	BCM Heat-map Diagram	BCM Heat-map Diagram on Confluence		Activity: Assess Strategic Architecture Gateway
Tasks:
•	Understand Business Context
Outputs:
•	Strategic Architecture Acceptance
APPLICATION-12	Value Stream Mapping (Level 1)	A value stream is a continuous flow of activities that adds value from the perspective of the customer, it helps to identify waste and non-value-added activities, and to focus on delivering value faster and more efficiently. We are checking the product or solution is adding the expected value.	Value Stream Diagram on Confluence		Activity: Design Overall Solution
Tasks:
•	Fulfil Overall Value Streams 
TECHNOLOGY-01	ESG and DOTS	Check the IT stack is compliant	Matrix of Tech Stack and ESG status		Activity: Manage Architecture Decisions
Outputs:
•	ADR's
Activity: Design Overall Solution
Tasks:
•	Review Adherence to Enterprise Standards
TECHNOLOGY-02	Environment Management	Environments/Locations/Platforms per enterprise direction. What environments exist? e.g. DEV/SIT/UAT/PERF. Who owns or should own the environment?	Environment RACI on Confluence		Activity: Manage Product Platform
Tasks:
•	Optimise Product Resources
