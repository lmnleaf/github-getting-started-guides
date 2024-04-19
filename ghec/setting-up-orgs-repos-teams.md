# Best Practices: Enterprises, Organizations, Repositories, and Teams

### Enterprise

#### Info:
- The enterprise account provides controls and insight into everything in your company's GitHub account.
- <details>
  <summary>What's in an Enterprise Account</summary>
  <br>
  
  - Organizations
  - Policies and Settings for all organizations
  - Security insights for customers using Advanced Security
  - GitHub Connect (connects Server instances to Cloud instances for customers using GitHub Enterprise Server in addition to GitHub Enterprise Cloud)
  - Audit Log
  - GitHub Compliance documentation
  
  <br>
  </details>


# <Line>

#### Best Practices:

- <details>
  <summary>Set up Audit Log streaming to a SIEM.</summary>
  <br>
  
  - _Rationale:_
    - The GitHub Audit Log allows you to view user activity, including Git activity.
    - Audit Log streaming allows you to:
      - track user activity over time.
      - retain your audit log beyond the 3-6 months it is available from GitHub.
      - set alerts for certain activities.
     
  <br>

  - **To view the Enterprise Audit Log and set up streaming, go to:**
    - _Enterprise &rarr; Settings (left sidebar) &rarr; Audit Log &rarr; Events/Log Streaming (tabs under the Audit Log heading)_

  <br>
  
  - **GitHub Docs:**
    - [Streaming Audit Log](https://docs.github.com/en/enterprise-cloud@latest/admin/monitoring-activity-in-your-enterprise/reviewing-audit-logs-for-your-enterprise/streaming-the-audit-log-for-your-enterprise)
    - [Setting Up Audit Log Streaming & Supported SIEMs](https://docs.github.com/en/enterprise-cloud@latest/admin/monitoring-activity-in-your-enterprise/reviewing-audit-logs-for-your-enterprise/streaming-the-audit-log-for-your-enterprise#setting-up-audit-log-streaming)

  <br>
  </details>

- <details>
  <summary>Configure settings and policies that cannot or should not be configured by org owners.</summary>
  <br>
  
  - _Rationale:_
    - Some policies must be configured at the enterprise level.
      - Examples:
        - Actions Workflow Permissions (default to Read on the enterprise).
        - Copilot Access Permissions (Note: Copilot licenses are assigned at the org level, but org level access must be granted at the enterprise level).
       
  <br>

  - **To configure Settings and Policies, go to:**
    - _Enterprise &rarr; Policies or Settings (left sidebar)_
       
  <br>
  
  - **GitHub Docs:**
    - [Setting Policies for Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/policies)

  <br>
  </details>

----

### Organizations

#### Info:
- Enterprises can have one or more organizations.
- Each organization can have a distinct set of members.
- Each organization has it's own repositories.
- <details>
  <summary>What's in an Organization</summary>
  <br>

  - Repositories
  - Copilot access
  - Projects
  - Packages
  - Discussions
  - Teams
  - Security & org level insights
  - Audit Log

  <br>
  </details>

- **Note:** Distinct organizations are NOT needed to limit repository access. (See Best Practices below for more info).

# <Line>

#### Best Practices:

- <details>
  <summary>Create ONE organization.</summary>
  <br>

  - <details>
    <summary>Why create only one organization?</summary>
    <br>
  
    - _Rationale:_
      - SCIM is only available at the organization level.
        - Using SCIM across multiple organizations requires unique SSO & SCIM configurations on each organization.
      - Individual organizations are intended for users who work together, i.e., whole engineering teams and their cross functional counterparts.
      - Access to and permissions on repositories are managed with base member permissions and GitHub Teams.

     <br>
    </details>

  - <details>
    <summary>When does it make sense to create more than one organization?</summary>
    <br>
  
    - Two main uses cases:
      - Companies with distinct business entitities who's engineering teams operate indepently.
        - Example:
          - Company A acquires Company B.
          - Each company has a unique product line and different engineerint teams.
          - The engineering teams rarely interact or work together on the same project.
          - Deploys are separate.
      - Companies with divisions/departments that operate independently.
        - Example:
          - Company A has an engineering team that works on their primary product.
          - They also have a small R&D team that works on highly sensitive code.
          - The two teams rarely interact or work together on the same project.
          - None of the R&D conversations should ever be visible to the engineering team or their cross functional counterparts.
       
    <br>

    - _Note:_ If there were an occasion for subsidiaries or departments to collaborate, one of the organizations can create internal repositories. (See the Repositories section for more info).

    <br>
    </details>

  <br>

  - **To create an organization, go to:**
    - _Enterprise &rarr; Organizations (left sidebar) &rarr; New organization (button upper right)_

  <br>
     
  - **GitHub Docs:**
      - [Creating a New Organization](https://docs.github.com/en/enterprise-cloud@latest/organizations/collaborating-with-groups-in-organizations/creating-a-new-organization-from-scratch)

  <br>
  </details>

- <details>
  <summary>Set base user permissions to Read.</summary>
  <br>

  - <details>
    <summary>Why set permissions to Read?</summary>
    <br>
  
    - _Rationale:_
      - Providing Read access to your repositories facilitates learning and development.
        - Developers tend to be curious and learn from each other. Fostering this curiousity and learning leads to a stronger dev team, with multiple devs capable of taking on and troubleshooting multiple different types of projects.

    <br>
    </details>

  - <details>
    <summary>When should base user permissions be set to No Permissions.</summary>
    <br>
 
    - If your organization includes some repositories that are particularly sensitive and should not be viewed by all devs, you can set the base permissions to No Permissions. This will ensure that no one has read access to some repositories unless explicitly granted that access.
 
    <br>
    </details>

    <br>

    - **To set base user permissions, go to:**
      - _Enterprise &rarr; Settings &rarr; Repositories (landing page) &rarr; Base Permissions (top of the page)_ OR
      - _Organization &rarr; Settings &rarr; Member Permissions (left sidebar) &rarr; Base Permissions (top of the page)_
     
    <br>

    - **GitHub Docs:**
      - [Setting Base User Permissions on an Organization](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-user-access-to-your-organizations-repositories/managing-repository-roles/setting-base-permissions-for-an-organization)

  <br>
  </details>

----

### Repositories

#### Info:
- Organizations can have a few to a few thousand repositories.
- Repositories are where your developers and supporting teams collaborate.
- <details>
    <summary>Three Types of Repositories</summary>
    <br>

    - **Private** - only accessible to members of the org.
    - **Internal** - accessible to all orgs (used for [innersource](https://resources.github.com/innersource/what-is-innersource/)).
    - **Public** - can be read or forked by anyone on the internet.

    <br>
  </details>
- Repositories can be categorized for easy filtering.
- Repository access is managed via GitHub Teams.
- Rulesets control how users interact with repository branches and tags.
- <details>
  <summary>What's in a Repository (Code! but there's more 🙂)</summary>
  <br>
  
  - Code
  - Markdown
  - Pull Requests
  - Issues & Projects (project management)
  - Wikis
  - Actions (CI/CD)
  - GitHub Advanced Security tooling
  - Repo insights

  <br>
  </details>

# <Line>

#### Best Practices

- <details>
  <summary>Create Rulesets for your production branches and/or release tags.</summary>
  <br>
  
  - _Rationale:_
    - Rulesets protect your branches and tags from unexpected changes.
    - Example rules:
      - Require pull requests before code is merged to a production branch.
      - Require Codeowner review.
      - Prevent deletions.
    - Optionally create rulesets for other branches.

  <br>

  <br>

  - **To create Rulesets, go to:**
    - _Organization &rarr; Settings (tab at the top) &rarr; Repositories (left sidebar) &rarr; Rulesets_ OR
    - _Repository &rarr; Settings (tab at the top) &rarr; Rules (left sidebar) &rarr; Rulesets_
       
  <br>
  
  - **GitHub Docs:**
    - [Rulesets](https://docs.github.com/en/enterprise-cloud@latest/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets)
    - [Create a Ruleset Overview](https://docs.github.com/en/enterprise-cloud@latest/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets)
    - [Create a Branch/Tag Ruleset](https://docs.github.com/en/enterprise-cloud@latest/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository#creating-a-branch-or-tag-ruleset)


  <br>
  </details>

- <details>
  <summary>Use Custom Properties to organize your repositories.</summary>
  <br>

  - _Rationale:_
    - Many companies have hundred or thousands of repositories that contain things like monorepos, microservices, internal tooling, documentation, customer facing tools, backfill scripts, and forks of open source tools.
    - Finding specific repositories can become unwieldy and it's not always feasible to implement strict naming conventions for repositories.
    - Categorizing repositories makes it much easier to find and manage reposotiries over time.
    - Custom properties are the best way to categorize repositories in GitHub.
    - Examples: Use repo categories to identify
      - repositiries that contain internal tooling and the type of tooling.
      - microservices for particular projects or product lines.
      - teams repsonsible for monitoring deploys.
     
  - **To create Custom Properties, go to:**
    - _Organization &rarr; Settings (tab at the top) &rarr; Repositories (left sidebar) &rarr; Custom Properties &rarr; New property (button top right)_
  - **To assign Custom Properties, go to:**
    - _Repository &rarr; Settings (tab at the top) &rarr; Custom Properties (left sidebar)_
       
  <br>
  
  - **GitHub Docs:**
    - [Managing Custom Properties](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-organization-settings/managing-custom-properties-for-repositories-in-your-organization)
    - [Create Custom Properties](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-organization-settings/managing-custom-properties-for-repositories-in-your-organization#adding-custom-properties)
    - [Setting Custom Properties]([https://docs.github.com/en/enterprise-cloud@latest/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository#creating-a-branch-or-tag-ruleset](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-organization-settings/managing-custom-properties-for-repositories-in-your-organization#setting-values-for-repositories-in-your-organization)


  <br>
  </details>

- <details>
  <summary>Pin important repositories on the org landing page for easy access.</summary>
  <br>

  - _Rationale:_
    - Many companies have repos that are very active. Pin these to the organization landing page so that everyone, especially new developers, can find them easily.
   
  <br>

  - **To pin repositories, go to:**
    - _Organization (landing page) &rarr; View as (right sidebar) &rarr; Member &rarr; Pin Repositories (blue link)_

  <br>

  - **GitHub Docs:**
    - [Customizing Your Organization's Profile](https://docs.github.com/en/enterprise-cloud@latest/organizations/collaborating-with-groups-in-organizations/customizing-your-organizations-profile)
    - [Pinning Repositories to Your Profile](https://docs.github.com/en/enterprise-cloud@latest/organizations/collaborating-with-groups-in-organizations/customizing-your-organizations-profile#pinning-repositories-to-your-organizations-profile)
  
  <br>
  </details>

----

### Teams

#### Info:
- Teams are groups of organization members.
- Teams are used for communication and controlling repository access permissions.
- <details>
  <summary>What's in a Team</summary>
  <br>

  - Members
  - Repository access controls
  - Project access controls
  - Organization role controls

  <br>
  </details>

# <Line>

#### Best Practice: 

- <details>
  <summary>Organize members into teams that reflect your company's structure.</summary>
  <br>

  - _Rationale:_
    - Teams are used for managing repository access, but they are also used for communication and can be used to filter repositories and security alerts (for customers using Advanced Security).
    - Given this, it is important to have teams that reflect your company or engineering team's structure.
    - **Note:** In addition to teams that reflect your comapny structure, you can also create teams that are just for permissions.
      - Example:
        - Your engineering group has a dev team called, "DevTeam1," that includes a team lead, four develoeprs, a QA engineer, and a scrum leader.
        - The team lead should have admin permissions on three repository, but everyone else should only have read or write permissions on those repositories.
        - Create a GitHub team for DevTeam1 that can be used for communication. Assign repos and give the team Read access.
        - Create another GitHub team for the developers on DevTeam1. Assign repos and give the devs Write access.
        - Finally, create one more GitHub team for the team lead. Assign repos and give them Admin access.
       
  <br>

  - **Note:** Teams can be synced to IdP groups. For more information, see the `new-enterprise-setup` readme or the `enabling-sso-on-existing-organization` readme.

  <br>

  - **To create teams, go to:**
    _ _Organization &rarr; Teams &rarr; New team (button to the right)_

  - **GitHub Docs:**
    - [Teams](https://docs.github.com/en/enterprise-cloud@latest/organizations/organizing-members-into-teams/about-teams)
    - [Creating a Team](https://docs.github.com/en/enterprise-cloud@latest/organizations/organizing-members-into-teams/creating-a-team)

  <br>
  </details>

----

For more best practices, please talk to your GitHub Rep or Solutions Engineer.

