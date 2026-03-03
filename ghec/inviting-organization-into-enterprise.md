# Inviting an Existing GitHub Organization into a GitHub Enterprise

<details>
  <summary>Step 1: Check the Number of Licenses on the Enterprise</summary>
  <br>
  
  - Ensure there are enough enterprise licenses available to cover any members of the org who aren't already members of the enterprise.
  - **Go to:**
    - _Enterprise &rarr; Billing & Licensing (tab at the top) &rarr; Licensing (left sidebar) &rarr; Licensing Enteprrise Cloud (first box)_

  # <Line>

  - **GitHub Docs:**
    - [Viewing License Usage](https://docs.github.com/en/enterprise-cloud@latest/billing/managing-your-license-for-github-enterprise/viewing-license-usage-for-github-enterprise)
  
  <br>
</details>

<details>
  <summary>Step 2: Check the Policies and Settings on the Enterprise</summary>
  <br>

  - Ensure that the policies and settings on the enterprise do NOT conflict with the policies and settings on the org.
  - **Info:**
    - Any settings or policies configured on the enterprise will override the settings and policies on the org.
    - If there are conflicts between enterprise and org settings, this can impact developer workflows, status checks, and CI/CD pipelines.
  - **Best Practice:** 
    - Although tedious, go through each enterprise policy and setting and compare it to the organization settings.
  - **Go to:**
    - _Enterprise &rarr;  Policies (tab at the top)_ AND _Enterprise &rarr; Settings (tab at the top)_ 
    - _Organization &rarr; Settings (tab at the top) &rarr; each setting (left sidebar)_
   
  # <Line>

  - **GitHub Docs:**
    - [Changes Made/Things to Check when Adding an Organization to an Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-organizations-in-your-enterprise/adding-organizations-to-your-enterprise#about-addition-of-organizations-to-your-enterprise-account)
    - [Enterprise Policies](https://docs.github.com/en/enterprise-cloud@latest/admin/policies/enforcing-policies-for-your-enterprise/about-enterprise-policies)

  <br>
</details>

<details>
  <summary>Step 3: Review Tips for Specific Use Cases</summary>
  <br>

  - <details>
    <summary>GitHub Actions (EXTRA IMPORTANT)</summary>
    <br>

    - Ensure the Actions settings at the enterprise level are not more restrictive than those on the org.
    - **EXTRA IMPORTANT:** Check the GITHUB_TOKEN permissions. 
      - Ensure that Workflow Permissions settings at the enterprise level match those on the org.
      - **Info:**
        - Workflow Permissions are permissions for the GITHUB_TOKEN.
        - By default the GITHUB_TOKEN is set to READ ONLY at the enterprise level but many orgs have it set to READ and WRITE.
    - **Go to:**
      - _Enterprise &rarr; Policies (tab at the top) &rarr; Actions &rarr; Workflow Permissions (bottom of the page)_
      - _Organization &rarr; Settings (tab at the top) &rarr; Actions (left side bar) &rarr; General &rarr; Workflow Permissions (bottom of the page)_
     
    <br>
    </details>

  - <details>
    <summary>GitHub Copilot</summary>
    <br>

    - Configure the Enterprise Copilot policy to allow all orgs access to Copilot OR after bringing the org into the enterprise, configure the Eneterprise Copilot policy to allow the specific org access to Copilot.
    - **Info:**
      - If the org is using Copilot Business or Copilot Enterprise and you do not do this, Copilot access for developers will be disrupted when the org is brought into the Enterprise.
    - **Go to:**
      - _Enterprise &rarr; Billing & Licensing (tab at the top) &rarr; Licensing (left sidebar) &rarr; scroll to Copilot (box in the middle) &rarr; Manage (button in box) &rarr; Organizations (tab in the middle of page) &rarr; search for organization &rarr; select license type (Business or Enterprise) &rarr; Grant Access_
     
    # <Line>

    - **GitHub Docs:**
      - [Granting User Access to GitHub Copilot in Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-access/grant-access), see section [Enabling Copilot for Organizations](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-access/grant-access#enabling-copilot-for-organizations)

    <br>
    </details>

  - <details>
    <summary>Beta Programs</summary>
    <br>

    - Tell your rep about any Beta enrollments for your org.
    - **Info:**
      - Beta programs need to be transferred to the enterprise for the org to continue to be enrolled, and your rep can do that for you.

    <br>
    </details>

  - <details>
    <summary>GitHub Marketplace Apps</summary>
    <br>

    - Contact the vendor to pay for any GitHub Marketplace Apps.
    - **Info:**
      - If your org is using any GitHub Marketplace apps that are billed to the org, the apps will no longer be billed to the org. Contact the vendor to pay them directly.

    <br>
    </details>

  - <details>
    <summary>Sponsoring Open Source Projects</summary>
    <br>

    - Sign up for sponsorships for open source projects.
    - **Info:**
      - If your org is sponsoring any open source projects, when it is moved to the enterprise, the existing sponsorships will be cancelled. To continue sponsoring them, you'll need to sign up again (see docs below for details).
     
    # <Line>

    - **GitHub Docs:**
      - [Paying for Sponsorships by Invoice](https://docs.github.com/en/enterprise-cloud@latest/sponsors/sponsoring-open-source-contributors/paying-for-github-sponsors-by-invoice)

    <br>
    </details>

  - <details>
    <summary>Enterprise with SSO Configured at Enterprise Level (Not Recommended)</summary>
    <br>
    
    - **Info:**
      - Org members will lose access to the organization until they login with SSO.
      - They will be prompted to login with SSO the first time they attempt to access organization resources after the org is moved into the enterprise. **Note:** They must already have an identity in your IdP with access to your GitHub enterprise.
      - Org members will need to configure SSH keys and PATs for SSO.
     
    # <Line>

    - **GitHub Docs:**
      - [Authenticating with SSO](https://docs.github.com/en/enterprise-cloud@latest/authentication/authenticating-with-saml-single-sign-on/about-authentication-with-saml-single-sign-on)
      - [Authorizing SSH Keys for SSO](https://docs.github.com/en/enterprise-cloud@latest/authentication/authenticating-with-saml-single-sign-on/authorizing-an-ssh-key-for-use-with-saml-single-sign-on)
      - [Authorizing PATs for SSO](https://docs.github.com/en/enterprise-cloud@latest/authentication/authenticating-with-saml-single-sign-on/authorizing-a-personal-access-token-for-use-with-saml-single-sign-on)

     <br> 
    </details>

  <br>
</details>

<details>
  <summary>Step 4: Invite the Organization to the Enterprise</summary>
  <br>

  - Invite the organization to join the enterprise.
  - **Info:**
    - When you invite an organization to join the enterprise, an email will be sent to the organization owner(s).
    - The organization owner will accept the invitation.
    - At that point, the organization will show as pending in the enterprise, so the enterprise admin can give final approval for the org to come into the enterprise.
  - **Got to:**
    - _Enterprise &rarr; Organizations (tab at the top) &rarr; Invite Organization (button top right) &rarr; search by org name_
   
  # <Line>

  - **GitHub Docs:**
    - [Adding Organizations to Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-organizations-in-your-enterprise/adding-organizations-to-your-enterprise#inviting-an-organization-to-join-your-enterprise-account), see section [Inviting an Existing Organization](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-organizations-in-your-enterprise/adding-organizations-to-your-enterprise#inviting-an-existing-organization)

  <br>
</details>
