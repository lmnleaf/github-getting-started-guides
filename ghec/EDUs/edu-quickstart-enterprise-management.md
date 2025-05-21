# Quickstart: GitHub as a Service

A guide to managing GitHub as a Service for your EDU community.

----

### Intro to GitHub as a Service

GitHub is a service that you'll provide to your educational community via your GitHub Enterprise account.

<details>
  <summary>Overview</summary>
  <br>
  
  - Groups within your EDU community will use organizations within your GitHub Enterprise account to collaborate on coding projects or develop code related curriculum.
- Although each educational institution is different, such groups often include:
  - Software Engineering or IT Teams
  - Departments (e.g., Computer Science or Chemistry)
  - Graduate Student Research Groups
  - Professors and TAs Teaching Classes
  - Extra Curricular Student Groups
 
  <br>
</details>

<details>
  <summary>Benefits of Providing GitHub as a Service</summary>
  <br>
  
  - Ensure all members of a GitHub organization belong to the EDU community.
  - Manage billing via a central account with Cost Centers & Budgets for each organization.
  - Implement global policies & settings as needed to ensure secure coding practices across your EDU coummunity.

  <br>
</details>

----

### What's involved in managing GitHub as a service?

With GitHub as a Service, a central IT team accepts and fulfills requests for GitHub organizations.

<details>
  <summary>What will my team need to do to manage GitHub as a service?</summary>
  <br>

  - Develop and maintain a process for accepting requests.
  - Create GitHub organizations within the enterprise account.
  - Invite requestors to join their organization as an organization admin.

  <br>
</details>

<details>
  <summary>What other tasks might my team do?</summary>
  <br>

  Depending on your institutional requirements, your team may also: 
  - Implement and maintain a process for approving requests for GitHub organizations.
  - Restrict organization access to particular GitHub features via enterprise level policies and settings.
  - Configure Cost Centers, Budgets, and billing details for requested organizations.
  - Remove inactive enterprise members from existing organizations.
  - Remove inactive organizations from the enterprise.
  - Set global policies that apply to all organizations within the enterprise.
  - Monitor enterprise activity via the enterprise Audit Log.
  - Monitor code security via the enterprise Code Security dashboards.
  - Stand up GitHub server instances for research groups with high compliance requirements.

  <br>
</details>

----

## Quickstart: Managing GitHub as a Service

Managing GitHub as a Service will require implementing the following steps or something similar. The drop downs below include information about each step as well as considerations and best practices for implementation.

<details>
  <summary>Step 1: Accept Requests for Organizations</summary>
  <br>

  - Create and implement a process via which members of your EDU community can request GitHub organizations in your enterprise.
  - Many EDUs use ServiceNow or other ticketing systems to accept and track requests.

  # <Line>

  - **Best Practices**

    - <details>
      <summary>Info to Collect in a Request</summary>
      <br>

      **Note:** This list is a recommendation. You may decide that you need to collect addtional or different information.

      |Info|Notes|Required to Set Up the Organization in GitHub|
      |----|-----|-----|
      |University Department||
      |Organization Admin Name||
      |Organization Admin Email|The organization admin will be invited to join the org via their email or GitHub handle (see Step 6).|:white_check_mark:
      |Organization Admin GitHub Handle|The organization admin will be invited to join the org via their email or GitHub handle (see Step 6).|
      |Reason the Organization is Needed||
      |Features Needed on the Org|Include a list of paid features that can be permitted or blocked with enterprise level settings. If permitted, payment methods and spending limits are set at the enterprise level. Examples of paid features: Advanced Security, Actions, GitHub Copilot, and Codespaces.
      |Organization Name||:white_check_mark:
      |New or Existing Organization|Some groups will already have an existing GitHub organization that they want to add to the enterprise. In such cases, the organization can be invited to join the enterprise. In all other cases, a new organization will need to be created.|
      |Compliance Requirements|Most EDUs allow organization admins to configure the settings on their organization to meet their compliance requirements.|
      |Whether a GitHub Server Instances is Needed to Meet the Compliance Requirements|Some EDUs have research groups that require high compliance environments and cannot use GitHub Enterprise Cloud. In such cases, research groups will set up a GitHub server instance that is hosted inside their high compliance environment.
      |Name & Email of Person Who Will Maintain the Server Instance (if one is needed)|Some EDUs have a central team that helps set up and maintain server instances when needed. Other EDUs provide the server license (available in the GitHub Enterprise) but leave it up to the research group to set up their own server instance.
      |Additional Organization Admin Emails|This is not required to create the organization, but best practice is to have multiple organization admins. The person who creates the organization will be added automatically as an organization admin.
      |Additional Organization Admin GitHub Handles|This is not required to create the organization, but best practice is to have multiple organization admins. The person who creates the organization will be added automatically as an organization admin.|
      |Member Emails|Some EDUs do not collect a list of organization members and instead allow organization admins to manage membership. This can be easier on the central IT team that manages GitHub as a Service. As long as SSO is configured at the enterprise level, only EDU community members will be able to join an organization, and enterprise admins can still remove inactive members from the organization.|

      <br>
      </details>

  <br>
