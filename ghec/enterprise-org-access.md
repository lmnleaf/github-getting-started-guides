# Best Practices: Organization Access in an Enterprise

Follow these best practices to lock down an organizatin within an Enterprise.

<details>
  <summary>Restrict Repository Access & Member Privileges</summary>
  <br>

**Repository Policies**

  - **Go to:**
    - _Organization &rarr; Settings &rarr; Policies &rarr; Repository_
    - **Note:** Repository Policies are in preview right now.
  _ **Selections:**
    - Target Repositories &rarr; All Repositories
    - Repository Policies &rarr;
      - Restrict Visibility
        - Private
        - Do NOT enable Public or Internal
      - Restrict Deletions
      - Restrict Transfers

**Member Privileges**

  - **Go to:**
    - _Organization &rarr; Setings &rarr; Member Privileges_
  - **Selections:**
    - Member Privileges
      - Base Permissions &rarr; No Permissions
      - Repository Creation &rarr; Private
      - Repository Forking &rarr; Uncheck (Do NOT allow)
      - Outside Collaborators &rarr; Uncheck (Do NOT allow)
      - Pages Creation &rarr; Private
    - Admin Repository Permissions
      - Repository Visibility Change &rarr; Uncheck (Do NOT allow)
      - Repository Deletion & Transfer &rarr; Uncheck (Do NOT allow)
    - Team Creation Rules
      - Team Creation Rules &rarr; Allow Members to Create Teams &rarr; Uncheck (Do NOT allow)

  <br>
</details>

<details>
  <summary>Set Up Single Sign On</summary>
  <br>

  **Single Sign On**

  - **Go to:**
    - _Settings &rarr; Authentication Security &rarr; SAML Single Sign-On_
  - **Selections:**
    - Enable SAML Authentication
    - Enforce SAML Authentication

  <br>
</details>

<details>
  <summary>Manage Email Notifications</summary>
  <br>

  **Verfied & Approvied Domains**

  - **Go to:**
    - _Organization &rarr; Settings &rarr; Verified and Approved Domains_
  - **Selections:**
    - Verified & Approved Domains &rarr; Add a Domain
    - Notification Preferences &rarr; Restrict Email Notifications to Only Approved or Verified Domains

  <br>
</details>

<details>
  <summary>Review Audit Log</summary>
  <br>

  **Audit Log**

  - **Go to:**
    - _Organization &rarr; Settings &rarr; Logs &rarr; Audit Log &rarr; Settings (tabs toward the top of the page)_
  - **Selections:**
    - Enable Source IP Discolsure
  - **Export Audit Log**
    - Events (tab toward the top of the page) &rarr; Export Git Events
  - **Note:** Audit Log streaming is available at the Enterprise level.
  
  </br>
</details>
