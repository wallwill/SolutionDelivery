# Scoring Criteria for Peer Review

## General Guidelines
- If a program exhibits criteria from multiple ratings on the scale, review members should use their judgment to determine which criteria are more important for the architecture being reviewed and provide a rating accordingly. Keep it simple and avoid over-engineering the scoring process.
- If any tech strategy is not applicable to the architecture/investment being reviewed, rate it as 3, the same as acceptable strategic alignment.
- Use these criteria as guidelines. Reviewers should use their best judgment to provide an objective rating for the architecture, as not every possible scenario might be covered within the criteria.

## What Does Rate 1-5 Signify?

| Rating | Significance                  |
|--------|-------------------------------|
| 1      | Lacks Strategic Alignment     |
| 2      | Deviates from Strategy        |
| 3      | Acceptable Strategic Alignment|
| 4      | Good Strategic Alignment      |
| 5      | Best Strategic Alignment      |


## Modernization

| Score | Criteria                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------|
| 1     | - New or unmodified monolithic application                                                          |
|       | - Application does not scale                                                                        |
|       | - Architecture inhibits ability to make core data accessible through data externalization techniques|
|       | - Not aligned to the criteria for Modern APIs and API standards with a critical severity rating of >3000ms P95 latency|
|       | - No AI best practices met                                                                          |
| 2     | - New or unmodified monolithic application                                                          |
|       | - Application scales vertically                                                                     |
|       | - No plans to make core data accessible through data externalization techniques.                    |
|       | - Somewhat aligned to the criteria for Modern, API standards with a high severity rating of >1000ms but <3000ms P95 latency |
|       | - 1-5 AI best practices met; team has no plan to meet outstanding                                   |
| 3     | - Minor enhancements to monolithic application, majority microservices cloud architecture.          |
|       | - Majority cloud native architecture, Application scales both vertically and horizontally with manual intervention |
|       | - Plans in place to make core data accessible through data externalization techniques.              |
|       | - Targeted to align to the criteria for Modern API standards with a medium severity rating of >500ms but <1000ms P95 latency |
|       | - 1-5 AI best practices met, team has plan to meet outstanding or 6-10 AI best practices met, team has no plan to meet outstanding |
| 4     | - Transitioning towards a full microservices, cloud-based architecture                              |
|       | - Using CI/CD, automation for build/deploy but testing not fully automated                          |
|       | - Transitioning towards full cloud native architecture, Application scales both vertically and horizontally with partial automation |
|       | - Core data accessible through data externalization techniques                                      |
|       | - Aligned to the criteria for Modern API standards with a low severity rating of >200ms but <500ms P95 latency soon to be reported within Enterprise Advisor |
|       | - 6-10 AI best practices met, team has plan to meet outstanding                                     |
| 5     | - Cloud-based architecture (Cloud native and failure mgmt. Containers. Based on Domain Driven Design and Microservice Architecture, Infra as code) |
|       | - Full cloud native architecture, Application scales both vertically and horizontally with full automation |
|       | - Recognized as key contributor, maintainer and/or reviewer for 3rd party contributions Core data accessible through data externalization techniques, aligned with and promoting use of Enterprise core architecture |
|       | - Building technology asset using emerging technologies for enterprise reuse                        |
|       | - Aligned to the criteria for Modern API standards with a goal rating of <200ms P95 latency as reported by Enterprise Advisor |
|       | - All AI best practices met |  

## Reuse & Simplify

