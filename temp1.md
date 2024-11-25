ad-hoc policy run
Requirement ID: REQ-072

Requirement Title: Ad-Hoc Policy Execution Trigger

Requirement Description: Provide users with the ability to trigger ad-hoc execution of Cloud Security Posture Management (CSPM) policies on-demand. This feature should allow users to manually initiate the execution of compliance checks or configuration assessments for specific cloud accounts, resource groups, or selected policies.

Requirement Rationale: Ad-hoc execution allows users to quickly validate changes or assess security posture without waiting for scheduled scans. This flexibility is particularly useful during incident investigations, validation of recent configuration changes, or when new policies are added to ensure immediate assessment.

Priority: 60 days

Requirement Dependency: REQ-010 (Centralized Policy Management)

Requirement ID: REQ-073

Requirement Title: Ad-Hoc Finding Validation

Requirement Description: Allow users to perform ad-hoc validation of specific findings detected by the CSPM platform. Users should be able to select a finding and trigger a validation process that rechecks the current state of the identified issue. The system should confirm whether the finding still exists, providing evidence such as updated screenshots, configuration snapshots, or HTTP request-response details.

Requirement Rationale: Ad-hoc validation of findings is essential for ensuring the accuracy of alerts and for verifying the remediation status. This capability helps reduce false positives and gives users confidence in the current state of their cloud environment by allowing immediate re-assessment of security issues.

Priority: 60 days

Requirement Dependency: REQ-003 (Continuous Configuration Assessment)


Near Realtime Configuration Evaluation
Toxic combination support for Azure

| Requirement ID | Requirement Title                     | Requirement Description                                                                                                                                                                                                                                               | Requirement Rationale                                                                                                                                                                                          | Priority  | Requirement Dependency           |
|----------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|----------------------------------|
| REQ-062        | Infrastructure-as-Code (IaC) Remediation Guidance | Provide Infrastructure-as-Code (IaC) snippets or examples in the remediation guidance for identified misconfigurations. These code snippets should demonstrate how to resolve issues directly within IaC frameworks like Terraform, CloudFormation, or Azure Resource Manager templates.  | Offering IaC remediation guidance enables development and DevOps teams to fix misconfigurations directly at the source code level, ensuring consistent and long-term fixes. It also encourages teams to integrate security earlier in the software development lifecycle. | 75 days   | N/A                              |
| REQ-063        | Policy Export Capability              | Enable users to export all CSPM policies, including both in-built and custom policies, along with all relevant details. The export should include policy names, descriptions, cloud provider, compliance mappings, severity levels, remediation actions, and any associated rules. The export format should be user-selectable (e.g., CSV, JSON, PDF) for easy integration with other systems or for audit purposes. | Exporting policies allows organizations to maintain documentation for compliance purposes, integrate policy information into other tools, and streamline collaboration across teams by sharing a complete set of security policies and configurations. | 60 days   | N/A                              |
| REQ-061        | Validation of Security Findings       | The CSPM platform must validate identified security findings by confirming their exposure with external verification. For instance, if a cloud storage bucket is flagged as publicly exposed, the platform should verify this by simulating an internet connection to confirm accessibility. Additionally, the platform must provide proof of validation, including screenshots, HTTP request and response details, or other forms of evidence. | Providing validation and proof for identified findings enhances the credibility of alerts, reduces false positives, and helps security teams prioritize actions with greater confidence. | 90 days   | N/A                              |
| REQ-069        | Natural Language Query Interface      | Provide an interface that allows users to create natural language-like queries to explore cloud resources, relationships, and security insights. The interface should be capable of understanding user input in a conversational manner and return results in graphical or tabular formats based on the user's preference. The results can include relationship visualizations, compliance status, access paths, or other relevant insights into the cloud environment. | Enabling users to query data using natural language makes it accessible to non-technical users, reducing the learning curve and increasing adoption. Presenting the results in multiple formats helps users understand complex data based on their individual needs. | 120 days  | REQ-064 (Cloud Resource Relationship Mapping) |
| REQ-070        | Network Reachability Analysis         | Provide the ability to analyze and visualize network reachability for all cloud resources and workloads. This feature should identify which resources and workloads are accessible over the internet or within the internal network and assess connectivity paths, such as open ports, security group rules, and firewall configurations. | Understanding network reachability is crucial for identifying potential attack surfaces and mitigating network-level risks. It enables security teams to proactively secure resources by limiting unnecessary exposure. | 90 days   | N/A                              |

# Requirements Table (REQ-091 through REQ-107)

