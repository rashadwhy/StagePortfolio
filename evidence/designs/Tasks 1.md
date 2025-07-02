
---

### 🧱 **Backend Infrastructure**

- Set up backend repo and project structure
    
- Configure environment variables
    
- Set up AWS DynamoDB
    
- Connect backend to DynamoDB
    
- Set up User mgmt (e.g., Cognito)

    
- Prepare deployment script or test deploy (AWS)
    

---

### 🔐 **Authentication & Session Management**

- Handle Microsoft Entra ID login
    
- Store access & refresh tokens
    
- Save session to `sessions` table
    
- Associate session with a user and company
    
- Add token refresh and session expiry middleware
    
- Protect routes with session-based access
    

---

### 👤 **User & Company Management**

- Create user on first login
    
- Store user role (`admin`, `user`)
    
- Create and store company data
    
- Associate users with companies
    

---

### 📊 **Graph API Integration & Data Storage**

- Fetch Microsoft Graph API data (users, sign-in logs)
    
- Create tables like `entra_users`, `entra_signins`
    
- Store fetched data scoped to `company_id`
    
- Expose simple read APIs (e.g., `/entra/users`)
    

---

### ✅ **Compliance Logic**

- Define schema for `compliance_controls`
    
- Write first compliance rule (e.g., MFA enabled for all users)
    
- Build logic to match stored data with compliance rules
    

---

### 🧪 **Testing & Validation**

- Test login → session → data fetch → storage flow
    
- Validate data accuracy and error handling
    

---

