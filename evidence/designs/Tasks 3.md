# Microsoft Graph API Feasibility Report  
**Scope:** Retrieve authentication method configurations (e.g., MFA) and Exchange/Outlook Safe Links status  
**Relevant Controls:**  
- ISMS-68 – Secure Authentication  
- ISMS-70 / ISO27001 – Protection Against Malware  

---

## 1. Authentication Methods (MFA Enabled) – ISMS-68

### ✅ Feasible via Microsoft Graph API

**Purpose:** Determine whether users have MFA enabled and view their authentication methods.

**Endpoints:**
- `GET /users/{user-id}/authentication/methods`  
  Retrieves all registered authentication methods per user.

- `GET /auditLogs/signIns`  
  Provides sign-in logs including `authenticationDetails` (indicates MFA usage).

**Required Permissions:**
- `User.Read.All`
- `AuditLog.Read.All`
- `Reports.Read.All` (for logs)

**Notes:**
- Admin privileges are required.
- Azure AD Sign-In logs must be enabled.
- MFA enablement status is not a direct flag; you infer it by analyzing registered methods or conditional access/successful sign-in types.

---

## 2. Exchange/Outlook Safe Links – ISMS-70 / ISO27001

### ❌ Not Feasible via Microsoft Graph API (as of now)

**Purpose:** Validate if Safe Links (part of Defender for Office 365) are enabled to protect users from malicious URLs.

**Access Method:**  
Currently retrievable **only via Exchange Online PowerShell** using:

```powershell
Connect-ExchangeOnline
Get-SafeLinksPolicy
Get-SafeLinksRule
```


# Other policies can be checked once the database is populated and I can filter on (automated = true).