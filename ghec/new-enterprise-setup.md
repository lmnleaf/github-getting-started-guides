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
  
  - **Info:** Setting up Team Sync will allow you to sync IdP Groups to GitHub Teams. For example, teams can be granted Copilot licenses, and when a user is removed from the IdP group, they will automatically be removed from the GitHub Team and their Copilot license will be revoked.
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

<details>
  <summary>Best Practices</summary>
  <br>
  
  - **SSO & SCIM:** Set up SSO at the organization level.
    - _Note:_ Setting up SSO at the enterprise level can be done but is NOT recommended.
    - _Rationale_ 
      - SCIM requires SSO and can only be configured at the organization level.
        - SCIM is only available at the organization level. When SSO is setup at the enterprise level, SCIM cannot be configured.
      - Team Sync requires SCIM setup, so it can only be configured at the organization level.
        - Team Sync can only be configured when SSO & SCIM have been configured at the organization level.
      - Setting up SSO at the organization level makes it possible for companies with multiple engineering organizations that operate as part of distinct business entities or subsidiaries to be part of the same enterprise and governed by the same enterprise policies, while still maintaining distinct IdPs.

  <br>
  
  - **Teams & Team Sync:** When using Team Sync to sync between IdP Groups and GitHub Teams, do NOT use GitHub Team hierarchies.
    - _Rationale:_
      - IdP groups will not sync to lower level teams.
  - **Teams & Team Sync:** Create a single, all-purpose engineering/organization team in your GitHub organization.
    - _Rationale:_
      - When new members are added to the IdP group, they will automatically be invited to the organization via the all-purpose team.
    - Give this team base permissions to all repositories.
    - Sync this team with the IdP group that has access to the GitHub Enterprise Cloud Organization app.
  - **Teams & Team Sync:** Create additional GitHub Teams and corresponding IdP groups.
      - Use the teams to manage permissions for users across repositories.
      - _Rationale:_
        - User permissions in GitHub can be managed via the IdP.
      - **Example:**
        - The GitHub team, _A-Devs_, includes GitHub users in the IdP group, _Dev Team A_. These users have write roles on Repos 1, 2, and 3.
        - The GitHub team, _B-Devs_, includes GitHub users in the IdP group, _Dev Team B_. These users have write roles on Repos 3, 4, and 5.
        - The GitHub team, _PM-1_ includes GitHub users in IdP group, _Product-Managers-1_. These users have triage roles on Repos 1, 2, and 3.
        - The GitHub team, _PM-2_ includes GitHub users in IdP group, _Product-Managers-2_. These users have triage roles on Repos 3, 4, and 5.

 <br>
    
  - **Organization & Repo Roles:** Create custom organization and repository roles as needed.
    - _Rationale:_
      - Some teams may want to give certain users certain maintainer or admin permissions without making the users full-fledged maintainers or admins.
  
  <br>
</details>


