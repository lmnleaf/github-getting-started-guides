## Managing Users in an Enterprise or Organization


### Enterprise

<details>
  <summary>Enterprise Owners & Billing Managers</summary>
  <br>

  - **Info:** Enterprise admins are either Owners or Billing Managers.
    - Owners have full administrative privileges on the enterprise.
    - Billing Managers have restricted access:
      - Can configure and view all billing related information.
      - Cannot access organizations or repositories.
      - Only type of user that does NOT consume an enterprise license.
  - **To invite admins, go to:**
    - _Enterprise &rarr; People (left sidebar) &rarr; Administrators &rarr; Invite admin &rarr; invite & set role_
  - **To view admins, go to:**
    - _Enterprise &rarr; People (left sidebar) &rarr; Members (landing page) &rarr; filter by role (top of list)_
   
  # <Line>

  - **GitHub Docs:**
    - [Inviting an Adminstrator to Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/user-management/managing-users-in-your-enterprise/inviting-people-to-manage-your-enterprise#inviting-an-enterprise-administrator-to-your-enterprise-account)
    - [Billing Managers](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-peoples-access-to-your-organization-with-roles/adding-a-billing-manager-to-your-organization)

  <br>
</details>



### Organization

<details>
  <summary>Organization Owners & Members</summary>
  <br>

  - **Info:** There are two primary roles for organization users: owner and member.
    - Additional custom organization roles can be created for users (see Custom Organization Roles).
  - **To invite organization owners/members, go to:**
    - _Organization &rarr; People (tab at the top) &rarr; Invite member_
  - **To view organization owners/members, go to:**
    - _Organization &rarr; People (tab at the top) &rarr; Members (filter near the top right)_
    
  # <Line>

  - **GitHub Docs:**
    - [Manage Organization Membership](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-membership-in-your-organization)
    - [Appointing Organization Owners](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-peoples-access-to-your-organization-with-roles/maintaining-ownership-continuity-for-your-organization#appointing-an-organization-owner)

  <br>
</details>

<details>
  <summary>Outside Collaborators</summary>
  <br>

  - **Info:**
    - There are two options for managing outside collaborators, i.e., 3rd party contractors, in a GitHub organization:
      - Invite 3rd party developers as Outside Collaborators.
      - Invite 3rd party developers as organization members.
    - When SSO is enabled and 3rd party developers are invited as
      - Outside Collaborators:
        - The 3rd party developers will not login with SSO but will have more restricted access to your organization overall based on the permissions you set for them.
        - Example: You can grant them access to only one or two repositories.
      - Members:
        - Add them as users in your IdP.
        - They will login with SSO like your regular employees.
        - If also using SCIM, setup a unique IdP group and corresponding GitHub team for the 3rd party developers, so their base level of access to the organization can be more restricted than that of your regular employees.
          - Example: Your regular employees could be in an IdP group that corresponds to a GitHub team that has write access to all repositories, while your contractors could be in a different IdP, corresponding to a GitHub team, that has read access to all repositories and write access to only one of them. GitHub teams can also be nested to provide additional access to selected organization members.
    - **Note:** Whether invited as outside collaborators or org members, 3rd party developers will consume an enterprise license.
    - **To invite outside collaborators, go to:**
      - _Organization &rarr; People (tab at the top) &rarr; Outside Collaborators (left sidebar) &rarr; Invite member &rarr; invite and set repo access_
     
  # <Line>

  - **GitHub Docs:**
    - [Managing Outside Collaborators](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-user-access-to-your-organizations-repositories/managing-outside-collaborators)
    - [Inviting Outside Collaborators](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-user-access-to-your-organizations-repositories/adding-outside-collaborators-to-repositories-in-your-organization)

  <br>
</details>

### Identifying/Tracking Organization Members

<details>
  <summary>Best Practices</summary>
  <br>

  - <details>
    <summary>Restrict Email Notifications to Verified/Approved Domains</summary>
    <br>

    - _Rationale:_
      - When email notifications are restricted to verified or approved domains:
        - Members and outside collaborators must add their work email addresses to their GitHub personal accounts to receive emails about the activity in your GitHub organization.
        - Member and outside collaborator email addresses will be visible along with their GitHub username in the People tab in your organization.
        - Member and outside collaborator email addresses will be available in exports and the REST API.
       
    # <Line>

    - **GitHub Docs:**
      [Adding a Verified or Approved Domain for Your Organization](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-organization-settings/verifying-or-approving-a-domain-for-your-organization)

    <br>
    </details>
  - <details>
    <summary>Set Metadata Restrictions using Repo Rulesets</summary>
    <br>

    - _Rationale:_
      - Metadata restrictions can be set to require users to have a committer email in a particular format, for example, ending in `workdomain.com`.
      - Email addresses appear in all commits accessed via the REST API.
     
    # <Line>

    - **GitHub Docs:**
      - [Managing Rulesets for an Organization](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-organization-settings/managing-rulesets-for-repositories-in-your-organization)
      - [Creating a Ruleset](https://docs.github.com/en/enterprise-cloud@latest/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository)
      - [Adding Metadata Restrictions](https://docs.github.com/en/enterprise-cloud@latest/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository#adding-metadata-restrictions)
    
    <br>
    </details>
  - <details>
    <summary>Review User Activity in the Audit Log</summary>
    <br>

    - _Rationale:_
      - View user activity in the Audit Log for an organization or enterprise.
      - When SSO is enabled, events include the users SSO identity.
      - _Note:_ The audit log is available at the organization and enterprise level, and it can be accessed from the UI or API, exported, or streamed to a SIEM (enterprise level only).
     
    # <Line>

    - **GitHub Docs:**
      - [Exporting Audit Log Activity](https://docs.github.com/en/enterprise-cloud@latest/admin/monitoring-activity-in-your-enterprise/reviewing-audit-logs-for-your-enterprise/exporting-audit-log-activity-for-your-enterprise)
      - [About the Audit Log](https://docs.github.com/en/enterprise-cloud@latest/admin/monitoring-activity-in-your-enterprise/reviewing-audit-logs-for-your-enterprise/about-the-audit-log-for-your-enterprise)
      - [Exporting Audit Log Activity for Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/monitoring-activity-in-your-enterprise/reviewing-audit-logs-for-your-enterprise/exporting-audit-log-activity-for-your-enterprise)
    - **GitHub Blog:**
      - [SAML Identity in the Audit Log](https://github.blog/changelog/2024-03-19-logging-saml-sso-and-scim-identity-data-in-audit-log-events-is-generally-available/)
    
    <br>
    </details>

  <br>
</details>
