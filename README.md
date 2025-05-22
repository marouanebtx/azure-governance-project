
# Azure Governance & Access Control Architecture

A hands-on governance structure in Azure to control and audit resource deployments using **Management Groups**, **Azure Policy**, and **RBAC**.

## Tools Used
- Azure Management Groups
- Entra ID Security Groups
- Role-Based Access Control (RBAC)
- Azure Policy

## Project Structure

- **Management Groups**:  
  - mg-LandingZone (Root)  
    - mg-IT  
    - mg-Dev
    - mg-HR

- **Entra ID Security Groups**:
  - IT-Contributer
  - DEV-Contributer
  - HR-Contributer
  - Managers-Readers

- **Role Assignments**:
  - Contributor roles to respective RGs
  - Reader role for "Managers-Readers" across all RGs

- **Policies**:
  - ✅ Allowed Locations: "UK South", "UK West"
  - ✅ Allowed VM Sizes: "B2s", "D2s_v3", "F2s_v2"
    _(*except "mg-IT" which can use any size)_
  - ✅ Append Tag from Resource Group

## Screenshots
See screenshots/ folder for examples of policy enforcement and role-based access behavior.

## Policy Definitions
Find JSON definitions under "policy-definitions/".

---
