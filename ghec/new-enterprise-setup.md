# Getting Started: GitHub Enterprise Cloud Setup

<details>
  <summary>Step 1: Accept the Invitation to Your New GitHub Enterprise Account</summary>
  <br>
  
  - This invitiation is sent to the email address you provided.

  <br>
</details>

<details>
  <summary>Step 2: Add a Backup Enterprise Owner to Your Enterprise Account</summary>
  <br>

  - **Go to:**
    - _Enterprise &rarr; People (left sidebar) &rarr; Administrators (left sidebar) &rarr; Invite admin (green button, top right)_

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

    - **Info:** When setting up SSO and SCIM, you will:
      - add the GitHub Enterprise Cloud - Organization app in the Microsoft Entra Admin Center and configure GitHub with SAML details from Microsoft Entra (such as your public certificate).
      - create a GitHub organization and invite members to join.
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

    - **Info:** When setting up SSO and SCIM, you will:
      - add the GitHub Enterprise Cloud - Organization app from Applications in Okta and configure GitHub with SAML details from Okta (such as your public certificate)
      - create a GitHub organization and invite members to join.
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

  - **Go to:**
    - _Organization &rarr; Settings &rarr; Authentication Security &rarr; Save Your Recovery Codes (under SAML Single Sign-On)_

  # <Line>

  - **GitHub Docs:**
    - [Downloading Your Organizations SAML SSO Recovery Codes](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-saml-single-sign-on-for-your-organization/downloading-your-organizations-saml-single-sign-on-recovery-codes)
    - [Accessing Your Organization if Your IdP is Unavailable](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-saml-single-sign-on-for-your-organization/accessing-your-organization-if-your-identity-provider-is-unavailable)
  
  <br>
</details>

<details>
  <summary>Step 5: Set up Team Sync (Optional)</summary>
  <br>
  
  - **Info:** Setting up Team Sync will allow you to sync IdP Groups to GitHub Teams. For example, teams can be granted Copilot licenses, and when a user is removed from the IdP group, they will automatically be removed from the GitHub Team and their Copilot license will be revoked.
  - **Go to:**
    - _Organization &rarr; Teams (tab at top) &rarr; New Team (green button on the right) &rarr; Identity Provider Group &rarr; Select group_

  # <Line>

  - **GitHub Docs:**
    - [Managing Team Sync for Your Organization](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-saml-single-sign-on-for-your-organization/managing-team-synchronization-for-your-organization)

  <br>
</details>

<details>
  <summary>Step 6: Add a Verified Domain to Your Organization (Optional)</summary>
  <br>

  - **Info:** Setting up a verified domain adds a verified badge to the company URL and email address displayed on your organization's public facing profile page. Verified domains are verified via your DNS provider. 
  - **To set a verified domain, go to:**
    - _Enterprise &rarr; Settings &rarr; Verified and Approved Domains &rarr Configure & Verify the Domain_ OR
    - _Organization → Settings → Security → Verified and Approved Domains &rarr; Configure & Verify the Domain_
  - **To set company URL and email address, go to:**
    - _Organization &rarr; Settings &rarr; General (landing page for Settings) &rarr; URL & Email fields_

  # <Line>

  - **GitHub Docs:**
    - [Verifying or Approving a Domain for Your Organization](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-organization-settings/verifying-or-approving-a-domain-for-your-organization)

  <br>
</details>

<details>
  <summary>Step 7: Restrict Email Notifications to Verified/Approved Domains (Optional)</summary>
  <br>

  - **Info:** Both verified and approvided domains can be used to restrict email notifications to specified domains for employees and contractors. Unlike verified domains, approved domains do not need to be verified via a DNS provider. 
  - **Go to:**
    - _Enterprise &rarr; Settings &rarr; Verified and Approved Domains &rarr select "Restrict email notifications to only verified and approved domains"_ OR
    - _Organization → Settings → Security → Verified and Approved Domains &rarr; select "Restrict email notifications to only verified and approved domains"_

  <br>
</details>

<details>
  <summary>Best Practices</summary>
  <br>
  
  - <details>
    <summary>Set up SSO at the organization level.</summary>
    <br>
    
    - _Note:_ Setting up SSO at the enterprise level can be done but is NOT recommended.
    - _Rationale:_
      - SCIM requires SSO and can only be configured at the organization level. It cannot be configured at the enterprise level.
      - Team Sync requires SCIM setup, so it can only be configured at the organization level as well.
      - Setting up SSO at the organization level makes it possible for companies with multiple engineering organizations that operate as part of distinct business entities or subsidiaries to be part of the same enterprise and governed by the same enterprise policies, while still maintaining distinct IdPs.
  
  - <details>
    <summary>When using Team Sync, do NOT use GitHub Team hierarchies.</summary>
    <br>
    
    - _Rationale:_
      - IdP groups will not sync to lower level GitHub teams.
    </details>
    
  - <details>
    <summary>If you have an IdP group with access to GitHub, create a single, all-purpose team in your GitHub organization to sync with this IdP group. Give the all-purpose GitHub team base permissions to all repositories.</summary>
    <br>
    
    - _Rationale:_
      - When new members are added to the IdP group, they will automatically be invited to the GitHub organization via the all-purpose GitHub team.
    </details>
    
  - <details>
    <summary>Create additional GitHub Teams to manage user roles across a GitHub organization. Sync these teams with IdP groups.</summary>
    <br>

    - _Rationale:_
      - Easily manage GitHub user permissions via your IdP.
    - **Example:**
      - The GitHub team, _A-Devs_, includes GitHub users in the IdP group, _Dev Team A_. These users have write roles on Repos 1, 2, and 3.
      - The GitHub team, _B-Devs_, includes GitHub users in the IdP group, _Dev Team B_. These users have write roles on Repos 3, 4, and 5.
      - The GitHub team, _PM-1_ includes GitHub users in IdP group, _Product-Managers-1_. These users have triage roles on Repos 1, 2, and 3.
      - The GitHub team, _PM-2_ includes GitHub users in IdP group, _Product-Managers-2_. These users have triage roles on Repos 3, 4, and 5.
    </details>
    
  - <details>
    <summary>Create custom organization and repository roles as needed.</summary>
    <br>
    
    - _Rationale:_
      - Some teams may want to give certain users certain maintainer or admin permissions without making the users full-fledged maintainers or admins.
    </details>
    
  <br>
</details>