| REQ ID | Category | Description | Rationale | Priority | Dependency | Est. Time (days) |
|--------|----------|-------------|-----------|----------|------------|------------------|
| REQ-097 | Compliance Posture Visualization | Provide a centralized dashboard that visually represents compliance status across all cloud accounts, subscriptions, and projects. | Enhances visibility into compliance posture across the organization. | High | REQ-012, REQ-037 | 12 |
| REQ-098 | Compliance Posture Visualization | Include all relevant compliance frameworks in a single visual representation. | Allows for comprehensive compliance monitoring. | High | REQ-097 | 10 |
| REQ-099 | Compliance Posture Visualization | Allow users to interact with compliance visuals to drill down into specific frameworks, controls, and affected resources. | Facilitates detailed analysis of compliance issues. | Medium | REQ-097 | 8 |
| REQ-100 | Compliance Posture Visualization | Enable filtering of compliance data by cloud provider, region, resource type, or specific compliance frameworks. | Provides tailored insights based on user needs. | Medium | REQ-097 | 7 |
| REQ-101 | Compliance Posture Visualization | Ensure visualizations reflect real-time compliance data, updating automatically with scans. | Keeps compliance information current for immediate action. | High | REQ-011, REQ-097 | 5 |
| REQ-102 | Compliance Posture Visualization | Map controls and requirements across different frameworks to identify common non-compliance areas. | Streamlines remediation efforts by addressing issues impacting multiple frameworks. | Medium | REQ-098 | 10 |
| REQ-103 | Compliance Posture Visualization | Integrate changes in compliance visuals with the alerting system for significant compliance shifts. | Ensures prompt notification of critical compliance issues. | High | REQ-019, REQ-097 | 6 |
| REQ-104 | Compliance Posture Visualization | Allow exporting of compliance visuals and underlying data for reports and presentations. | Supports communication with stakeholders and auditors. | Medium | REQ-039 | 5 |
| REQ-105 | Compliance Posture Visualization | Implement role-based access to control who can view or interact with compliance visualizations. | Protects sensitive compliance information. | High | REQ-059 | 7 |
| REQ-106 | Compliance Posture Visualization | Store historical compliance data to analyze trends over time. | Helps in measuring compliance improvements or deteriorations. | Medium | REQ-041 | 8 |
| REQ-107 | Compliance Posture Visualization | Highlight anomalies where certain accounts or resources significantly deviate from overall compliance posture. | Identifies potential issues requiring immediate attention. | Medium | REQ-097 | 7 |

REQ-006: Visualization of Resource Relationships

    •    Req Description:
    •    Provide visualization tools to map relationships and dependencies between resources.
    •    Req Rationale:
    •    Helps in understanding resource interconnections for better security analysis.
    •    Priority: Medium
    •    Req Dependency: REQ-001
    •    Estimated Time to Implement (in days): 12
REQ-009: Creation of Custom Compliance Policies

    •    Req Description:
    •    Allow users to create and enforce custom compliance rules based on organizational policies.
    •    Req Rationale:
    •    Supports specific compliance needs unique to the organization.
    •    Priority: High
    •    Req Dependency: None
    •    Estimated Time to Implement (in days): 10

REQ-019: Real-time Critical Issue Alerts

    •    Req Description:
    •    Provide immediate alerts (email, Microsoft Teams, ) for critical security issues and compliance violations.
    •    Req Rationale:
    •    Enables prompt response to significant security events.
    •    Priority: High
    •    Req Dependency: REQ-011, REQ-013
    •    Estimated Time to Implement (in days): 7

REQ-026: Contextual Links to Documentation

    •    Req Description:
    •    Include links to relevant documentation and best practices within remediation guidance.
    •    Req Rationale:
    •    Enhances understanding and adherence to best practices.
    •    Priority: Medium
    •    Req Dependency: REQ-025
    •    Estimated Time to Implement (in days): 5
Here's the information in a tabular format:


Sure! Below is the breakdown of the requirements **REQ-013**, **REQ-016**, and **REQ-017** in a markdown table format.

---

