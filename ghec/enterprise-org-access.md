# Best Practices: Organization Access in an Enterprise

Follow these best practices to limit access to an organization's resources within an Enterprise.

<details>
  <summary>Restrict Repository Access & Member Privileges</summary>
  <br>

  **Repository Policies (Preview)**

  - **Go to:**
    - _Organization &rarr; Settings &rarr; Policies &rarr; Repository_
    - **Note:** Repository Policies are in preview right now.

  <br>

  - **Selections:**
    - Target Repositories
      - Target
        - :white_check_mark: All Repositories
    - Repository Policies 
      - Restrict Visibility
        - :x: Public (do NOT allow)
        - :x: Internal (do NOT allow)
        - :white_check_mark: Private
      - :white_check_mark: Restrict Transfers

  <br>

  **Member Privileges**

  - **Go to:**
    - _Organization &rarr; Setings &rarr; Member Privileges_

  <br>
  
  - **Selections:**
    - Member Privileges
      - Base Permissions
        - :white_check_mark: No Permissions OR Read
      - Repository Creation
        - :x: Public (do NOT allow)
        - :white_check_mark: Private
        - :x: Internal (do NOT allow)
      - Repository Forking
        - :x: Allow forking of private and internal repositories (do NOT allow)
      - Outside Collaborators
        - :x: Allow repository administrators to invite outside collaborators (do NOT allow)
      - Pages Creation
        - :x: Public (do NOT allow)
        - :white_check_mark: Private
      - Integration Access Requests
        - :x: Allow integration requests from outside collaborators (do NOT allow)
    - Admin Repository Permissions
      - Repository Visibility Change
        - :x: Allow members to change repository visibility (do NOT allow)
      - Repository Deletion & Transfer
        - :x: Allow members to delete or transfer repositories (do NOT allow)

  <br>
</details>

<details>
  <summary>Configure Authentication Security (including SSO)</summary>
  <br>

  - **Go to:**
    - _Settings &rarr; Authentication Security_

  <br>
  
  - **Selections:**
    - Two-Factor Authentication
      - :white_check_mark: Require two-factor authentication
    - SAML Single Sign-On
      - :white_check_mark: Enable SAML Authentication
      - :white_check_mark: Enforce SAML Authentication
    - SSH Certificate Authorities (Optional)
      - :white_check_mark: Require SSH Certificates
    - IP Allow List
      - :white_check_mark: Enable IP Allowlist

  <br>
</details>

<details>
  <summary>Manage Email Notifications</summary>
  <br>

  - **Go to:**
    - _Organization &rarr; Settings &rarr; Verified and Approved Domains_

  <br>

  - **Selections:**
    - Verified & Approved Domain
      :white_check_mark: Add a Domain
    - Notification Preferences
      - :white_check_mark: Restrict email notifications to only approved or verified domains

  <br>
</details>

<details>
  <summary>Review Audit Log</summary>
  <br>

  - **Go to:**
    - _Organization &rarr; Settings &rarr; Logs &rarr; Audit Log &rarr; Settings (tabs toward the top of the page)_

  <br>
  
  - **Selections:**
    - Settings (tab under page title)
      - :white_check_mark: Enable source IP disclosure
    - Events
      - :white_check_mark: Export Git Events
      - :white_check_mark: Export (other events)
    - **Note:** Audit Log streaming to a SIEM is available at the Enterprise level.
  
  </br>
</details>
