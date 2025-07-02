

---

### 🧱 Database Architecture (AWS DynamoDB)

#### 📚 Baseline Database (Public)

- **Schema:** `iso27001_baseline`
    
- **Tables:**
    
    - One table per ISO 27001:2022 chapter, including subsections/subcontrols.
        
    - Each table stores:
        
        - `section_id` (PK),
            
        - `title`,
            
        - `description`,
            
        - `control_type`,
            
        - `expected_evidence`, etc.
            

#### 🔐 Company Compliance Database (Private)

- **Schema:** `company_compliance`
    
- **Tables:**
    
    - Mirrors baseline schema (one table per ISO 27001 section)
        
    - Fields include:
        
        - `entry_id` (PK), `company_id` (FK),
            
        - `status` (`compliant`, `non-compliant`, `in-progress`, `not-applicable`),
            
        - `notes`, `evidence_links`, `last_updated`, etc.
            

#### 👥 User & Company Tables

- `companies`: `company_id` (UUID PK), `name`, `created_at`
    
- `company_admins`: `admin_id`, `company_id` (FK), `user_id` (FK)
    
- `company_users`: `user_id`, `company_id` (FK), `role`, `created_at`
    

> All relations use UUIDs for secure and unique identification.

---

### 🛠️ Comparison Logic

- **Automated Checks:**
    
    - Use Entra ID / Microsoft Graph API to pull live data.
        
    - Validate data against baseline controls (e.g., password policy, MFA).
        
- **Manual Submission:**
    
    - Companies provide evidence via API or dashboard.
        
    - Stored in `company_compliance` tables.
        

---