</details>

<details>
  <summary>Step 2: Approve Requests for Organizations</summary>
  <br>

  - Create and implement a process for approving requests.

  # <Line>

  - **Best Practices**

    - Many EDUs use a ticket system such as ServiceNow to approve and track requests.

  <br>
</details>

<details>
  <summary>Step 3: Add Organizations to the Enterprise</summary>
  <br>

  - <details>
    <summary>Create a New Organization</summary>
    <br>

    - **Go to:**
      - _Enterprise &rarr; Organizations &rarr; New Organization (upper left)_
    - **Note:** Creating an organizatin must be done via the UI.
    
    <br>
    </details>
  - <details>
    <summary>Invite an Existing Organization</summary>
    <br>

    - Please follow this guide: [Inviting an Existing Organization Into an Enterprise](https://github.com/lmnleaf/github-getting-started-guides/blob/main/ghec/inviting-organization-into-enterprise.md)
    - **Note:** Creating an organizatin must be done via the UI.

    <br>
    </details>

  # <Line>
  
  - **GitHub Docs:**
    - [Adding Organizations to Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-organizations-in-your-enterprise/adding-organizations-to-your-enterprise)

  <br>
</details>

<details>
  <summary>Step 4: Configure Enterprise Level Policies for the Organizations</summary>
  <br>

  - **Go to:**
    - _Enterprise &rarr; Policies_

  # <Line>

  - **Best Practices**

    - <details>
      <summary>Policy Configuration</summary>
      <br>

      **Note:** This list is a recommendation. You may decide that you need to configure different or additional policies and settings.

      |Feature|Policy|Recommended Setting|Location|Notes|
      |-------|------|-------------------|--------|-----|
      |Actions|Enablement|Enable for Specific Organizations|_Enterprise &rarr; Policies &rarr; Actions (top of page just under the Policies heading)_|Enabling for specific organizations allows you to set payment methods and spending limits for organizations that are prepared to pay for Actions usage. All other organizations will not have access to Actions. Alternatively, enable Actions for all organizations and set spending limits to $0. If spending limits are not set, and the organization uses Actions, Actions usage will be billed to the enterprise.|
      |Actions|Workflow Permissions|Read and write permissions.|_Enterprise &rarr; Policies &rarr; Actions (scroll to the very bottom of the page)_|Since enterprise policies override organization policies, this should be set to read and write, to ensure that those organizations can use the [GITHUB_TOKEN](https://docs.github.com/en/enterprise-cloud@latest/actions/security-for-github-actions/security-guides/automatic-token-authentication) in their Actions workflows.|
      |Advanced Security|GitHub Advanced Security Availability|Allow for Selected Organizations|_Enterprise &rarr; Policies &rarr; Code Security (scroll all the way to very bottom of the page)_|Allowing for specific organizations allows you to pay for only those organizations that should have GitHub Advanced Security. **Note:** GitHub Advanced Security will be billed to the enterprise.|
      |GitHub Copilot|Copilot Enablement|Allow for Specific Organizations|_Enterprise &rarr; Policies &rarr; Copilot (mid page)_|Allowing for specific organizations allows you to set payment methods and spending limits for organizations that are prepared to pay for GitHub Copilot Business Licenses. All other organizations will not have access to Copilot Business licenses. Alternatively, enable Copilot for all organizations and set spending limits to $0. If spending limits are not set, and the organization uses Copilot Business, Copilot usage will be billed to the enterprise. **Note:** Copilot Pro licenses are free to verified teachers and students via their personal GitHub accounts. Reach out to your GitHub rep to learn more about [Copilot license types](https://github.com/features/copilot/plans).|
      |GitHub Copilot|Suggestions Matching Public Code (Duplication Detection Filter)|Blocked|_Enterprise &rarr; Policies &rarr; Copilot &rarr; Policies (tab toward the top of page) &rarr; Suggestions Matching Public Code (scroll down)_|Set this at the enterprise level for IP protection.|
      |Codespaces|Codespaces Enablement|Allow for Specific Oganizations|_Enterprise &rarr; Policies &rarr; Codespaces_|Allowing for specific organzations allows you to set payment methods and spending limits for organizations that are prepared to pay for Codespaces.|
      |Other Policies||No Policy|_Enterprise &rarr; Policies_ AND _Enterprise &rarr; Settings_|Setting "No policy" allows organization admins to set the policies for their organization, giving them maximum flexibility. **Note:** Please review all other policies and settings to ensure 'No Policy' is appropriate for your EDU community.|

      **Notes:**
      - If paid features are enabled for all organizations and spending limits are NOT set to $0, charges incurred will be billed to the enterprise. When enabled, Advanced Security is always billed to the enterprise.
      - After a set amount of free usage, Git LFS and Packages are also paid features.
      - Please review the GitHub docs for more information about GitHub Enterprise policies.
      - Please review the GitHub docs or talk to your GitHub rep for more information about billing.

      <br>
      </details>

  # <Line>

  - **GitHub Docs:**
    - [About Enterprise Policies](https://docs.github.com/en/enterprise-cloud@latest/admin/enforcing-policies/enforcing-policies-for-your-enterprise/about-enterprise-policies)
    - [GitHub Billing](https://docs.github.com/en/enterprise-cloud@latest/billing)

  <br>
</details>

<details>
  <summary>Step 5: Create Cost Centers & Budgets for Organizations</summary>
  <br>

  - **To add a Cost Center, go to:**
    - _Enterprise &rarr; Billing and Licensing &rarr; Cost Centers_
  - **To add a Budget for the Cost Center, go to:**
    - _Enterprise &rarr; Billing and Licensing &rarr; Budgets and Alerts_

  # <Line>

  - **Additional Info**

    - Cost Centers
      - Cost Centers are used to manage payment methods and budgets organizations, reposotiries, or users.
      - Cost Centers can be configured with an Azure Subscription ID for payment.

    - Budgets
      - Budgets are used to set spending limits and alert people when spending is approaching the limit.
      - Budgets are assigned to the enterprise, organization, repository, or Cost Center.

  # <Line>

  - **Best Practices**

    - <details>
      <summary>Cost Center & Budget Configuration</summary>
      <br>

      - Configure a Cost Center for any organization that will use paid features.
      - Configure a Budget for any organization that will use paid features.
      - Work with the organization admin to determine:
        - who should be alerted when the organization is reaching it's spending limits.
        - whether usage should be stopped when the spending limit is reached.
      - **Note:** Cost Centers are required if setting an organization specific payment method. If a Budget is set and associated with an organization rather than a Cost Center, any usage the organization incurs will be billed to the Enterprise.

      <br>
      </details>

  # <Line>

  - **GitHub Docs:**
    - [Cost Centers: Charging Business Units](https://docs.github.com/en/enterprise-cloud@latest/billing/using-the-new-billing-platform/charging-business-units)
    - [Budgets: Prevent Overspending](https://docs.github.com/en/enterprise-cloud@latest/billing/using-the-new-billing-platform/preventing-overspending)
    - [GitHub Billing](https://docs.github.com/en/enterprise-cloud@latest/billing)

  <br>
</details>

<details>
  <summary>Step 6: Invite Organization Admins to Join Their Organizations</summary>
  <br>

  - **To invite org admins from the GitHub UI, go to:**
    _ Enterprise &rarr; Organizations &rarr; Select the Organization &rarr; People &rarr; Invite Member_
    - Once the admin accepts their invitation, update their role by going to _Organization &rarr; People &rarr; Three Dots (right) &rarr; Change Role &rarr; Select Owner_
  - **To invite org admins via the GitHub API, see these docs:**
    - [Create an Organization Invitiation](https://docs.github.com/en/enterprise-cloud@latest/rest/orgs/members?apiVersion=2022-11-28#create-an-organization-invitation) (also see Best Practices below)

  # <Line>

  - **Additional Info**

    - Organization admins and members can be invited to join an organization via the UI or API.
      - When inviting users via the API, you can specify their role in the request.
    - Once invited, organization admins and members will receive an email.
    - When users accept the invitation:
      - If they already have a GitHub personal account:
        - They'll log into that account and then into the Enterprise with SSO to access the organization resources.
      - If they do NOT have a GitHub personal account or are NOT logged in:
        - They'll be prompted to login or create an account.
        - Once they've created the account, they'll log into the Enterprise with SSO to access the organization resources.

  # <Line>

  - **Best Practices**

    - <details>
      <summary>Automated Invites</summary>
      <br>

      - Use GitHub Actions or another automation platform to automate the process of inviting organization admins.
      - If managing member invitations on behalf of the org admin, automate this process as well.
      - See [GitHub Terraform Provider](https://registry.terraform.io/providers/integrations/github/latest/docs) to use or as an example.

      <br>
      </details>

  <br>
</details>

<details>
  <summary>Step 7: Monitor & Maintain Enterprise Organizations and Members</summary>
  <br>

  - Review the Audit Log
    - **To view the Enterprise Audit Log, go to:**
      - _Enterprise &rarr; Audit Log_
    - **To set up Audit Log Streaming, go to:**
      - _Enterprise &rarr; Audit Log &rarr; Log Streaming_
    - **To access the Audit Log via the API, see these docs:**
      - [Enterprise Audit Logs](https://docs.github.com/en/enterprise-cloud@latest/rest/enterprise-admin/audit-log?apiVersion=2022-11-28)
     
  - Remove Inactive Members from Organizations
    - **To remove inactive members from organizations via the API, see these docs:**
      - [Export a List of Organization Members](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-membership-in-your-organization/exporting-member-information-for-your-organization)
      - [Export Dormant Enterprise Users](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-users-in-your-enterprise/managing-dormant-users#downloading-the-dormant-users-report-from-your-enterprise-account)
      - [Remove an Organization Member](https://docs.github.com/en/enterprise-cloud@latest/rest/orgs/members?apiVersion=2022-11-28#remove-an-organization-member)

  # <Line>

  - **Best Practices**

    - <details>
      <summary>Audit Log Streaming & Automated Member Management</summary>
      <br>

      - Set up audit log streaming to and alerting from a SIEM to monitor GitHub usage across your enterprise.
      - Set up an automated process to remove inactive members from your enterprise.
        - Remove members after 6-12 months of inactivity.
        -  Example Action for Removing Inactive Members: [Cleaning Up Organization Members](https://github.com/lmnleaf/clean-up-organization-members)
      - Remove inactive organization from your enterprise.
        - Remove organizations after 12-18 months of inactivity.
        - Organizations may be inactive when they do not have any members other than admins and/or do not contain any repos.
        - Check with the org admins to ensure the organization can be removed.

      <br>
      </details>

  # <Line>

  - **GitHub Docs:**
    - [Monitoring Activity in Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/monitoring-activity-in-your-enterprise)
    - [Streaming the Audit Log for Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/monitoring-activity-in-your-enterprise/reviewing-audit-logs-for-your-enterprise/streaming-the-audit-log-for-your-enterprise)
    - [Exporting Member Information for Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-users-in-your-enterprise/exporting-membership-information-for-your-enterprise)
    - [Exporting Member Information for Your Organization](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-membership-in-your-organization/exporting-member-information-for-your-organization)

  <br>
</details>

**Note:** If you are setting up a dual presence, with both standard and Enterprise Managed Users (EMU) enterprises, please reach out to your GitHub rep for additional information about EMUs.
