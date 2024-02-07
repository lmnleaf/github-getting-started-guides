# Getting Started: GitHub Enterprise Cloud Setup

<details>
  <summary>Step 1: Accept the Invitation to Your New GitHub Enterprise Account</summary>
  <br>
  
  - This invitiation is sent to the email address you provided.

  <br>
</details>

<details>
  <summary>Step 2: Add a Backup Enterprise Onwer to Your Enterprise Account</summary>
  <br>

  - **Go to:** _Enterprise &rarr; People (left sidebar) &rarr; Administrators (left sidebar) &rarr; Invite admin (green button, top right)_

  # <Line>

  - **GitHub Docs:**
    - [Inviting People to Manage Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-users-in-your-enterprise/inviting-people-to-manage-your-enterprise)
 
  <br>
</details>

<details>
  <summary>Step 3: Setup SSO and SCIM</summary>
  <br>

  - <details>
    <summary>Microsoft Entra ID</summary>
    <br>

    - To set up SSO and SCIM, add the GitHub Enterprise Cloud - Organization app in the Microsoft Entra Admin Center and configure GitHub with SAML details from Microsoft Entra (such as your public certificate).
    - As part of this process, you will create a GitHub organization and invite members to join.
    - To set up SSO and SCIM, follow the Microsoft tutorials (see docs below line).
   
    # <Line>

    - **Microsoft Tutorials**
      - [Microsoft Entra SSO Integration with GitHub Cloud Organization](https://learn.microsoft.com/en-us/entra/identity/saas-apps/github-tutorial)
      - [Configure GitHub for Automatic User Provisioning (SCIM)](https://learn.microsoft.com/en-us/entra/identity/saas-apps/github-provisioning-tutorial)
    - **GitHub Docs**
      - [Creating a New Organization](https://docs.github.com/en/enterprise-cloud@latest/organizations/collaborating-with-groups-in-organizations/creating-a-new-organization-from-scratch)

    <br>
    </details> 
  - <details>
    <summary>Okta</summary>
    <br>

    - To set up SSO and SCIM, add the GitHub Enterprise Cloud - Organization app from Applications in Okta and configure GitHub with SAML details from Okta (such as your public certificate).
    - As part of this process, you will create a GitHub organization and invite members to join.
    - To set up SSO and SCIM, follow the GitHub and Okta tutorials (see docs below line).
   
    # <Line>

    - **Okta Tutorial**
      - [Okta SSO Integration with GitHub Cloud Organization](https://saml-doc.okta.com/SAML_Docs/How-to-Configure-SAML-2.0-for-Github-com.html)
    - **GitHub Docs**
      - [Configure SAML SSO & SCIM with Okta](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-saml-single-sign-on-for-your-organization/configuring-saml-single-sign-on-and-scim-using-okta)

    <br>
    </details> 

  <br>
</details>

<details>
  <summary>Step 4: Download SAML SSO Recovery Codes</summary>
  <br>

  - **Go to:** _Organization &rarr; Settings &rarr; Authentication Security &rarr; Save Your Recover Codes (under SAML Single Sign-On)

  # <Line>

  - **GitHub Docs:**
    - [Downloading Your Organizations SAML SSO Recovery Codes](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-saml-single-sign-on-for-your-organization/downloading-your-organizations-saml-single-sign-on-recovery-codes)
    - [Accessing Your Organization if Your IdP is Unavailable](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-saml-single-sign-on-for-your-organization/accessing-your-organization-if-your-identity-provider-is-unavailable)
  
  <br>
</details>

<details>
  <summary>Step 5: Set up Team Sync (Optional)</summary>
  <br>
  
  - Setting up Team Sync will allow you to sync IdP Groups to GitHub Teams. For example, teams can be granted Copilot licenses, and when a user is removed from the IdP group, they will automatically be removed from the GitHub Team and their Copilot license will be revoked.
  - To add a GitHub Team and connect it to an existing IdP Group, **go to**: _Organization &rarr; Teams (tab at top) &rarr; New Team (green button to the right)_

  # <Line>

  - **GitHub Docs:**
    - [Managing Team Sync for Your Organization](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-saml-single-sign-on-for-your-organization/managing-team-synchronization-for-your-organization)

  <br>
</details>

<details>
  <summary>Step 6: Add Verified and Approved Domains (Optional)</summary>
  <br>

  <br>
</details>

<details>
  <summary>Step 7: Restrict Email Notifications to Verified/Approved Domains (Optional)</summary>
  <br>

  <br>
</details>