| Score | Criteria                                                                                                                                                     |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | - Increase in TCO and addition to technical or architectural debt                                                                                           |
|       | - Not a core API, internal API solving one business use case                                                                                                 |
|       | - No reuse of core API or core asset                                                                                                                         |
|       | - Duplication of function and/or data of an existing Enterprise Capability but for a different data set/domain/sales context                                 |
|       | - No method of publishing capability backlog (Aha!)                                                                                                          |
|       | - No contribution to inner source                                                                                                                            |
|       | - No code/config/lifecycle segregation of Line of Business (LoB) specific functionality from core common capabilities                                         |
|       | - Uses Discouraged or Unacceptable technologies                                                                                                              |
|       | - Significantly adds to the duplication of data, duplication of code bases, and/or duplication of security-related context/attributes                         |
|       | - No metadata or capability publication to enterprise solutions                                                                                              |
| 2     | - Inherits existing technical or architecture debt with minor incremental additions to debt                                                                  |
|       | - Not a core API, internal API solving multiple business use cases                                                                                           |
|       | - No reuse of core API or core asset                                                                                                                         |
|       | - No contribution to inner source                                                                                                                            |
|       | - Transitioning to publishing product backlog                                                                                                                |
|       | - Limited duplication of data, no duplication/forking of code, no duplication of security-related context/attributes                                         |
|       | - No metadata or capability publication to enterprise solutions                                                                                              |
| 3     | - Inherits existing technical or architecture debt with minor incremental additions to debt                                                                  |
|       | - Not a core API, internal API solving multiple business use cases                                                                                           |
|       | - No reuse of core API or core asset                                                                                                                         |
|       | - No contribution to inner source                                                                                                                            |
|       | - Transitioning to publishing product backlog                                                                                                                |
|       | - Limited duplication of data, no duplication/forking of code, no duplication of security-related context/attributes                                         |
|       | - Limited metadata publication to enterprise solutions                                                                                                       |
| 4     | - Significant (or net) reduction to technical or architectural debt, OR significant reductions in duplication of existing function                          |
|       | - Not a core API, internal API solving multiple business use cases                                                                                           |
|       | - Core enterprise asset                                                                                                                                      |
|       | - Reuse of core API                                                                                                                                          |
|       | - Contributing to inner source                                                                                                                               |
|       | - Transition towards exposing data and functionality as API streams, not all sources streaming                                                               |
|       | - Transition towards exposing/consuming product/application agnostic Business Events to the Enterprise ecosystem                                            |
|       | - Primarily leveraging Preferred technologies                                                                                                                |
| 5     | - Decommissioning of existing assets directly reducing Total Cost of Ownership and Technical Debt                                                            |
|       | - Is a core API, can be reused by other applications                                                                                                          |
|       | - Core enterprise asset                                                                                                                                      |
|       | - Producing and contributing to streams                                                                                                                      |
|       | - No duplication of data from Enterprise capabilities                                                                                                        |
|       | - Product/Application agnostic Business Events published to Enterprise Consumers                                                                             |
|       | - Contribution to inner source                                                                                                                               |
|       | - Fully matured federated product and federated software development lifecycle                                                                               |
|       | - Fully enterprise viewable federated product capability backlog with regular cadence of product council review, prioritization, and feature governance      |

## Data Management

(Note: Assumption here of an Enterprise Data Catalog)