| **Requirement ID** | **Requirement Title**                    | **Requirement Description**                                                                                                                                                   | **Requirement Rationale**                                                                                                  | **Priority** | **Requirement Dependency** |
|--------------------|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|--------------|----------------------------|
| REQ-037            | Continuous Data Collection               | Continuously collect data on resource configurations, compliance statuses, risk scores, and remediation actions across all connected cloud accounts.                           | Ensures a comprehensive and up-to-date dataset for analysis, enabling accurate reporting and effective security monitoring. | 30 days      | None                       |
| REQ-038            | Secure Historical Data Storage           | Securely store historical security posture data for a configurable retention period, adhering to data privacy and compliance regulations.                                      | Allows organizations to perform long-term trend analysis, comply with audit requirements, and conduct forensic investigations when necessary. | 45 days      | REQ-037                    |
| REQ-039            | Trend Visualization Tools                | Provide visual tools such as charts, graphs, and heat maps to illustrate trends in security posture, compliance levels, and risk exposure over time.                           | Enhances data comprehension, allowing users to quickly identify patterns, anomalies, and areas of concern.                  | 60 days      | REQ-038                    |
| REQ-040            | Custom Time Frame Selection              | Allow users to select specific time ranges for analysis, including daily, weekly, monthly, quarterly, and yearly views.                                                        | Enables focused analysis on relevant periods, supporting better decision-making and reporting.                              | 60 days      | REQ-038                    |
| REQ-041            | Comparative Period Analysis              | Enable comparison between different time periods to assess changes in security posture and the effectiveness of security measures.                                            | Helps evaluate the impact of security initiatives and identify trends or recurring issues.                                  | 75 days      | REQ-040                    |
| REQ-042            | Data Export Functionality                | Provide options to export trend data and visualizations in various formats (e.g., PDF, CSV, PNG) for reporting and presentation purposes.                                      | Facilitates sharing insights with stakeholders and integrating data into external reports or tools.                        | 45 days      | REQ-039                    |
| REQ-043            | Anomaly Detection in Trends              | Identify and highlight significant deviations or anomalies in historical security data that may indicate emerging threats or compliance issues.                                | Allows for proactive response to unusual patterns that could signify security incidents or policy violations.               | 90 days      | REQ-038                    |
| REQ-044            | Integration with External Analytics Tools | Allow integration with external business intelligence and reporting tools (e.g., Tableau, Power BI) for advanced data analysis.                                               | Enables users to leverage existing analytics platforms for deeper insights and customized reporting.                        | 90 days      | REQ-037                    |
| REQ-045            | Simplified Navigation Structure          | Implement a clear and logical menu structure with easily accessible features and functions to reduce complexity.                                                               | Enhances user efficiency and reduces the learning curve, leading to increased productivity.                                 | 30 days      | None                       |
| REQ-046            | Consistent Design Language               | Use consistent icons, colors, and typography throughout the platform to maintain a cohesive look and feel.                                                                     | Improves user experience by reducing cognitive load and enhancing visual appeal.                                            | 30 days      | None                       |
| REQ-047            | Responsive User Interface Design         | Ensure the user interface is responsive and accessible on various devices, including desktops, tablets, and mobile phones.                                                    | Provides flexibility for users to access the platform from any device, increasing accessibility and convenience.            | 60 days      | None                       |
| REQ-048            | Comprehensive Default Dashboard          | Provide a default dashboard summarizing key metrics and alerts, offering an immediate overview of the security posture.                                                        | Allows users to quickly assess the overall status without navigating through multiple sections.                             | 45 days      | None                       |
| REQ-049            | Interactive User Assistance              | Incorporate tooltips, hover-over explanations, and guided tours to assist users in understanding platform features.                                                            | Reduces the need for extensive training and supports self-guided learning.                                                  | 60 days      | None                       |
| REQ-050            | Advanced Search and Filtering            | Include robust search and filtering options to quickly locate resources, policies, alerts, or reports based on various criteria.                                              | Enhances efficiency by enabling users to find specific information rapidly.                                                 | 45 days      | None                       |
| REQ-051            | User Personalization Settings            | Allow users to set preferences for language, theme (e.g., dark mode), and default views to customize their experience.                                                         | Increases user satisfaction by accommodating individual preferences.                                                        | 60 days      | None                       |
| REQ-052            | Accessibility Compliance Standards       | Design the user interface to comply with accessibility standards (e.g., WCAG 2.1) to support users with disabilities.                                                          | Ensures inclusivity and may be required for compliance with legal accessibility mandates.                                   | 90 days      | None                       |
| REQ-053            | Widget Library for Dashboards            | Provide a collection of widgets representing different data types like compliance status, risk scores, recent alerts, and remediation activities.                              | Enables users to tailor their dashboards with relevant information.                                                         | 60 days      | None                       |
| REQ-054            | Drag-and-Drop Dashboard Customization    | Enable users to add, remove, and rearrange dashboard widgets through a drag-and-drop interface.                                                                               | Simplifies dashboard customization, enhancing user engagement and satisfaction.                                             | 60 days      | REQ-053                    |
| REQ-055            | Widget Configuration Options             | Allow users to configure each widget's data sources, filters (e.g., by cloud provider, region, resource type), and visualization styles.                                      | Provides flexibility to display data in a way that best suits the user's role and needs.                                    | 75 days      | REQ-053                    |
| REQ-056            | Support Multiple Dashboards Per User     | Allow users to create and manage multiple dashboards to cater to different projects or focus areas.                                                                           | Helps users organize information effectively and switch contexts easily.                                                    | 75 days      | REQ-054                    |
| REQ-057            | Role-Based Dashboard Templates           | Offer pre-built dashboard templates tailored to common roles (e.g., Security Analyst, Compliance Officer, DevOps Engineer).                                                   | Accelerates onboarding and helps users quickly access relevant information.                                                 | 60 days      | None                       |
| REQ-058            | Dashboard Sharing Capabilities           | Enable users to share their custom dashboards with team members or export them for presentations.                                                                             | Facilitates collaboration and ensures consistent information dissemination among teams.                                     | 90 days      | REQ-056                    |
| REQ-059            | Real-Time Data Refresh                   | Ensure that dashboard data is refreshed in real-time or near real-time to provide the most current information.                                                                | Critical for timely decision-making and responsive security operations.                                                     | 60 days      | REQ-053                    |
| REQ-060            | Responsive Dashboard Design              | Design dashboards to be fully functional and viewable across various devices and screen sizes.                                                                                | Enhances accessibility and allows users to monitor security posture on-the-go.                                              | 75 days      | REQ-054                    |

---
