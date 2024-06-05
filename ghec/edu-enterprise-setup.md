# GitHub Enterprise Best Practices for Educational Institutions

### Enterprise Configuration

<details>
  <summary>Use a Standard GitHub Enterprise.</summary>
  <br>
  
- GitHub has two types of enterprise accounts: **Standard** and **Enterprise Managed Users (EMU)**.
- Both provide a single point for management and enforcement of policies and settings for your institution's GitHub account.
- However, **standard enterprises** are more flexible and therefore recommended for educational institutions.

# <Line>

- <details>
  <summary>What's in an Enterprise Account?</summary>
  <br>
  
  - Organizations
  - Policies and Settings for All Organizations
  - Security Insights
  - GitHub Server License Keys
  - GitHub Connect (connects Server instances to Cloud instances for customers using GitHub Enterprise Server in addition to GitHub Enterprise Cloud)
  - Enterprise Audit Log
  - GitHub Compliance Documentation
  </details>
- <details>
  <summary>Why are standard enterprise accounts recommended for educational institutions?</summary>
  <br>
  
  - <details>
    <summary>Standard enterprises include the option for public facing resources.</summary>
    <br>
    
    - Public facing resources include things such as public repositories, issues, discussions, gists, and pages.
    - Public facing resources are important for various use cases.
      - _Example:_ A research group working on AI wants to share their newest AI skill with the braoder AI research community. They can do so by making the repo public.
    </details>
  - <details>
    <summary>Standard enterprises support SAML 2.0 SSO with Shibboleth.</summary>
    <br>

    - Shibboleth is used by many educational institutions for identity management.
    - Other supported identity providers include Microsoft Entra ID (previously known as Azure AD), Microsoft Active Directory Federation Services (AD FS), Okta, OneLogin, and PingOne.
    - [Supported SAML 2.0 Identity Providers](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-saml-single-sign-on-for-your-organization/about-identity-and-access-management-with-saml-single-sign-on#supported-saml-services)
    </details>
  - <details>
    <summary>Organizations and repositories can be transfered into or out of the enterprise via the GitHub UI.</summary>
    <br>
    
    - When educational institutions set up their GitHub enterprise, they often have multiple affiliated teams or people already working in existing GitHub organizations and repositories that should be, but are not, centrally managed by the institution.
      - _Example:_ A university IT department is already actively working in an existing GitHub organization. The organization does NOT have any authentication security in place, and the IT department head is expensing the cost of the GitHub organization each month. 
    - Educational institutions need a simple way to transfer such organizations or repositories into their enterprise.
      - **Note:** Organizations and repositories can be transferred into a standard enterprise via the UI with enterprise owner/admin approval and current owner/admin approval.
    - Sometimes educational institutions also need a simple way to transfer repositories out of the enterprise.
      - _Example:_ A student writes code for their Computer Science class. The code is added to a repository in the organization that belongs to their class. When the class ends, the student gets admin approval to transfer the repo into the student's personal namespace, so the student can continue working on their project and show their code, commit history, pull requests, etc., to a potential employer.
      - **Note:** organizations and repositories can be transferred out of an enterprise via the UI with current and future owner/admin approval.
    - [Inviting an Organization to Join an Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-organizations-in-your-enterprise/adding-organizations-to-your-enterprise#inviting-an-organization-to-join-your-enterprise-account)
    - [Repository Transfers](https://docs.github.com/en/enterprise-cloud@latest/repositories/creating-and-managing-repositories/transferring-a-repository#repository-transfers-and-organizations)
    </details>
  - <details>
    <summary>GitHub Enterprise features, such as GitHub Actions, Advanced Security, Codespaces, and Copilot, can be governed at the enterprise level.</summary>
    <br>

    - Educational institutions can set policies that permit or block access to certain features for all or selected organizations.
      - _Example:_ Features like GitHub Advanced Security can be purchased for selected organizations, such as one used by the institution's web development team, while still being blocked for all other organizations.
    - [Enterprise Policies Overview](https://docs.github.com/en/enterprise-cloud@latest/admin/policies/enforcing-policies-for-your-enterprise/about-enterprise-policies)
    </details>
  - <details>
    <summary>GitHub Contribution graphs reflect user activity in the enterprise.</summary>
    <br>

    - Contribution graphs appears on the public facing profile page of a GitHub user's personal account. 
    - Contribution graphs NEVER show details about commits made to private repositories, however, they do show the number of commits made on any given day regardless of whether that commit was made to a public or private repo.
    - Many developers, especially students, use their Contribution Graph to market themselves to the larger development community and to future employers. The contribution graph shows that they are actively committing code.
    - [GitHub Profile & Contribution Graph](https://docs.github.com/en/enterprise-cloud@latest/account-and-profile/setting-up-and-managing-your-github-profile/managing-contribution-settings-on-your-profile/showing-an-overview-of-your-activity-on-your-profile)
    </details>
  </details>

- <details>
  <summary>Why aren't EMU accounts recommended?</summary>
  <br>

  - EMU enterprises do NOT include any public facing resources.
  - Shibboleth is NOT a supported Identity Provider for SSO.
  - <details>
    <summary>All EMU user accounts, including student accounts, belong to the enterprise.</summary>
    <br>
    
    - In EMU enterprises, enterprise owners/admins create individual accounts for EMU enterprise members.
    - These individual user accounts are only available to the member in the context of the EMU enterprise.
    - Any repositories created by the user in their individual account, belong to the enterprise rather than the user.
    </details>
  - <details>
    <summary>Moving existing GitHub organizations and repositories into an EMU enterprise requires a migration.</summary>
    <br>
      
    - Migrations can be completed with GitHub's self-service CLI tool, GitHub Enterprise Importer, but bringing them into the enterprise will requires time spent planning, coordinating, and executing the migration.
    </details>

  </details>

----
</details>

<details>
  <summary>Setup SSO at the Enterprise level.</summary>
  <br>

- Give every member of your community access to the GitHub enterprise via your identity provider (IdP).

# <Line>

- <details>
  <summary>Why give every community member access to the GitHub enterprise?</summary>
  <br>

  - Give community members access to the GitHub enterprise as part of the standard system access they receive when joining the educational institution.
  - This makes it easier to manage access over the long term.
    - _Example:_ When organization owners/admins, such as a professor or department head, wants to invite new students to an organization, they will not need to also ensure that the students have access to the GitHub enterprise. Students will already have access via the your instutition's IdP.
  - **Notes:**
    - With this setup, any member of your community with a GitHub personal account can go to the enterprise landing page and login to the institution's enterprise account with SSO via your IdP.
      - If they do so and have NOT been invited to an organization, they will have access to an empty enterprise landing page.
    - Community members will need to be invited to an organization by an organization owner/admin to view the organization's resources (repos, issues, discussions, etc.).
  </details>
- [Configure SAML 2.0 SSO on an Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/identity-and-access-management/using-saml-for-enterprise-iam/configuring-saml-single-sign-on-for-your-enterprise)

----
</details>

<details>
  <summary>Setup multiple organizatons for different user groups.</summary>
  <br>

  - Educational institutions often have multiple distinct user groups that need their own organizations.

# <Line>

- <details>
  <summary>What's in an Organization?</summary>
  <br>

  - Repositories
  - GitHub Classrooms
  - Copilot Access (when permitted at the Enterprise level)
  - Projects
  - Packages
  - Discussions
  - Teams
  - Actions in Private Repositories (when permitted at the Enterprise level)
  - Security & Org Level Insights
  - GitHub Advanced Security (when purchased and permitted at the Enterprise level)
  - Audit Log
  - Organizations can have their own admins.
- <details>
  <summary>Why set up organizations for different groups?</summary>
  <br>

  - Organizations can be used for groups who work closely together and need access to many of the same repositories.
  - Each organization can have its own members, public and private repositories, and teams (groups of members with varying levels of permissions).
  - Enterprise admins can give selected organizations access to certain features, such as GitHub Advanced Security and Actions.
  - Organization admins can manage organization membership and settings for features made available to the organization by the enterprise admin.
  </details>
- <details>
  <summary>Example Use Cases for Organizations</summary>
  <br>
    
  - **Biology Department**
    - Members: professors and grad students who teach in the department.
    - Repos: tooling used for data analysis.
    - Feature Access:
      - GitHub Actions can be used in public and private repositories.
      - No access to GitHub Advanced Security.
      - No access to Copilot licenses through the university.
  - **Class: CS101**
    - Members: professors, TAs, and students for all CS101 class sections.
    - Repos: starter projects used in all CS101 classes regardless of who teaches them.
    - GitHub Classrooms: unique GitHub classrooms for each CS101 section and managed by the professor and TAs for that section.
    - Feature Access:
      - No access to GitHub Actions for private repositories.
      - No access to GitHub Advanced Security.
      - No access to Copilot licenses paid for by the university.
  - **IT Department**
    - Members: staff in the IT Department.
    - Repos: scripts and applications managed by IT.
    - Feature Access:
      - GitHub Actions in private repositories.
      - Copilot Business licenses through the university.
      - No access to GitHub Advanced Security.
  - **University Web App Development Team**
    - Members: seveloper team that creates and maintains the university website.
    - Repos: any relevant applications or microservices.
    - Feature Access:
      - GitHub Actions in private repositories.
      - Copilot Business licenses paid for by the university.
      - GitHub Advanced Security.
  - **Student Group**
    - Members: small group of students who have decided to work on coding projects together over the summer and want to make a website for their student group.
    - Repos: code for the student group's projects and website.
    - Feature Access:
      - No access to GitHub Actions on private repositories.
      - No access to GitHub Advanced Security.
      - No access to Copilot licenses through the university.
    </details>
  - [Organizations and Enterprise Accounts](https://docs.github.com/en/enterprise-cloud@latest/organizations/collaborating-with-groups-in-organizations/about-organizations#organizations-and-enterprise-accounts)
  - [Organizations Overview](https://docs.github.com/en/enterprise-cloud@latest/organizations/collaborating-with-groups-in-organizations/about-organizations)


----
</details>

# <Line>

### Organization Management

<details>
  <summary>Give staff in a central IT/services office GitHub enterprise support entitlements.</summary>
  <br>

- With GitHub support entitlements, IT/services staff will be able to open, view, and comment on support tickets for the enterprise account and any organizations within the enterprise via GitHub's support portal.
- **Notes:**
  - Support entitlements are only available with paid educational enterprise plans.
  - Enterprise owners/admins will automatically have support entitlements.

# <Line>

- [Managing Enterprise Support Entitlements](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-users-in-your-enterprise/managing-support-entitlements-for-your-enterprise)

----
</details>

<details>
  <summary>Manage organization creation through the central IT/services office.</summary>
  <br>

  - A central IT/services office should create GitHub organizations.

# <Line>

- <details>
  <summary>Why manage organization creation through a central IT/services office?</summary>
  <br>

  - Manage organization creation via a central office to:
    - Limit the number of Enterprise owners and support entitlements needed for the GitHub enterprise.
    - Allow for better monitoring and management of the enterprise.
  </details>
- <details>
  <summary>What will the IT/services office need to do to set up an organization?</summary>
  <br>
  
  - Create the new organization in the institution's enterprise account.
  - Invite an organization owner/admin to the organization.
  - Invite initial members to the organization.
  - **Notes:**
    - Organizations must be created via the GitHub UI, so some IT/services staff will need owner/admin access to the Enterprise.

  </details>

----
</details>

<details>
  <summary>Provide a process for individuals to request new organizations.</summary>
  <br>
  
- Providing a process for requesting a new GitHub organization will make it easy for members of your community to get started with GitHub.
- **Notes:**
  - Allow for flexibility in who can request a GitHub organization.
    - _Example:_ Allow students, professors, and staff to request organizations, rather than only department heads.
  - Too many restrictions on who can request or obtain a GitHub organization can delay projects and discourage community members from working on projects in organizations that can be monitored/governed by the educational institution.

# <Line>

- <details>
  <summary>Example GitHub Organization Request Process</summary>
  <br>

  - Professors, staff, or students go to an IT services website to submit a form to request a GitHub organization.
  - The form requires the following information:
    - Organization name.
    - Organization slug.
    - Organization owner/admin name.
    - Organization owner/admin GitHub account handle.
    - Purpose of the GitHub organization.
    - List of organization members.
  - The IT/services department will:
    - Create the GitHub organization manually via the GitHub UI.
    - Run a script to:
      - Invite the organization owner and members to join the organization.
      - Sets default organization level settings.
    - Give the organization access to features, such as Actions or Advanced Security, at the enterprise level when appropriate.
  </details> 
- [Create an Organization in an Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-organizations-in-your-enterprise/adding-organizations-to-your-enterprise)
- [Invite Members to an Organizaton](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-membership-in-your-organization/inviting-users-to-join-your-organization)
- [Create an Organization Member Invitation](https://docs.github.com/en/enterprise-cloud@latest/rest/orgs/members?apiVersion=2022-11-28#create-an-organization-invitation) (REST API Docs)
- [Enforce Enterprise Policies](https://docs.github.com/en/enterprise-cloud@latest/admin/policies)
- [Terraform: GitHub Provider for Managing Organizations](https://registry.terraform.io/providers/integrations/github/latest/docs) (maintained by HashiCorp)
- [Example Scripts for Managing Organizations](https://github.com/bertvv/github-org-mgmt) (open source project that is NOT supported by GitHub)


----
</details>

<details>
  <summary>Add an organization owner/admin when the organization is created.</summary>
  <br>

- Make the individual requesting the organization, or another designated person, an organization owner/admin.
- Among other things, organization owners/admins can:
  - Configure policies and settings on the GitHub organization that aren't already governed by the enterprise.
  - Invite organization members.
  - Add additional organization owners.
  - Create repositories within the organization.
  - Create repository rule sets.
  - Create teams of members to manage access to repositories within the organization.
 
# <Line>

- <details>
  <summary>What are Repository Rule Sets?</summary>
  <br>

  - Repository Rule Sets are rules that control how members of an organization can interact with selected branches and tags in a repository.
    - _Examples:_
      - Control who can push commits to a specified branch.
      - Require pull requests for specified branches.
      - Control who can delete or rename a tag.
  - Repository Rules can be configured per a repository or for all repositories in an organization.
  - [Repository Rule Sets](https://docs.github.com/en/enterprise-cloud@latest/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets)

  </details>
- <details>
  <summary>What are Teams?</summary>
  <br>

  - Teams are groups of organization members.
  - Teams are used grant/control repository and organization access permissions.
  - Teams are used for communication within GitHub (e.g., notifying a team that a particular PR needs attention).
  - <details>
    <summary>What's in a team?</summary>What's in a team?
    <br>
 
    - Members
    - Repository access controls
    - Project access controls
    - Organization role controls
    </details>
  - [GitHub Teams](https://docs.github.com/en/enterprise-cloud@latest/organizations/organizing-members-into-teams/about-teams)
  </details>
- [Organization Roles](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization#permissions-for-organization-roles)

----
</details>

<details>
  <summary>Make features such as GitHub Actions, Advanced Security, Codespaces, and Copilot available to selected organizations.</summary>
  <br>

- Some groups within your community will need access to additional GitHub features in their organization.
  - _Example:_ A university web develpment team needs access to GitHub Actions to test and deploy their applications and Advanced Security to scan their code for security vulnerabilities and secrets.

# <Line>

- [GitHub Actions](https://docs.github.com/en/enterprise-cloud@latest/actions/learn-github-actions/understanding-github-actions)
- [GitHub Advanced Security](https://docs.github.com/en/enterprise-cloud@latest/get-started/learning-about-github/about-github-advanced-security)
- [GitHub Codespaces](https://docs.github.com/en/enterprise-cloud@latest/codespaces/overview)
- [GitHub Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/about-github-copilot)
- [GitHub Packages](https://docs.github.com/en/enterprise-cloud@latest/packages/learn-github-packages/introduction-to-github-packages)

----
</details>

<details>
  <summary>Provide GitHub Enterprise server licenses to research teams or other groups as needed.</summary>
  <br>

- Research groups may have especially stringent compliance requirements, where even their code, not just their data, must be in a high compliance environment.
- In such cases, running a GitHub server instance in a high compliance environment is the best option.
- **Note:** GitHub Enterprise Server licenses are included with GitHub Enterprise plans.

# <Line>

- [GitHub Enterprise Server](https://docs.github.com/en/enterprise-server@3.12/admin/overview/about-github-enterprise-server)
- [Setting Up a GitHub Enterprise Server Instance](https://docs.github.com/en/enterprise-server@3.12/admin/installation/setting-up-a-github-enterprise-server-instance)

----
</details>

# <Line>

### Monitoring Enterprise and Organization Activity

<details>
  <summary>Use the GitHub Audit Log.</summary>
  <br>

- The audit log is available via the UI or API at the enterprise and organization levels.
- At the enterprise level, the audit log can be streamed to various SIEMs.
- Use the Audit Log to monitor enterprise and organization activity.
- Set up alerts for unexpected activity, such as changes to enterprise policies.

# <Line>

- [GitHub Enterprise Audit Log](https://docs.github.com/en/enterprise-cloud@latest/admin/monitoring-activity-in-your-enterprise/reviewing-audit-logs-for-your-enterprise/audit-log-events-for-your-enterprise)

----
</details>

<details>
  <summary>Provide organization owners with tools to maintain and monitor organization settings.</summary>
  <br>

- [Safe Settings](https://github.com/github/safe-settings) - a tool for monitoring and setting repository settings across an organization
- [Organization Audit Log](https://docs.github.com/en/enterprise-cloud@latest/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/audit-log-events-for-your-organization)

----
</details>

# <Line>

### Making the Most of GitHub

<details>
  <summary>Encourage students and faculty to take advantage of free GitHub offerings.</summary>
  <br>

- Many features are available for free to faculty and students OR on public facing repositories.

# <Line>

- [Free GitHub Education Benefits](https://education.github.com/discount_requests/application?type=student)
  - GitHub Education Benefits includes things such as:
    - Free Codespaces minutes.
    - Free Actions compute time.
    - Free access to GitHub Copilot.
- [GitHub Student Developer Pack](https://education.github.com/pack)
- [GitHub Education Overview](https://docs.github.com/en/education)
- [Dependabot Alerts](https://docs.github.com/en/enterprise-cloud@latest/code-security/getting-started/dependabot-quickstart-guide) (free on all GitHub repositories)

----
</details>

<details>
  <summary>Encourage faculty to use GitHub Classroom for technical courses.</summary>
  <br>

- GitHub Classroom provides professors, teachers, and school administrators with a digital classroom space.
- With GitHub Classroom, professors and teachers can:
  - Create assignments with due dates for individual students or groups of students.
  - Provide feedback and grade assignments.
  - Track assignments on a classroom dashboard.
  - Integrate with other educational tools.

# <Line>

- [GitHub Classroom](https://docs.github.com/en/education/manage-coursework-with-github-classroom/get-started-with-github-classroom/about-github-classroom)

----
</details>

<details>
  <summary>Share GitHub Skills with facutly and staff.</summary>
  <br>

- GitHub Skills is a collection of self-guided resources for learning about GitHub.
- GitHub Skills includeds lessons on things like Markdown, Pull Requests, and getting started with Actions.

# <Line>

- [GitHub Skills](https://skills.github.com/)

----
</details>

<details>
  <summary>Purchase Expert Services workshops for faculty and staff so they can become GitHub Champions and provide further training to other faculty, staff, and students.</summary>
  <br>

- Expert Services workshops teach developers how to use GitHub effectively.

# <Line>

- Example Workshops:
  - [GitHub Copilot for Developers Intermediate](https://github.com/services/github-copilot-for-developers-intermediate)
  - [GitHub Actions Training](https://github.com/services/actions-training)
  - [CodeQL Query Customizations](https://github.com/services/codeql-query-customizations)
- [Expert Services Catalog](https://github.com/services#services-catalog)

----
</details>