| Score | Criteria                                                                                                                                                                                                                                                 |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | - **Data Governance**: Data usage and rights have been mainly ignored. What's a data steward? Business owner/stakeholders are not at the table for decisions. Unnecessarily duplicates data (tables) and repositories. Datasets (raw metadata) do not exist in the Enterprise Catalog.              |
|       | - **Metadata Management**: There is no capture of any metadata in the solution.                                                                                                                                                                           |
|       | - **Data Quality**: Data quality characteristics are not understood for data repositories present in this solution. No DQ exception processing has been considered. Enterprise capability is ignored, and actions are taken based on inputs from consumer and downstream applications.               |
|       | - **Data Orchestration & Integration**: Job scheduling and pipeline orchestration have not been considered. Existing Data Products have not been considered with no intent to build a new one. The data pipeline uses unacceptable tools. Failure points and impacts on downstream processes undefined. Requirements for data pipeline latency, throughput, and elasticity are not defined. No RPO or RTO defined. |
|       | - **Information Model**: Missed opportunities to employ canonical data; no roadmap to remediate; accesses source system data directly.                                                                                                                    |
|       | - **Data Privacy**: Data at rest or in transit is never encrypted, or sensitive data (PHI/PII) is not masked/de-identified/tokenized. Enterprise capability is ignored.                                                                                    |
|       | - **Reporting & Analytics**: Solution ignores reporting and analytics considerations.                                                                                                                                                                     |
|       | - **Data Repositories**: Scalability, reliability, serviceability, performance, fault-tolerance, availability, and capacity for the solution are ignored. Solution fails when data repositories are unavailable. Site availability less than 80%. No auto scalability, unmet SLAs, no DR or forecast plan. |
|       | - **Reference Data**: Reference data traditionally ignored, leading to duplicate, outdated, and inaccurate data instances with multiple licenses, incurring cost.                                                                                            |
| 2     | - **Data Governance**: Datasets with raw metadata are available on the Enterprise Data Catalog with enforced metadata by contract. Some data usage and rights criteria reviewed. Ad-hoc data steward available. Sporadic stakeholder involvement. Some duplicative outcome for the enterprise.        |
|       | - **Metadata Management**: Capture of existing production technical or business metadata exists in a non-preferred data catalog.                                                                                                                          |
|       | - **Data Quality**: Data quality characteristics understood for major repositories; minor DQ exception processing considered. Enterprise capabilities acknowledged but not engaged. Focus is on ETL-based DQ check or manual QA team queries.                                                       |
|       | - **Data Orchestration & Integration**: Minimal job scheduling and pipeline orchestration, with discouraged tools. Some failure points addressed. Requirements for latency, throughput, and elasticity partially defined. RPO and RTO defined but viability unclear.                                |
|       | - **Information Model**: Missed opportunities to employ canonical data; remediation roadmap in place; accesses source system data directly.                                                                                                                |
| 3     | - **Data Governance**: Datasets with raw metadata and some enrichments available on the Enterprise Catalog. Informally reviewed data usage and rights criteria. Ad-hoc data steward available with some stakeholder processes. Less duplicative outcome for the enterprise.                        |
|       | - **Metadata Management**: Existing production technical metadata used to populate a dataset in the Enterprise Data Platform with some business metadata (e.g., data steward, definitions).                                                              |
|       | - **Data Privacy**: Sensitive data at rest or in transit is masked/de-identified/tokenized. Enterprise capabilities assessed.                                                                                                                             |
|       | - **Data Orchestration & Integration**: Minor job scheduling and orchestration with minor automation. Some existing Data Products leveraged. Pipeline uses acceptable tools. Most failure points addressed. Defined latency, throughput, and elasticity requirements, albeit viability is unclear.    |
|       | - **Information Model**: Some use of canonical data where appropriate; does not access source system data directly.                                                                                                                                        |
|       | - **Data Quality**: Some data quality characteristics understood for some repositories. Some DQ processing considered. Enterprise capabilities evaluated.                                                                                                 |
|       | - **Reporting & Analytics**: Solution considers major reporting and analytics elements. Enterprise capabilities assessed.                                                                                                                                |
|       | - **Data Repositories**: Some focus on scalability, reliability, and other metrics. Site availability 85-90%. Auto-scaling exists with generally met SLAs. Some performance metrics captured periodically, with DR and forecast planning in place.                                                 |
|       | - **Reference Data**: Datasets available on the Enterprise Data Catalog for public healthcare and endorsed business standards, including technical and business metadata for healthcare reference data licensed by other units.                                                                  |
| 4     | - **Data Governance**: Asset available on the Enterprise Data Catalog as Data Product(s) with robust enrichments. Subscription requests reviewed within the Data Platform Catalog. Access manually provisioned. Minimum duplicative outcome for the enterprise.                                      |
|       | - **Metadata Management**: Production metadata used in a full-function suite in the Data Platform with data lineage and manual enrichment.                                                                                                                 |
|       | - **Data Quality**: Well-understood data quality characteristics for key repositories. Happy-path DQ processing evident. Enterprise capabilities included in plan.                                                                                                                               |
|       | - **Data Orchestration & Integration**: Good job scheduling and automation support. Existing Data Products leveraged. Some preferred tools used. Most failure points addressed and recovery plans considered. Defined latency, throughput, and elasticity requirements. RPO and RTO plans developed.   |
|       | - **Information Model**: Good use of canonical data; does not access source system data directly.                                                                                                                                                         |
|       | - **Data Privacy**: Sensitive data both at rest and in transit masked/de-identified/tokenized. Enterprise capabilities planned.                                                                                                                            |
|       | - **Reporting & Analytics**: Reporting and analytics integral to the solution, with enterprise capabilities planned.                                                                                                                                     |
|       | - **Data Repositories**: Significant attention to metrics like scalability and availability, surviving short-term outages. Numerous dashboards for metrics. Site availability 90-95%. Auto-scaling solutions mostly meeting SLAs with RCAs on discrepancies.       |
|       | - **Reference Data**: Subscription requests reviewed by Data Product Owners; reference data access managed by the reference management team via the HPC Data Platform.                                                                                   |
| 5     | - **Data Governance**: Asset available on the Enterprise Data Catalog as Data Product(s) with extensive metadata enrichments.                                                                                                                            |
|       | - **Metadata Management**: Metadata populates a full-function suite with comprehensive lineage and automated enrichment using Enterprise classification tools.                                                                                            |
|       | - **Data Quality**: Comprehensive understanding of data quality characteristics, including profiling and DQ exception processing.                                                                                                                     |
|       | - **Data Orchestration & Integration**: Automated job scheduling and orchestration. Existing and new reusable Data Products. Uses all preferred tools. All failure points addressed. Defined latency, throughput, and elasticity requirements with evidence of achievement, including RPO/RTO design. |
|       | - **Information Model**: Excellent use of canonical data, strengthening existing definitions; avoids direct system data access.                                                                                                                            |
|       | - **Data Privacy**: Sensitive data both at rest and in transit masked/de-identified/tokenized. Enterprise capabilities engaged as needed.                                                                                                                  |
|       | - **Data Integration, Reporting & Analytics**: Comprehensive account in architecture with engaged enterprise capabilities.                                                                                                                                   |
|       | - **Data Repositories**: Robust solutions with metrics captured via dashboards, monitoring, and alerts. All SLAs tracked, with comprehensive planning for scalability, fault-tolerance, and capacity. |   
|.     	| - **Reference Data **: All subscription requests are reviewed within the Enterprise Data Platform Catalog by Data Product Owners.  |

