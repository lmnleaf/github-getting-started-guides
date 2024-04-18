# Enabling SSO on an Existing GitHub Organization

<details>
  <summary>Step 1: Enable SSO & SCIM on the GitHub Organization. DO NOT require SSO Yet.</summary>
  <br>

  - <details>
    <summary>Microsoft Entra ID</summary>
    <br>

    - **Info:** When setting up SSO and SCIM, you will:
      - add the GitHub Enterprise Cloud - Organization app in the Microsoft Entra Admin Center and configure GitHub with SAML details from Microsoft Entra (such as your public certificate).
    - To set up SSO and SCIM, follow the Microsoft tutorials (see docs below line).
   
    # <Line>

    - **Microsoft Tutorials**
      - [Microsoft Entra SSO Integration with GitHub Cloud Organization](https://learn.microsoft.com/en-us/entra/identity/saas-apps/github-tutorial)
      - [Configure GitHub for Automatic User Provisioning (SCIM)](https://learn.microsoft.com/en-us/entra/identity/saas-apps/github-provisioning-tutorial)

    <br>
    </details> 
  - <details>
    <summary>Okta</summary>
    <br>

    - **Info:** When setting up SSO and SCIM, you will:
      - add the GitHub Enterprise Cloud - Organization app from Applications in Okta and configure GitHub with SAML details from Okta (such as your public certificate)
    - To set up SSO and SCIM, follow the GitHub and Okta tutorials (see docs below line).
   
    # <Line>

    - **Okta Tutorial**
      - [Okta SSO Integration with GitHub Cloud Organization](https://saml-doc.okta.com/SAML_Docs/How-to-Configure-SAML-2.0-for-Github-com.html)
    - **GitHub Docs**
      - [Configure SAML SSO & SCIM with Okta](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-saml-single-sign-on-for-your-organization/configuring-saml-single-sign-on-and-scim-using-okta)

    <br>
    </details>

  # <Line>
  
  - **Warning:** DO NOT click Require SAML SSO yet (clicking require will remove all your org members from the org).

  # <Line>
  
  - <details>
    <summary>Best Practices</summary>
    <br>
    
    - After enabling SSO:
      - Give a couple of your org members access to the GitHub app in your IdP.
      - Ensure the test org members can login to GitHub via the GitHub tile/app in your IdP.
    - **Info:**
      - Once your org members login with SSO, they will _always_ be prompted to login with SSO.
      - They will also need to configure their SSH keys and PATs for SSO access to the org (see below).
  
    <br>
    </details>
  
  <br>
</details>

<details>
  <summary>Step 2: Download SAML SSO Recovery Codes</summary>
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
  <summary>Step 3: Enable SSO for All Org Members and Service Accounts. DO NOT requires SSO yet.</summary>
  <br>

  - To enable SSO for all org members, make the GitHub app available to them in your IdP.
  - **Note:** Do this for your service accounts too.
  - Org members will be prompted to login to GitHub via SSO with a banner at the top of the page when they are in the organization namespace.

  <br>
</details>

<details>
  <summary>Step 4: Prepare to Require SSO Login</summary>
  <br>

  - After enabling SSO but BEFORE requring it, ask your org members to do three things:
    - Double check that the GitHub tile/app is available to them in their IdP account.
    - Click the GitHub tile/app OR link in the banner at the top of the page in the GitHub UI to sign in to GitHub via your IdP.
    - In their GitHub accounts, configure SSO for any SSH keys and PATs they use for work (see below for details).
  - Do this for your service accounts too.
  - **Info:** After your org members have completed these tasks, you can require SSO in your GitHub organization.
  - **Note:** Some GitHub Apps may require re-authorization with an active SAML session.

  # <Line>

  - **GitHub Docs:**
    - [Authorizing a PAT for SSO](https://docs.github.com/en/enterprise-cloud@latest/authentication/authenticating-with-saml-single-sign-on/authorizing-a-personal-access-token-for-use-with-saml-single-sign-on)
    - [Authorizing an SSH Key for SSO](https://docs.github.com/en/enterprise-cloud@latest/authentication/authenticating-with-saml-single-sign-on/authorizing-an-ssh-key-for-use-with-saml-single-sign-on)
    - [SAML & GitHub Apps](https://docs.github.com/en/enterprise-cloud@latest/apps/using-github-apps/saml-and-github-apps)

  <br>
</details>

<details>
  <summary>Step 5: Require SAML SSO Authentication</summary>
  <br>

  - **Go to:**
    - _Organization &rarr; Settings &rarr; Authentication security &rarr; SAML single sign-on &rarr; Require SAML SSO authentication_
  - **Info:** Once SSO is required:
    - Any org member who did not already sign in via your IdP will be removed from the organization. 
      - They will be able to rejoin the organization by logging into GitHub via their IdP account for a period of time (~3 months).
    - Any org member who signed in via your IdP but did not configure their SSH keys or PATs will not be able to push to any of the organization's repos or use the API to access org resources.
      - They can fix this by going to their personal account and configuring their SSH keys and PATs for SSO.
     
  # <Line>

  - **GitHub Docs:**
    - [Enforcing SSO](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-saml-single-sign-on-for-your-organization/enforcing-saml-single-sign-on-for-your-organization)

  <br>
</details>

<details>
  <summary>Step 6: Set up Team Sync (Optional)</summary>
  <br>
  
  - **Info:** Setting up Team Sync will allow you to sync IdP Groups to GitHub Teams.
  - **Go to:**
    - _Organization &rarr; Teams (tab at top) &rarr; New Team (green button on the right) &rarr; Identity Provider Group &rarr; Select group_

  # <Line>

  - **GitHub Docs:**
    - [Managing Team Sync for Your Organization](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-saml-single-sign-on-for-your-organization/managing-team-synchronization-for-your-organization)

  <br>
</details>
