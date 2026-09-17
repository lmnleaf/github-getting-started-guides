# GitHub Copilot License Assignment

<details>
  <summary>Step 1: Set Up a Payment Method for GitHub Copilot</summary>
  <br>

  - **Info:** GitHub Copilot is billed monthly. Charges will be posted against a payment method configured at the Enterprise level or on a Cost Center in the Enterprise Account.
    - **Enterprise Level Payment Methods:**
      - GitHub only customers can pay for Copilot with a credit card or PayPal.
      - Microsoft customers, who have an Azure subscription, can pay with an Azure Subscription ID.
    - **Cost Centers:**
      - A Cost Center is a way to manage spending for enterprise teams, organizations, repositories, or individual members. In the case of Copilot, add enterprise teams, organizations, or individual members to the Cost Center, and add the Cost Center to a budget.

  - **To set an Enterprise level payment method, go to:**
    - _Enterprise &rarr; Billing & Licensing (tab at the top) &rarr; Payment Information (left sidebar)_

  # <Line>
  
  - **GitHub Docs:**
    - [Payment Info: Managing Your Payment and Billing Information](https://docs.github.com/en/enterprise-cloud@latest/billing/how-tos/set-up-payment/manage-payment-info)

  <br>
</details>

<details>
  <summary>Step 2: Create Enterprise Teams</summary>
  <br>

  - **Info:** Enterprise teams are groups of users at the enterprise level.
    - Enterprise teams can be linked to Identity Provider groups.
    - Enterprise teams can be used to manage Copilot access and policies for a group of users.
      - Copilot licenses can be assigned to an enterprise team, so anyone who's added to the team automatically receives a Copilot license.
      - Model policies that limit which models are available to users can be set for enterprise teams.
      - Enterprise teams can be assigned to Cost Centers so an AI credit budget can be set for the team and/or Copilot spend can be tracked.
    - Enterprise teams can be used to assign users to organizations.
    - Enterprise teams can be used for enterprise level role assignment.
   
  - **To create an Enterprise Team, go to:**
    - _People &rarr; Enterprise Teams (left sidebar)_
   
  - **GitHub Docs:**
    - [Creating Enterprise Teams](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-accounts-and-repositories/managing-users-in-your-enterprise/create-enterprise-teams)

  <br>
</details>

<details>
  <summary>Step 3: Create Cost Centers & Budgets</summary>
  <br>

  - **Info:** Cost Centers and Budgets allow you to limit included AI credit usage and overages for the enterprise, enterprise teams, and individual users.

  - **To create a Cost Center and Budget, go to:**
    - _Enterprise &rarr; Billing & Licensing (left sidebar) &rarr; Cost Centers (left sidebar) &rarr; New Cost Center_
      - Add the enterprise team.
      - Add the Azure Subscription ID.
      - Select **AI included credit usage cap** to limit the cost center to consuming the AI credits included with the Copilot licenses associated with the cost center.
    - _Enterprise &rarr; Billing & Licensing (tab at the top) &rarr; Budgets and Alerts &rarr; New Budget_
      - Select AI Credit Usage.
      - Add spending limits and alerts as needed.

  # <Line>
  
  - **GitHub Docs:**
    - [Cost Centers: Allocate Costs to Business Units](https://docs.github.com/en/enterprise-cloud@latest/billing/how-tos/products/use-cost-centers)
    - [Budgets: Setting Up Budgets to Control Spending](https://docs.github.com/en/enterprise-cloud@latest/billing/how-tos/set-up-budgets)
    - [Usage Based Billing for Organizations and Cost Centers](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/billing-and-usage/organizations-and-enterprises/billing)
    - [Controlling and Tracking Costs at Scale](https://docs.github.com/en/enterprise-cloud@latest/billing/tutorials/control-costs-at-scale)

  <br>
</details>

<details>
  <summary>Step 4: Assign Copilot Licenses to Enterprise Teams</summary>
  <br>

  - **Info:** When an enterprise team is assigned a Copilot license, every member in the team will have a Copilot license.

  - **To assign Copilot licenses to Enterprise Teams, go to:**
    - _Enterprise &rarr; AI Controls (tab at the top) &rarr; Copilot (left sidebar) &rarr; Access Management (box near the top) &rarr; Enterprise Teams (tab in the middle of the page)_

  - **GitHub Docs:**
    - [Granting Users Access to GitHub Copilot in Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-access/grant-access)
  

  <br>
</details>

<details>
  <summary>Step 5: Set Copilot Policies at the Enterprise Level</summary>
  <br>

  - **Info:** Copilot policies and models can be configured at the enterprise level. Copilot models can be configured for the enterprise and for enterprise teams.
    - Copilot policies determine which features are available to users.
    - Copilot models determine which models are available to users.
  - **To configure Copilot policies and models, go to:**
    - _Enterprise &rarr; AI Controls (tab at the top) &rarr; Copilot (left sidebar) &rarr; Features & Clients (middle of the page)_
    - _Enterprise &rarr; AI Controls (tab at the top) &rarr; Copilot (left sidebar) &rarr; Models (box in top section of page)_
  - **To configure Copilot models for enterprise teams, go to:**
    - _Enterprise &rarr; People (tab at the top) &rarr; Enterprise Teams (left sidebar) &rarr; Default Models (tab)_
  
  # <Line>

  - **GitHub Docs:**
    - [Managing Policies and Features for Copilot in Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies)
    - [Managing Availability of Models in Your Enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-availability-of-default-models)

  <br>
</details>
