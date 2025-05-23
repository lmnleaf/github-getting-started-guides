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
    - _Enterprise &rarr; Billing & Licensing (left sidebar) &rarr; Payment Information (left sidebar)_

  - **To create a Cost Center and Budget, go to:**
    - _Enterprise &rarr; Billing & Licensing (left sidebar) &rarr; Cost Centers (left sidebar) &rarr; New cost center_
      - Add the organization or members. **Note:** Members must be added via the API.
      - Add the Azure Subscription ID.
    - _Enterprise &rarr; Billing & Licensing (left sidebar) &rarr; Budgets and alerts &rarr; New budget_
      - Add Copilot.
      - Add spending limits and alerts as needed.

  # <Line>
  
  - **GitHub Docs:**
    - [Cost Centers: Charging Business Units](https://docs.github.com/en/enterprise-cloud@latest/billing/using-the-new-billing-platform/charging-business-units)
    - [Budgets: Preventing Overspending](https://docs.github.com/en/enterprise-cloud@latest/billing/using-the-new-billing-platform/preventing-overspending)
    - [Payment Info: Managing Your Payment and Billing Information](https://docs.github.com/en/enterprise-cloud@latest/billing/using-the-new-billing-platform/managing-your-payment-and-billing-information)

  # <Line>
  
  - <details>
      <summary>Previous Billing Platform (will be deprecated 2025 Q1)</summary>
      <br>

      - **Note:** All enterprises should be migrated to the new billing platform by the end of Q1 2025.
      - **Info:** If your enterprise is still on the previous billing platform, you will only be able to bill for Copilot licenses at the enterprise level.
      - **To add billing information, go to:**
        - _Enterprise &rarr; Settings (left sidebar) &rarr; Billing &rarr; Payment Information (tab under the Billing heading and metered services summary)_


      - **GitHub Docs:**
        - [Adding/Updating Enterprise Account Payment Information (Credit Card or PayPal)](https://docs.github.com/en/enterprise-cloud@latest/billing/managing-your-github-billing-settings/adding-or-editing-a-payment-method)
        - [Connecting an Azure Subscription to GitHub](https://docs.github.com/en/enterprise-cloud@latest/billing/managing-the-plan-for-your-github-account/connecting-an-azure-subscription)

      <br>
    </details>

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
  <summary>Step 3: Set Copilot Policies at the Enterprise Level</summary>
  <br>

  - **Info:** Copilot policies can be configured at the enterprise level. Copilot policies determine which features are available to users.
  - **Go to:**
    - _Enterprise &rarr; Polices (left sidebar) &rarr; Policies (tab toward the top, under the Copilot heading)_
   
  # <Line>

  - **GitHub Docs:**
    - **Enterprise Level Enforcement**
      - [Managing Policies and Features for Copilot in Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/managing-copilot/managing-copilot-for-your-enterprise/managing-policies-and-features-for-copilot-in-your-enterprise)

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
    - [Set Up Team Synchronization with an IdP Group](https://docs.github.com/en/enterprise-cloud@latest/organizations/organizing-members-into-teams/synchronizing-a-team-with-an-identity-provider-group)
  
  <br>
</details>

<details>
  <summary>Step 5: Share Copilot Resources with Your Devs</summary>
  <br>

  - **GitHub Docs:**
    - [Configuring Copilot in Your IDE](https://docs.github.com/en/enterprise-cloud@latest/copilot/configuring-github-copilot/configuring-github-copilot-in-your-environment)
    - [Changing the AI Model for Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/using-github-copilot/ai-models/changing-the-ai-model-for-copilot-chat?tool=vscode)
    - [Copilot Agents](https://docs.github.com/en/enterprise-cloud@latest/copilot/building-copilot-extensions/building-a-copilot-agent-for-your-copilot-extension/about-copilot-agents)
    - 

  - **Other Resources:**
    - [GitHub Copilot Fridays](https://github.registration.goldcast.io/series/ff0939de-f20a-4395-80ff-4bc606e356fd)
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
    <summary>Provide time for developers to practice using Copilot.</summary>
    <br>
    
    - _Rationale:_
      - When developers work with Copilot, they are prompt engineering.
      - Prompt engineering is a skill that can be learned and improved.
    - _Resources for Copilot Practice:_
      - [GitHub Copilot Hackathon](https://github.com/octodemo/copilot-hackathon) (repo)
      - [Microsoft Learn: Copilot Learning Modules](https://learn.microsoft.com/en-us/training/browse/?terms=GitHub%20Copilot)

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
      - [Copilot Metrics in the API](https://docs.github.com/en/enterprise-cloud@latest/rest/copilot/copilot-metrics?apiVersion=2022-11-28)

    <br>
    </details>

  <br>
</details>
