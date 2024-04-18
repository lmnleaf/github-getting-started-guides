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