## Security

| Score | Criteria                                                                                                                                                                                      |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | - Less than 59% of applications use enterprise capability for identity and access management                                                                                                  |
|       | - Less than 59% of applications use enterprise capability for source code management and infrastructure as code                                                                               |
|       | - Less than 59% of applications use enterprise-approved encryption methods for data at rest and data in transit                                                                               |
|       | - Less than 59% of applications have logging and monitoring in place using enterprise capability                                                                                               |
|       | - Less than 59% remediation of Severe, Critical, and High violations for all applicable vulnerabilities scans according to application risk category (Static, Dynamic, Pen Test)              |
|       | - Less than 59% of applications have appropriate network controls in place for segmentation, endpoint protection, and defense in depth                                                                                                |
| 2     | - 60% - 69% of applications use enterprise capability for identity and access management                                                                                                       |
|       | - 60% - 69% of applications use enterprise capability for source code management and infrastructure as code (GitHub)                                                                           |
|       | - 60% - 69% of applications use enterprise-approved encryption methods for data at rest and data in transit                                                                                   |
|       | - 60% - 69% of applications have logging and monitoring in place using enterprise capability                                                                                                    |
|       | - 60% - 69% of remediations for Severe, Critical, and High violations for all applicable vulnerabilities scans according to application risk category (Static, Dynamic, Pen Test)              |
|       | - 60% - 69% of applications have appropriate network controls in place for segmentation, endpoint protection, and defense in depth                                                                                                    |
| 3     | - 70% - 79% of applications use enterprise capability for identity and access management                                                                                                       |
|       | - 70% - 79% of applications use enterprise capability for source code management and infrastructure as code                                                                                    |
|       | - 70% - 79% of applications use enterprise-approved encryption methods for data at rest and data in transit                                                                                    |
|       | - 70% - 79% of applications have logging and monitoring in place using enterprise capability                                                                                                    |
|       | - 70% - 79% remediation of Severe, Critical, and High violations of all applicable vulnerabilities according to application risk category (Static, Dynamic, Pen Test)                          |
|       | - 70% - 79% of applications have appropriate network controls in place for segmentation, endpoint protection, and defense in depth                                                                                                      |
| 4     | - 80% - 90% of applications use enterprise capability for identity and access management                                                                                                        |
|       | - 80% - 90% of applications use enterprise capability for source code management and infrastructure as code                                                                                    |
|       | - 80% - 90% of applications use enterprise-approved encryption methods for data at rest and data in transit                                                                                    |
|       | - 80% - 90% of applications have logging and monitoring in place using enterprise capability                                                                                                    |
|       | - 80% - 90% remediation of Severe, Critical, and High violations of all applicable vulnerabilities according to application risk category (Static, Dynamic, Pen Test)                          |
|       | - 80% - 90% of applications have appropriate network controls in place for segmentation, endpoint protection, and defense in depth                                                                                                     |
| 5     | - 100% of applications use enterprise capability for identity and access management                                                                                                            |
|       | - 100% of applications use enterprise capability for source code management and infrastructure as code                                                                                         |
|       | - 100% of applications use enterprise-approved encryption methods for data at rest and data in transit                                                                                         |
|       | - 100% of applications have logging and monitoring in place using enterprise capability                                                                                                         |
|       | - 100% remediation of Severe, Critical, and High violations of all applicable vulnerabilities according to application risk category (Static, Dynamic, Pen Test)                               |
|       | - 100% of applications have appropriate network controls in place for segmentation, endpoint protection, and defense in depth    |

                                                                                                         |
