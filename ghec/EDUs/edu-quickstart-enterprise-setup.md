# Quickstart: GitHub Enterprise Setup for EDUs

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
    - _Enterprise &rarr; People (left sidebar) &rarr; Administrators (left sidebar) &rarr; Invite Admin (top right)_

  # <Line>

  - **GitHub Docs:**
    - [Inviting People to Manage Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-users-in-your-enterprise/inviting-people-to-manage-your-enterprise)
 
  <br>
</details>

<details>
  <summary>Step 3: Set Up SAML Single Sign On (SSO)</summary>
  <br>

  - **Go to:**
    - _Enterprise &rarr; Settings (left sidebar) &rarr; Authentication Security &rarr; SAML Single Sign-on_

  # <Line>

  - **Best Practices**
    - Set up SSO at the Enterprise Level.
    - For more information, see [Best Practices for EDUs](https://github.com/lmnleaf/github-getting-started-guides/blob/main/ghec/EDUs/edu-best-practices.md).

  # <Line>

  - **GitHub Docs:**
    - [Configuring SAML Single Sign On for Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-iam/using-saml-for-enterprise-iam/configuring-saml-single-sign-on-for-your-enterprise)

  <br>
</details>

<details>
  <summary>Step 4: Download SAML SSO Recovery Codes</summary>
  <br>

  - **Go to:**
    - _Enterprise &rarr; Settings &rarr; Authentication Security &rarr; Save Your Recovery Codes (under SAML Single Sign-on)_

  # <Line>

  - **GitHub Docs:**
    - [Downloading Your Enterprise SAML SSO Recovery Codes](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-iam/managing-recovery-codes-for-your-enterprise/downloading-your-enterprise-accounts-single-sign-on-recovery-codes)
    - [Accessing Your Enterprise If Your IdP is Unavailable](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-iam/managing-recovery-codes-for-your-enterprise/accessing-your-enterprise-account-if-your-identity-provider-is-unavailable)
  
  <br>
</details>

<details>
  <summary>Step 5: Require SAML SSO Authentication</summary>
  <br>

  - **Go to:**
    - _Enterprise &rarr; Settings &rarr; Authentication Security &rarr; SAML Single Sign-On &rarr; Require SAML Authentication_
   
  # <Line>

  - **Info:**
    - Once SSO is set up and required:
      - Enterprise members must login via your IdP to access their organization's resources.
      - Enterprise members must configure their SSH keys and PATs for SSO with your enterprise.
      - Some GitHub Apps may require an active SSO session for authorization.

  # <Line>

  - **GitHub Docs:**
    - [Enforcing SSO](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-iam/using-saml-for-enterprise-iam/configuring-saml-single-sign-on-for-your-enterprise#enforcing-saml-single-sign-on-for-organizations-in-your-enterprise-account)
    - [Authorizing a PAT for SSO](https://docs.github.com/en/enterprise-cloud@latest/authentication/authenticating-with-saml-single-sign-on/authorizing-a-personal-access-token-for-use-with-saml-single-sign-on)
    - [Authorizing an SSH Key for SSO](https://docs.github.com/en/enterprise-cloud@latest/authentication/authenticating-with-saml-single-sign-on/authorizing-an-ssh-key-for-use-with-saml-single-sign-on)
    - [SAML & GitHub Apps](https://docs.github.com/en/enterprise-cloud@latest/apps/using-github-apps/saml-and-github-apps)
     
  <br>
</details>

<details>
  <summary>Step 6: Add a Verified Domain to Your Enterprise (Optional)</summary>
  <br>

  - **Go to:**
    - _Enterprise &rarr; Settings &rarr; Verified and Approved Domains &rarr; Configure & Verify the Domain_

  # <Line>

  - **Info:**
    - Verified domains are verified via your DNS provider. 
    - Setting up a verified domain adds a verified badge to the institution's URL and email address displayed on the public facing profile pages for all organizations in the Enterprise that set the institution's URL as the organization URL.

  # <Line>

  - **GitHub Docs:**
    - [Verifying or Approving a Domain for Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/configuring-settings/configuring-user-applications-for-your-enterprise/verifying-or-approving-a-domain-for-your-enterprise)

  <br>
</details>

<details>
  <summary>Step 7: Restrict Email Notifications to Verified/Approved Domains (Optional)</summary>
  <br>

  - **Go to:**
    - _Enterprise &rarr; Settings &rarr; Verified and Approved Domains &rarr; select Restrict email notifications to only verified and approved domains_

  # <Line>

  - **Info:**
    - Both verified and approvided domains can be used to restrict email notifications to specified domains for faculty, staff, and students. Unlike verified domains, approved domains do not need to be verified via a DNS provider.

  # <Line>

  - **GitHub Docs:**
    - [Restricting Email Notifications for Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/enforcing-policies/enforcing-policies-for-your-enterprise/restricting-email-notifications-for-your-enterprise)

  <br>
</details>

<details>
  <summary>Step 8: Set Policies & Settings on the Enterprise</summary>
  <br>

  - **Go to:**
    - _Enterprise &rarr; Policies &rarr; review each policy_
    - _Enterprise &rarr; Settings &rarr; review each setting_
   
  # <Line>

  - **Best Practices**
  - Allow organization admins to configure their own Policies and Settings for all but the paid features.
    - To do this, set policies to 'No Policy'.
  - To start, disable all paid features.
    - Paid features include Actions, GitHub Advanced Security (under Code Security), Codespaces, and Copilot.
    - Paid features can be enabled for selected organizations, and Cost Centers and Budgets can be created to limit spending and manage payment for these organizations.
  - Set the Actions Workflow Permissions to read and write.
    - To do this, go to: _Enterprise &rarr; Policies &rarr; Actions &rarr; Workflow Permissions (bottom of the page) &rarr; select Read and write permissions_
  - For additional information, see [Best Practices for EDUs](https://github.com/lmnleaf/github-getting-started-guides/blob/main/ghec/EDUs/edu-best-practices.md)

  # <Line>

  - **GitHub Docs:**
    - [Enterprise Policies](https://docs.github.com/en/enterprise-cloud@latest/admin/enforcing-policies/enforcing-policies-for-your-enterprise/about-enterprise-policies)

  <br>
</details>

<details>
  <summary>Step 9: Add an Organization to the Enterprise for Your GitHub Admin/Management Team</summary>
  <br>

  - **To invite an existing organization to join the Entperprise, go to:**
    - _Enterprise &rarr; Organizations &rarr; Invite Organization (upper right corner)_
  - **If the team needs a new organization, go to:**
    - _Enterprise &rarr; Organizations &rarr; New Organization (upper right corner)_

  # <Line>

  - **Info:**
    - This organization will be used by your GitHub Admin/Management team, i.e., a central IT team that will manage the GitHub Enterprise and administer GitHub as a Service for the rest of your EDU community.
    - This team may already have an existing GitHub organization. If so, that organization can be moved into the enterprise. Otherwise, you can create a new organization.

  # <Line>

  - **Best Practice**
    - Review this doc before inviting an organization into your enterprise: [Inviting an Existing GitHub Organization into a GitHub Enterprise](https://github.com/lmnleaf/github-getting-started-guides/blob/main/ghec/inviting-organization-into-enterprise.md)

  # <Line>

  - **GitHub Docs:**
    - [Adding Organizations to Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-organizations-in-your-enterprise/adding-organizations-to-your-enterprise)

  <br>
</details>

<details>
  <summary>Step 10: Implement GitHub as a Service for Your EDU Community </summary>
  <br>

  - **Info:**
    - Review the rest of this guide to learn more about managing organizations and members within your GitHub Enterprise account:
  - [Quickstart: GitHub as a Service](https://github.com/lmnleaf/github-getting-started-guides/blob/main/ghec/EDUs/edu-quickstart-enterprise-management.md)
  - [Overview: What's in a GitHub Enterprise?](https://github.com/lmnleaf/github-getting-started-guides/blob/main/ghec/EDUs/edu-enterprise-overview.md)
  - [GitHub Enterprise: Best Practices for EDUs](https://github.com/lmnleaf/github-getting-started-guides/blob/main/ghec/EDUs/edu-best-practices.md)

  <br>
</details>

