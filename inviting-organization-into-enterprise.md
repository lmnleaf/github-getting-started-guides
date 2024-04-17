# Inviting an Existing GitHub Organization into a GitHub Enterprise

<details>
  <summary>Step 1: Check the Number of Licenses on the Enterprise</summary>
  <br>
  
  - Ensure there are enough enterprise licenses available in cover any members of the org who aren't already members of the enterprise.
  - **Go to:**
    - _Enterprise &rarr; People (left sidebar) &rarr; User Licenses Consumed (box at the top under Members heading)_

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
Any settings or policies configured on the enterprise will override the settings and policies on the org
If there are conflicts between enterprise and org settings, this could impact developer workflows, status checks, and CI/CD pipelines.
Recommendation: 
Although tedious, go through each enterprise policy and setting and compare it to the organization settings. 
To view the Enterprise policies and settings, go to: Enterprise >  Policies/Settings (left sidebar). 
To view the Organization settings, go to: Organization > Settings (tab at the top) > each setting (left sidebar).

  <br>
</details>

For orgs using Actions:
Check the Actions Policies and Settings
Ensure the Actions settings at the enterprise level are not more restrictive than those on the org.
EXTRA IMPORTANT: Check the GITHUB_TOKEN Permissions
Ensure that the GITHUB_TOKEN settings at the enterprise level match those on the org. 
Note: By default the GITHUB_TOKEN is set to READ ONLY at the enterprise level but many orgs have it set to READ and WRITE.
For orgs using Copilot:
Configure Copilot on the Enterprise (for orgs using Copilot already)
Configure the Enterprise Copilot policy to allow all orgs access to Copilot.
To do this, go to: Enterprise > Policies > Copilot > Manage organization access to GitHub Copilot > Allow for all organizations.
Note: If the org is using Copilot Business and you do not do this, license access can be disrupted when the org is brought into the Enterprise
For orgs using GitHub beta features:
Tell Us about Beta Enrollments
Let us know if your org is currently enrolled in any Beta programs. 
Beta programs need to be transferred to the enterprise for the org to continue to be enrolled, and we can do that for you.
For orgs using GitHub Marketplace Apps or sponsoring open source projects:
Contact the Vendor to Pay for GitHub Marketplace Apps (for orgs using Marketplace Apps)
If your org is using any GitHub Marketplace apps that are billed to the org, the apps will no longer be billed to the org. Contact the vendor to pay them directly.
Sign Up for Sponsorships (for orgs Sponsoring Open Source Projects)
If your org is sponsoring any open source projects, when it is moved to the enterprise, the existing sponsorships will be cancelled. 
To continue sponsoring them, you'll need to sign up again (see docs below for details).

Additional Resources:
Selected GitHub Docs:
Changes Made/Things to Check When Adding an Organization to an Enterprise
Enterprise Policies
How to Invite an Organization to Join Your Enterprise Account
Paying for Sponsorship by Invoice
Gist, created by one of my colleagues, that includes links to all the getting started docs: Teams to GHEC Upgrade.

Please reach out with any questions.
