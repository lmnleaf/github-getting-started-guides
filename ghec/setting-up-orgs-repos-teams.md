# Best Practices: Organizations, Repositories, and Teams

### Organizations

#### Info:
- Enterprises can have one or more organizations.
- Organizations include
  - Repositories
  - Copilot access
  - Projects
  - Packages
  - Discussions
  - Teams
  - Security & org level insights
  - Audit Log
- Each organization can have a distinct set of members.
- Each organization has it's own repositories.
- **Note:** Distinct organizations are NOT needed to limit repository access. (See Best Practices below for more info).

# <Line>

#### Best Practice:

- Create **one** organization.

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