## Consumer Experience

| Score | Criteria                                                                                                                                                                                 |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | - Stakeholder experience is not seamless or personalized, leading to a negative NPS for the product or solution                                                                           |
|       | - Outreach to end constituents (e.g., via email, SMS) is not aligned to standards, outmoded (e.g., paper, fax), and is not documented or coordinated across business LoBs                 |
|       | - Experiences are created in a bespoke fashion based on modality (e.g., web only), not allowing seamless leverage across various devices (mobile, tablet, etc.)                          |
|       | - Significant increase to TCO in the short or long term with no new capabilities                                                                                                         |
|       | - Solution architecture and development process does not enable quick delivery of business value (more than 9-12 months)                                                                  |
|       | - Solution does not use common components to provide a consistent experience                                                                                                              |
|       | - Solution does not tag and track experience                                                                                                                                              |
| 2     | - Stakeholder experience is less than seamless or personalized, potentially leading to a negative NPS for the product or solution                                                         |
|       | - Outreach to end constituents (e.g., via email, SMS) is not aligned to standards and is not documented or coordinated across business LoBs                                               |
|       | - Experiences are not fully multimodal in nature                                                                                                                                          |
|       | - No impact to TCO                                                                                                                                                                        |
|       | - Solution architecture and development process enables delivery of business value (less than 9 months), but iteration speed to assess, measure, and adjust experience is slow (>4 weeks)  |
|       | - Solution uses one or two common components to provide a consistent experience but could use more and has apparent experience deficiencies                                               |
|       | - Solution tags and tracks experience without using standard RUM and consumer journey tracking solutions                                                                                  |
| 3     | - Incremental experience design leading to a more personalized or seamless experience in the long-term, improving NPS in the long run                                                      |
|       | - Outreach to end constituents (e.g., via email, SMS) is aligned to standards but may not be fully documented or coordinated across all business LoBs                                      |
|       | - Experiences are designed to be multimodal but may not be optimized for all modalities (e.g., sub-par mobile experience)                                                                  |
|       | - Reduces TCO in less than 18 months                                                                                                                                                      |
|       | - Solution architecture and development process enables quick delivery of business value (less than 4 months), with moderate iteration speed (2-4 weeks)                                  |
|       | - Solution uses common components to provide a consistent experience but could use more, with minor experience deficiencies                                                               |
|       | - Solution tags and tracks most of the experience using enterprise standard RUM and consumer journey tracking solutions                                                                   |
| 4     | - Experience design leading to a more personalized or seamless experience in the short-term, improving NPS in the long run                                                                |
|       | - Outreach to end constituents (e.g., via email, SMS) is aligned to standards, fully documented, and coordinated for a given business                                                      |
|       | - Experiences are designed to be multimodal and optimized across modalities                                                                                                               |
|       | - Reduces TCO in the near future                                                                                                                                                          |
|       | - Solution architecture and development process enables quick delivery of business value (less than 2 months), with quick iteration speed (<2 weeks)                                       |
|       | - Solution uses common components to provide a consistent experience at every opportunity                                                                                                 |
|       | - Solution tags and tracks experience using enterprise standard RUM and consumer journey tracking solutions                                                                               |
| 5     | - Experience design leading to a highly personalized or seamless experience in the immediate term, significantly improving NPS in the short run                                            |
|       | - Outreach to end constituents (e.g., via email, SMS) is aligned to standards, fully documented, and coordinated across the enterprise                                                     |
|       | - Experiences are designed to be multimodal and optimized across modalities                                                                                                               |
|       | - Significantly reduces TCO in the near future                                                                                                                                           |
|       | - Solution architecture and development process enables quick turnaround (less than 1 month), with fast iteration speed (<3 days)                                                          |
|       | - Solution uses common components to provide a consistent experience at every opportunity                                                                                                 |
|       | - Solution tags and tracks experience using enterprise standard RUM and consumer journey tracking solutions      |

       ## Engineering Excellence

