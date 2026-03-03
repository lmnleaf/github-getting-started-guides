# GitHub Copilot License Assignment

<details>
  <summary>Step 1: Set Up a Payment Method for GitHub Copilot</summary>
  <br>

  - **Info:** GitHub Copilot is billed monthly. Charges will be posted against a payment method configured at the Enterprise level or on a Cost Center in the Enterprise Account.
    - **Enterprise Level Payment Methods:**
      - GitHub only customers can pay for Copilot with a credit card or PayPal.
      - Microsoft customers, who have an Azure subscription, can pay with an Azure Subscription ID.
    - **Cost Centers:**
      - A Cost Center is a way to manage spending for groups of organizations, repositories, or individual members. In the case of Copilot, add organizations or individual members to the Cost Center. Optionally, add the Cost Center to a Budget, to limit the features billed to the Cost Center or to set spending limits for Copilot.
      - **Cost Center Payment Methods:**
        - GitHub only customers can use Cost Centers to manage spending, but everything will be billed to the enterprise level payment method.
        - Microsoft customers, who have an Azure subscription, can use Cost Centers to bill to unique Azure Subscription IDs per Cost Center. 

  - **To set an Enterprise level payment method, go to:**
    - _Enterprise &rarr; Billing & Licensing (tab at the top) &rarr; Payment Information (left sidebar)_

  - **To create a Cost Center and Budget, go to:**
    - _Enterprise &rarr; Billing & Licensing (left sidebar) &rarr; Cost Centers (left sidebar) &rarr; New Cost Center_
      - Add the organization or members.
      - Add the Azure Subscription ID.
    - _Enterprise &rarr; Billing & Licensing (tab at the top) &rarr; Budgets and Alerts &rarr; New Budget_
      - Add Copilot.
      - Add spending limits and alerts as needed.

  # <Line>
  
  - **GitHub Docs:**
    - [Cost Centers: Allocate Costs to Business Units](https://docs.github.com/en/enterprise-cloud@latest/billing/using-the-new-billing-platform/charging-business-units)
    - [Budgets: Controlling Spending for Metered Products](https://docs.github.com/en/enterprise-cloud@latest/billing/using-the-new-billing-platform/preventing-overspending)
    - [Payment Info: Managing Your Payment and Billing Information](https://docs.github.com/en/enterprise-cloud@latest/billing/using-the-new-billing-platform/managing-your-payment-and-billing-information)

  <br>
</details>

<details>
  <summary>Step 2: Enable GitHub Copilot for Organizations at the Enterprise Level</summary>
  <br>

  - **Info:** Copilot Business licenses can be assigned at the enterprise or organization level. Copilot Enterprise licenses must be assigned at the organization level.
    - If Copilot licenses will be assigned by organization admins at the organization level, Copilot must be enabled for organizations at the enterprise level first.
    - If you are assigning Copilot licenses at the enterprise level, go to Step 3.
  - **Go to:**
    - _Enterprise &rarr; AI Controls (tab at the top) &rarr; Copilot (left sidebar) &rarr; Access Management (box in top section of page) &rarr; Organizations (tab middle of page) &rarr; select organization &rarr; set Copilot license type &rarr; Assign Licenses (button)_
   
  # <Line>

  - **GitHub Docs:**
    - [Enabling Copilot for Organizations](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-access/grant-access#enabling-copilot-for-organizations)

  <br>
</details>

<details>
  <summary>Step 3: Set Copilot Policies at the Enterprise Level</summary>
  <br>

  - **Info:** Copilot policies and models can be configured at the enterprise level.
    - Copilot policies determine which features are available to users.
    - Copilot models determine which models are available to users.
  - **Go to:**
    - _Enterprise &rarr; AI Controls (tab at the top) &rarr; Copilot (left sidebar) &rarr; Privacy_ AND _Features (middle of the page)_
    - _Enterprise &rarr; AI Controls (tab at the top) &rarr; Copilot (left sidebar) &rarr; Configure Allowed Models (box in top section of page)_
  # <Line>

  - **GitHub Docs:**
    - **Enterprise Level Enforcement**
      - [Managing Policies and Features for Copilot in Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/managing-copilot/managing-copilot-for-your-enterprise/managing-policies-and-features-for-copilot-in-your-enterprise)

  <br>
</details>

<details>
  <summary>Step 4: Assign Copilot Licenses to Users</summary>
  <br>

  - **Info:** Copilot licenses can be assigned to individual users or teams at the enterprise or organization level. Copilot licenses can also be assigned by uploading a CSV of users.
  - To assign licenses at the **enterprise level**, **go to:**
    - _Enterprise &rarr; AI Controls (tab at the top) &rarr; Copilot (left sidebar) &rarr; Access Management (box in top section of page) &rarr; All Members_ or _Enterprise Teams (tabs middle of page)_
  - to assign licenase at the **organization level**, **go to:**
    - _Organization &rarr; Settings (tab top right) &rarr; Copilot (left sidebar) → Access &rarr; select Enable for: All members of the organization_ OR _Enable for: Selected members_

  # <Line>

  - **GitHub Docs:**
    - [Assigning Licenses at the Enterprise Level](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-access/grant-access#assigning-licenses)
    - [Creating Enterprise Teams](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-users-in-your-enterprise/create-enterprise-teams)
    - [Enabling Copilot for Organizations](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-access/grant-access#enabling-copilot-for-organizations) and [Granting Access to Copilot for Members of Your Organization](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-organization/manage-access/grant-access)
    - [Set Up Team Synchronization with an IdP Group](https://docs.github.com/en/enterprise-cloud@latest/organizations/organizing-members-into-teams/synchronizing-a-team-with-an-identity-provider-group)
  
  <br>
</details>

<details>
  <summary>Step 5: Share Copilot Resources with Your Devs</summary>
  <br>

  - **GitHub Docs:**
    - [Configuring Copilot in Your IDE](https://docs.github.com/en/enterprise-cloud@latest/copilot/configuring-github-copilot/configuring-github-copilot-in-your-environment)
    - [Completions for GitHub Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/completions)
    - [GitHub Copilot Chat](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/chat)
    - [IDE Copilot Chat Cheat Sheet](https://docs.github.com/en/enterprise-cloud@latest/copilot/reference/cheat-sheet)
    - [GitHub Copilot Coding Agent, Code Review, and CLI](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/agents)
    - [Prompting and Customizing Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/prompting)
    - [Model Selection](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/auto-model-selection)
    - [Copilot Auto Model Selection](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/auto-model-selection)

  - **Other Resources:**
    - [GitHub Copilot Fridays]([https://github.registration.goldcast.io/series/ff0939de-f20a-4395-80ff-4bc606e356fd](https://github.registration.goldcast.io/series/ff0939de-f20a-4395-80ff-4bc606e356fd#Text%20Grid%204))
    - [GitHub YouTube Channel](https://www.youtube.com/@GitHub) (regularly updated with new Copilot tips and training videos)
    - [VS Code YouTube Playlist: GitHub Copilot Series for VS Code](https://www.youtube.com/playlist?list=PLj6YeMhvp2S5_hvBl2SE-7YCHYlLQ0bPt)
    - [GitHub Copilot Training Modules](https://learn.microsoft.com/en-us/training/browse/?terms=GitHub%20Copilot)(from Microsoft Learn)

  <br>
</details>

<details>
  <summary>Best Practices for Copilot Adoption</summary>
  <br>
  
  - <details>
    <summary>Identify Copilot Champions.</summary>
    <br>
    
    - _Rationale:_
      - Many developers resist adopting new tools including Copilot, but the faster your developers adopt Copilot, the more quickly your team will see productivity gains overall.
      - Copilot Champions are early adopters and AI enthusaists who recognize the value of Copilot for increased productivity.
      - Copilot Champions act as a resource for your team, making adoption more attractive and easier by providing tips for working with Copilot and concrete use cases where Copilot made a difference for them.
      - When your developers have questions about Copilot or want to learn more about prompt engineering, send them to your Copilot Champions.
      - Engineering teams with Copilot Champions adopt Copilot more quickly.

    <br>
    </details>

  - <details>
    <summary>Provide Copilot training for your administrators and developers.</summary>
    <br>
    
    - _Rationale:_
      - Copilot training will help your developers become efficient Copilot users.
      - Copilot training will help your admins setup Copilot at scale and identify security considerations.
    - _GitHub Training Programs:_
      - [GitHub Copilot Business for Developers Fundamentals](https://github.com/services/copilot-for-business-fundamentals-training)
      - [GitHub Copilot Business for Developers - Intermediate](https://github.com/services/github-copilot-for-developers-intermediate)
      - For additional training programs, including Copilot programs for adminstrators that address security considerations, contact your GitHub rep or view GitHub's [Services Catalog](https://github.com/services#services-catalog).

    <br>
    </details>

  - <details>
    <summary>Provide time for developers to learn about and practice using Copilot.</summary>
    <br>
    
    - _Rationale:_
      - When developers work with Copilot, they are prompt engineering.
      - Prompt engineering is a skill that can be learned and improved.
    - _Resources for Copilot Learning & Practice:_
      - [5 Ways to Integrate Copilot Coding Agent into Your Workflows](https://github.blog/ai-and-ml/github-copilot/5-ways-to-integrate-github-copilot-coding-agent-into-your-workflow/)
      - [Build Reliable AI Workflows with Agent Primitives and Context Engineering](https://github.blog/ai-and-ml/github-copilot/how-to-build-reliable-ai-workflows-with-agentic-primitives-and-context-engineering/?utm_source=blog-release-oct-2025&utm_campaign=agentic-copilot-cli-launch-2025)
      - [How to Use Copilot to Level Up Code Reviews and PRs](https://github.blog/ai-and-ml/github-copilot/how-to-use-github-copilot-to-level-up-your-code-reviews-and-pull-requests/)
      - [Tips for Writing Custom Instructions for Copilot](https://github.blog/ai-and-ml/github-copilot/5-tips-for-writing-better-custom-instructions-for-copilot/)
      - [Awesome Copilot](https://github.com/github/awesome-copilot) (repo)
      - [GitHub Copilot Hackathon](https://github.com/octodemo/copilot-hackathon) (repo)
      - [Microsoft Learn: Copilot Learning Modules] (https://learn.microsoft.com/en-us/training/browse/?terms=GitHub%20Copilot)

    <br>
    </details>

  - <details>
    <summary>Review Copilot metrics and usage data and GitHub's Engineering System Success Playbook.</summary>
    <br>
    
    - _Rationale:_
      - Review usage data to ensure you haven't allocated more licenses than are needed.
      - Review metrics to get a sense of who is using Copilot and how it is impacting your business.
      - Review GitHub's Engineering System Success Playbook for a 3 step process for driving meaningful and measurable improvements in your Engineering organization.
    - _Resources_:
      - [Copilot Metrics & Dashboards](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/copilot-usage-metrics)
      - [Measuring Copilot Adoption Over Time](https://docs.github.com/en/enterprise-cloud@latest/copilot/tutorials/roll-out-at-scale/measure-adoption)
      - [Driving the Downstream Impact of Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/tutorials/roll-out-at-scale/drive-downstream-impact)
      - [Copilot Metrics API](https://docs.github.com/en/enterprise-cloud@latest/rest/copilot/copilot-metrics?apiVersion=2022-11-28)
      - [Metrics Data Properties for GitHub Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/reference/metrics-data)
      - [Intro to GitHub's Engineering System Success Framework]( https://resources.github.com/engineering-system-success-playbook/)
      - [GitHub's Engineering System Success Playbook](https://assets.ctfassets.net/wfutmusr1t3h/59IWCIRvx0KfHbh6B7bv62/d9f55b94ab43fe91e9ed183d73882954/2025-05-28-GitHub-ESSP-Ebook-EZ-Version012.pdf)

    <br>
    </details>

  <br>
</details>
