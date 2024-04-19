# GitHub Copilot License Assignment

<details>
  <summary>Step 1: Set Up a Payment Method for GitHub Copilot</summary>
  <br>

  - **Info:** GitHub Copilot is billed monthly. Charges will be posted against a payment method configured on the Enterprise account. The payment method can be a credit card or Azure Subscription.
  - **Go to:**
    - _Enterprise &rarr; Settings (left sidebar) &rarr; Billing &rarr; Payment Information (tab under the Billing heading and metered services summary)_

  # <Line>

  - **GitHub Docs:**
    - **Credit Card:** [Adding/Updating Enterprise Account Payment Information](https://docs.github.com/en/enterprise-cloud@latest/billing/managing-your-github-billing-settings/adding-or-editing-a-payment-method)
    - **Azure Subscription:** [Connecting an Azure Subscription to GitHub](https://docs.github.com/en/enterprise-cloud@latest/billing/managing-the-plan-for-your-github-account/connecting-an-azure-subscription)

  <br>
</details>

<details>
  <summary>Step 2: Enable GitHub Copilot at the Enterprise Level</summary>
  <br>

  - **Info:** Copilot must be enabled for organizations at the enterprise level before organization admins can assign Copilot licenses to members of their organizations.
  - **Go to:**
    - _Enterprise &rarr; Policies (left sidebar) &rarr; Access Management (landing tab) &rarr; select "Allow for: All Organizations" OR "Allow for: Specific Organizations"_
   
  # <Line>

  - **GitHub Docs:**
    - [Managing Access to GitHub Copilot in Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-github-copilot-in-your-enterprise#managing-access-to-github-copilot-in-your-enterprise)

  <br>
</details>

<details>
  <summary>Step 3: Set Copilot Policies at the Enterprise or Organization Level</summary>
  <br>

  - **Info:** Copilot policies can be configured at the enterprise or organization level. Copilot policies determine which features are available to users and whether matches to public code will be blocked.
    - Please Note: Copilot in GitHub.com requires Copilot Enterprise licenses. Once enabled, all Copilot license assignments will be for Copilot Enterprise rather than Copilot Business (see additional info below).
  - **Go to:**
    - _Enterprise &rarr; Polices (left sidebar) &rarr; Policies (tab toward the top, under the Copilot heading)_
    - _Organization &rarr; Settings (tab at the top) &rarr; Copilot (left sidebar) &rarr; Policies_
   
  # <Line>

  - **GitHub Docs:**
    - **Enterprise Level Enforcement**
      - [Enforcing an Enterprise Policy for Matches to Public Code](https://docs.github.com/en/enterprise-cloud@latest/admin/policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-github-copilot-in-your-enterprise#enforcing-a-policy-to-manage-the-use-of-github-copilot-suggestions-that-match-public-code)
      - [Enforcing an Enterprise Policy for Copilot Access in GitHub.com](https://docs.github.com/en/enterprise-cloud@latest/admin/policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-github-copilot-in-your-enterprise#enforcing-a-policy-to-manage-the-use-of-github-copilot-features-on-githubcom)
      - [Enforcing an Enterprise Policy for Copilot Chat in the IDE](https://docs.github.com/en/enterprise-cloud@latest/admin/policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-github-copilot-in-your-enterprise#enforcing-a-policy-to-manage-the-use-of-github-copilot-chat-in-ides)
      - [Enforcing an Enterprise Policy for Copilot in the CLI](https://docs.github.com/en/enterprise-cloud@latest/admin/policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-github-copilot-in-your-enterprise#enforcing-a-policy-to-manage-the-use-of-github-copilot-in-the-cli)
    - **Organization Level Enforcement**
      - [Enforcing an Organization Policy for Matches to Public Code](https://docs.github.com/en/enterprise-cloud@latest/copilot/managing-github-copilot-in-your-organization/managing-policies-and-features-for-copilot-in-your-organization#configuring-suggestion-matching-policies-for-github-copilot-in-your-organization)
      - [Enforcing an Organization Policy for Copilot Access in GitHub.com, Chat in the IDE, and Copilot in the CLI](https://docs.github.com/en/enterprise-cloud@latest/copilot/managing-github-copilot-in-your-organization/managing-policies-and-features-for-copilot-in-your-organization#enabling-features-of-github-copilot-in-your-organization)

  <br>
</details>

<details>
  <summary>Step 4: Assign Copilot Licenses to Users</summary>
  <br>

  - **Info:** Copilot licenses can be assigned to individual users or teams. Copilot licenses can also be assigned by uploading a CSV of users.
  - **Go to:** 
    - _Organization &rarr; Settings (tab top right) &rarr; Copilot (left sidebar) → Access &rarr; select "Enable for: All members of the organization" OR "Enable for: Selected members"_

  # <Line>

  - **GitHub Docs:**
    - [Configuring Access to GitHub Copilot in Your Organization](https://docs.github.com/en/enterprise-cloud@latest/copilot/managing-github-copilot-in-your-organization/managing-access-for-copilot-in-your-organization#configuring-access-to-github-copilot-in-your-organization)
  
  <br>
</details>

<details>
  <summary>Step 5: Share Copilot Resources with Your Devs</summary>
  <br>

  - **GitHub Docs:**
    - [Configuring Copilot in Your IDE](https://docs.github.com/en/enterprise-cloud@latest/copilot/configuring-github-copilot/configuring-github-copilot-in-your-environment)

  - **Other Resources:**
    - [Tips for Prompting Copilot](https://github.blog/2023-06-20-how-to-write-better-prompts-for-github-copilot/)
    - [GitHub Copilot Tips & Tricks](https://www.youtube.com/watch?v=1qs6QKk0DVc) (video resource)
    - [Beginners Guide to Prompt Engineering](https://dev.to/github/a-beginners-guide-to-prompt-engineering-with-github-copilot-3ibp)

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
    <summary>Provide time for developers to practice using Copilot.</summary>
    <br>
    
    - _Rationale:_
      - When developers work with Copilot, they are prompt engineering.
      - Prompt engineering is a skill that can be learned and improved.
    - _GitHub Resources for Copilot Practice:_
      - [Copilot Hackathon](https://github.com/octodemo/copilot-hackathon) (repo)

    <br>
    </details>

  - <details>
    <summary>Review Copilot usage data.</summary>
    <br>
    
    - _Rationale:_
      - Review usage data to ensure you haven't allocated more licenses than are needed.
      - Review usage data to get a sense of who is using Copilot and how it is impacting your business.
    - GitHub Docs:
      - [Copilot Usage Data in the UI](https://docs.github.com/en/enterprise-cloud@latest/copilot/managing-github-copilot-in-your-organization/managing-access-for-copilot-in-your-organization#reviewing-usage-data-for-github-copilot-in-your-organization)
      - [Copilot Usage Data in the API](https://docs.github.com/en/enterprise-cloud@latest/rest/copilot/copilot-user-management?apiVersion=2022-11-28#list-all-copilot-seat-assignments-for-an-organization)

    <br>
    </details>

  <br>
</details>
