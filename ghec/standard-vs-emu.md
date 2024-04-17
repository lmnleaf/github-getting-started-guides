# Standard GitHub Enterprise Account vs Enterprise Managed User Account

### Standard GitHub Enterprises

Standard GitHub enterprises are designed so tech companies can do two things:
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
    - A user must login to their personal GitHub account and login via SSO to access the organization's resources.
      - Note: users cannot access any private resources on GitHub without logging in to their personal account.
    - When a user's SSO session expires and they go to a link or URL for organization resources, they will be , they will be prompted to login via SSO.
    - If a user logs out of their GitHub personal account and then goes to a link or URL for organization resources, they will be promted to
      - 1) login to their personal account and
      - 2) login with SSO.
  - With standard enterprises:
    - User provisioning automatically invites an existing GitHub user to become a member of the organization.
      - When the user accepts the invite, they will be prompted to login with SSO. At that time, GitHub will link their GitHub personal account to their IdP identity.
    - User deprovisioning removes the GitHub user from the organization, and they will no longer be able to access the organization's resources.
  - Note: For standard enterprises, best practices is to set up SSO at the organization level as SCIM is only available at that level. In addition, configuring SSO at the organization level allows companies with multiple business entities/subsidiaries to configure SSO with different IdPs on different organizations.

  <br>
</details>

# <Line>

### Enterprise Managed Users

Enterprise Managed User (EMU) enterprise are designed for companies with:
- strict compliance requirements that prevent them from using the standard model.

<details>
  <summary>How SSO & SCIM Work with an EMU Enterprise</summary>
  <br>
  
  - SAML SSO & SCIM can be configured at the Enterprise level only.
  - Once SSO and SCIM are configured:
    - A user must login with SSO to access organization resources.
  - With EMUs:
    - user provisioning creates a new user account in GitHub.
    - user deprovisioning deletes the account.
  - There are some restrictions on EMU enterprises that do not apply to standard enterprises (see next dropdown).

  <br>
</details>

<details>
  <summary>EMU Limitations</summary>
  <br>

  <br>
</details>

