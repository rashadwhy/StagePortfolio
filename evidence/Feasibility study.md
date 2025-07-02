---

---
---
Meeting notes:

Compare company GRC with baseline (forms format)
Be able to connect using SSO from MS, Google workspace, AWS
Be able to import company data from MS, Google workspace, AWS
Be able to parse company data into comparable format for usage with baseline.
Be able to hook onto existing MDM to manage.

Baseline:
GDPR
CCPA
ISO2700

How much relevant data does MS, Google workspace, AWS allow to be exported?
What data is relevant for the comparison?
Why is this data relevant for the comparison?

Which tier (MS, Google workspace, AWS) provides what data?


---

## **Feasibility Study: Comparing Company GRC with GDPR, CCPA, ISO27001**

### **Mission**

This study explores the feasibility of:

1. Comparing a company’s governance, risk, and compliance (GRC) framework with three key baselines: **GDPR**, **CCPA**, and **ISO27001**.
2. Utilizing data export capabilities from **Microsoft 365**, **Google Workspace**, and **AWS**.
3. Parsing the exported data into a format that allows it to be measured against the selected baselines.
4. Integrating Single Sign-On (SSO) functionality for seamless connectivity with MS, Google Workspace, and AWS.

---

### **Section 1: What Data Can Be Exported?**

#### **Microsoft (MS) 365**

- **Exportable Data:**
    - User activity logs, file metadata, email headers, compliance reports, security assessments, and data loss prevention (DLP) records.
- **How to Export:**
    - Tools like PowerShell, Microsoft Graph API, and the Compliance Center.
- **Tiers Required:**
    - Microsoft 365 **E3** and **E5**, as well as **Azure AD Premium**, provide access to advanced compliance and security tools.

#### **Google Workspace**

- **Exportable Data:**
    - User data, Drive file metadata, admin activity logs, audit logs, and security reports.
- **How to Export:**
    - Admin Console (Data Export), Google APIs, and BigQuery for advanced analytics.
- **Tiers Required:**
    - Business Plus and Enterprise Plus offer full compliance data access.

#### **AWS**

- **Exportable Data:**
    - IAM (Identity and Access Management) data, S3 bucket metadata, security findings (GuardDuty), and Config logs.
- **How to Export:**
    - Via AWS CLI, CloudTrail logs, and Management Console.
- **Tiers Required:**
    - AWS Business Support and Enterprise Support plans unlock comprehensive compliance data.

---

### **Section 2: Relevant Data for Comparison**

The focus is on extracting and using data that directly correlates with GDPR, CCPA, and ISO27001 requirements.

|**Data Category**|**Why It’s Important**|
|---|---|
|**User Identity Data**|Critical for GDPR and CCPA compliance. Helps in ensuring user access rights, consent, and data retention.|
|**Access Logs**|Essential for ISO27001 audit trails and GDPR/CCPA tracking of user interactions with sensitive data.|
|**File Metadata**|Tracks data sharing and storage practices. Useful for checking encryption and residency requirements.|
|**Security Reports**|Aligns with ISO27001’s security incident management and control verification.|
|**Configuration Logs**|Validates the configurations of systems against baseline requirements, such as encryption or access control.|

---

### **Section 3: Parsing Data into a Comparable Format**

Once exported, the data must be parsed into a structured, standardized format that aligns with the baselines. The process is outlined below:

1. **Data Import**:
    - Collect data via APIs (JSON, CSV formats) or manual file uploads.
    - Example: Access logs from AWS CloudTrail, user data from Google Workspace, and DLP records from MS.
2. **Data Normalization**:
    - Convert raw data into standardized categories:
        - Example: User access actions → Audit Logs (ISO27001).
        - Example: File sharing metadata → Consent and sharing analysis (GDPR/CCPA).
3. **Data Mapping**:
    - Map fields to specific requirements in GDPR, CCPA, and ISO27001. For example:
        - "Data sharing actions" → CCPA opt-out compliance.
        - "Encryption status" → ISO27001 technical controls.
4. **Export Parsed Data**:
    - Output the transformed data into a clear, comparison-ready format (CSV, dashboard, or report).

---

### **Section 4: Tier Comparison for MS, Google Workspace, and AWS**

|**Provider**|**Tier**|**Key Data Available**|
|---|---|---|
|**Microsoft (MS)**|Microsoft 365 E3/E5|User logs, email metadata, DLP reports, compliance insights, and file access logs.|
|**Google Workspace**|Enterprise Plus|File activity logs, audit logs, Drive metadata, admin reports, and compliance investigation data.|
|**AWS**|Enterprise Support|Security findings (GuardDuty, Config), IAM configurations, access logs, and resource usage metadata.|

---

### **Section 5: Relevance of Data for Comparison**

| **Baseline** | **Relevant Data Examples**                                                                                      | **Purpose of Data**                                                                            |     |
| ------------ | --------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | --- |
| **GDPR**     | User information (names, emails, file metadata, activity logs), encryption reports, data residency information. | Ensures compliance with consent, data access, and right-to-erasure requirements.               |     |
| **CCPA**     | File-sharing logs, opt-out actions, consumer requests, metadata tracking.                                       | Validates compliance with consumer rights, opt-out handling, and lawful data sharing.          |     |
| **ISO27001** | Security incident reports, access control logs, system configurations, backup verification, and audit trails.   | Aligns with ISO’s focus on maintaining a robust information security management system (ISMS). |     |
TODO: Acquire mock data from each service to decide on relevance.


---

### **Section 6: SSO Integration Feasibility**

All three providers (MS, Google Workspace, AWS) support SSO integration, which ensures secure and seamless authentication. Examples of integrations include:

- **Microsoft 365**: Azure AD SSO (SAML or OAuth2-based).
- **Google Workspace**: SSO through Admin Console (supports SAML, OIDC).
- **AWS**: SSO via AWS IAM Identity Center, integrated with MS Azure AD or Google Workspace.

SSO setup simplifies user authentication across systems while meeting ISO27001 and GDPR access control requirements.

---

### **Section 7: Compromises**

- **Data Availability by Tier**:
    - Advanced data (e.g., DLP or Config reports) may require higher subscription tiers (e.g., Microsoft E5, Google Workspace Enterprise Plus, AWS Enterprise).
- **Parsing Complexity**:
    - Normalizing logs and metadata from different providers into one format requires a solid parsing engine or custom-built scripts.
- **Compliance Gaps**:
    - The exported data may lack some granularity for full compliance evaluation (e.g., encryption details in free-tier logs).

---

### Continuing

1. **Relevance extraction & tier comparison**:
	- Acquire mock data from each service and tier to portray relevance per tier in each service.
2. **Evaluate Tools**:
    - Identify tools for data import and parsing (e.g., SIEM platforms, APIs, or custom parsers).
3. **Pilot Test**:
    - Export sample data from MS, Google, and AWS to test parsing and baseline mapping.
4. **SSO Setup**:
    - Implement SSO across platforms and test user authentication flow.
5. **Finalize Parsing Rules**:
    - Create detailed mapping between provider data fields and baseline requirements.

---
