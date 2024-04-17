# Standard GitHub Enterprise vs Enterprise Managed Users

### Standard GitHub Enterprise

Standard GitHub enterprises are designed so companies can do two things:
- work on their own proprietary codebases.
- collaborate with their customers and the broader development community.

Most GitHub customers are on a standard GitHub enterprise. 

# <Line>

<details>
  <summary>Analogy: GitHub as Coworking Space</summary>
  <br>

  GitHub and the stanard GitHub enterprise are somewhat analogous to a physical coworking space.

  - Imagine a coworking space in a multi-level building:
    - First Floor
      - The first floor is for collaboration:
        - Although anyone can look in the windows when walking by the building, only members can actually get in.
        - To access the first floor, you _must_ be a member of the coworking space - you must have the door code and check in at the front desk.
    - Upper Floors
      - The upper floors house individual companies.
        - People walking by can't see in, and each floor is only accessible to employees of the particular company on that floor.
        - To access an upper floor, an employee must have the elevator code for that floor.

  <br>

  - Now think about GitHub:
    - Everyone with a personal account is part of the GitHub community.
      - All members of the GitHub community must log in with a username and password (and eventually with 2FA).
    - But only some people can access enterprise resources, i.e., organizations & private repositories.
      - Access to enterprise resources is invite only.
      - And access to enterprise resources protected by SSO requires an additional login.

  <br>
</details>

# <Line>

<details>
  <summary>How SSO & SCIM Work on a Standard GitHub Enterprise</summary>
  <br>
  
  - SAML SSO can be configured at the enterprise or organization level.
  - When an organization requires SSO:
    - A user must login to their personal GitHub account AND login via SSO to access the organization's resources.
      - Note: users cannot access any private resources on GitHub without logging in to their personal account.
    - When a user's SSO session expires and they go to a link or URL for organization resources, they will be prompted to login via SSO.
    - If a user logs out of their GitHub personal account and then goes to a link or URL for the organization's resources, they will be promted to:
      - 1) login to their personal account and
      - 2) login with SSO.
  - User provisioning and deprovisioning with SCIM:
    - User provisioning automatically invites an existing GitHub user to become a member of the organization.
      - When the user accepts the invite, they will be prompted to login with SSO. At that time, GitHub will link their GitHub identity to their IdP identity.
    - User deprovisioning automatically removes the GitHub user from the organization.
      - The user will no longer have access the organization's resources, and their GitHub identity will no longer be linked to the IdP identity.
  - Note: For standard enterprises, best practice is to set up SSO at the organization level as SCIM is only available at that level. In addition, configuring SSO at the organization level allows companies with multiple business entities/subsidiaries to configure SSO with different IdPs on different organizations.

  <br>
</details>

# <Line>

### Enterprise Managed Users

Enterprise Managed User (EMU) enterprise are designed for companies with:
- strict compliance requirements that prevent them from using the standard model.

# <Line>

<details>
  <summary>EMU Limitations</summary>
  <br> 
  
  - Some teams use public facing repositories, gists, wikis, or pages to share client libraries or tooling with their customers and the broader development community. This is NOT an option with EMU.
    - EMU enterprises have only private and internal repositories.
    - EMU enterprises cannot interact with public facing resources. For example, they cannot create or fork public repositories. 
  - All members of an EMU enterprise must have an identity in the same IdP tenant.
    - There are some cases where this is not ideal. For example, when one company acquires another and both companies use separate IdPs for SSO.
  - Finally, with EMU, the commits your devs make at work will not add to their GitHub contribution graphs. The contribution graph never shows details about commits made to private repositories, but it does show that a developer committed on any given day. Some developers want their contributions to show because it is part of how they market themselves to the larger development community and to future employers.
  - Existing GitHub Customers: Moving from a GitHub organization or standard GitHub enterprise to an EMU enterprise requires a migration.
    - There are two options for the migration:
      - a self-serve migration using [GitHub Enterprise Importer](https://github.com/github/gh-gei).
      - an [Expert Services](https://github.com/services/) engagement.
    
  <br>
</details>

# <Line>

<details>
  <summary>How SSO & SCIM Work on an EMU Enterprise</summary>
  <br>
  
  - SAML SSO & SCIM can be configured at the Enterprise level only.
  - When SSO is configured:
    - A user must login with SSO to access the organization's resources.
  - User provisioning and deprovisioning with SCIM:
    - User provisioning creates a new user account in GitHub.
      - The user will be invited to access the GitHub account which will also give them access to the organization's resources.
    - User deprovisioning deletes the account.
      - The user will no longer have access to a work related GitHub account or to the organization's resources.
  - There are some restrictions on EMU enterprises that do not apply to standard enterprises (see next dropdown).

  <br>
</details>