| Score | Criteria                                                                                                                                                                                                                                                                                                                                  |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | - **Engineering Culture**: Less than 40% of program engineers contribute meaningful code in GitHub over a 30-day period                                                                                                                                                                                                                   |
|       | - **Engineering Culture**: Less than 60% of eligible program source code repositories are in GitHub Enterprise Cloud                                                                                                                                                                                                                     |
|       | - **Performance & Accountability**: Less than 30% of applications have respective Vital Business Functions (VBF) identified, mapped, monitored with availability probes, and integrated into Enterprise Advisor for reporting                                                                                                             |
|       | - **Open Source Software and Technology**: <30% of technologies implemented are Preferred open source solutions                                                                                                                                                                                                                          |
|       | - Open Source technologies are not registered to the applications or compliant with licensing                                                                                                                                                                                                                                            |
|       | - Program team has not contributed to any open source projects leveraged in the solutions                                                                                                                                                                                                                                                |
| 2     | - **Engineering Culture**: 40-49% of program engineers contribute meaningful code in GitHub over a 30-day period                                                                                                                                                                                                                           |
|       | - **Engineering Culture**: 60% of eligible program source code repositories are in GitHub Enterprise Cloud                                                                                                                                                                                                                                |
|       | - **Performance & Accountability**: 30% or more applications have respective VBF identified, mapped, monitored with availability probes                                                                                                                                                                                                   |
|       | - **Open Source Software and Technology**: 30% of technologies implemented are Preferred open source solutions                                                                                                                                                                                                                            |
|       | - Open Source technologies are not registered to the applications or compliant with licensing                                                                                                                                                                                                                                             |
|       | - Program team has not contributed code, docs, or feedback to the open source projects leveraged in the solutions                                                                                                                                                                                                                         |
| 3     | - **Engineering Culture**: 50-54% of program engineers contribute meaningful code in GitHub over a 30-day period                                                                                                                                                                                                                           |
|       | - **Engineering Culture**: 70% of eligible program source code repositories are in GitHub Enterprise Cloud                                                                                                                                                                                                                                |
|       | - **Performance & Accountability**: 40% or more applications have respective VBF identified, mapped, monitored with availability probes, and integrated into Enterprise Advisor for reporting                                                                                                                                             |
|       | - **Open Source Software and Technology**: 50% of technologies implemented are Preferred open source solutions                                                                                                                                                                                                                            |
|       | - Open Source technologies are registered to the applications or program in Barista and compliant with licensing                                                                                                                                                                                                                          |
|       | - Program team has contributed code, docs, or feedback to one or more open source projects leveraged in the solutions                                                                                                                                                                                                                     |
| 4     | - **Engineering Culture**: 55-59% of program engineers contribute meaningful code in GitHub over a 30-day period                                                                                                                                                                                                                           |
|       | - **Engineering Culture**: 80% of eligible program source code repositories are in GitHub Enterprise Cloud                                                                                                                                                                                                                                |
|       | - **Performance & Accountability**: 50% or more applications have respective VBF identified, mapped, monitored with availability probes, and integrated into Enterprise Advisor for reporting                                                                                                                                             |
|       | - **Open Source Software and Technology**: 65% of technologies implemented are Preferred open source solutions                                                                                                                                                                                                                            |
|       | - Open Source technologies are registered to the applications and compliant with licensing                                                                                                                                                                                                                                                |
|       | - Aspects of the program are released as open source                                                                                                                                                                                                                                                                                      |
|       | - Program team has contributed code or docs to one or more open source projects leveraged in the solution(s)                                                                                                                                                                                                                              |
| 5     | - **Engineering Culture**: 60% of program engineers contribute meaningful code in GitHub over a 30-day period                                                                                                                                                                                                                              |
|       | - **Engineering Culture**: 90% of eligible program source code repositories are in GitHub Enterprise Cloud                                                                                                                                                                                                                                |
|       | - **Performance & Accountability**: 60% or more applications have respective VBF identified, mapped, monitored with availability probes                                                                                                                                                                                                  |
|       | - **Open Source Software and Technology**: 80% of technologies implemented are Preferred open source solutions                                                                                                                                                                                                                            |
|       | - Open Source technologies are registered to the applications and compliant with licensing                                                                                                                                                                                                                                                |
|       | - Aspects of the program are released as open source                                                                                                                                                                                                                                                                                      |
|       | - Program team has contributed code, docs, and feedback to one or more open source projects leveraged in the solution(s)                      |                                                                                                                                                                                            |
                                                                  |



