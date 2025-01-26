
# Notes: Syncing Identities from On-Premises Microsoft AD to Microsoft Entra ID

## Microsoft Entra ID Domain Services
- Acts as a substitute for Microsoft Active Directory (AD) on the Azure platform.
- Provides a managed service for hosting Microsoft AD.

## Scenario
- The company cannot migrate on-premises users to Microsoft Entra ID.
- Applications are migrated to Azure, but identities remain on-premises in Microsoft AD.
- On-premises users need access to Azure services.

## Challenge
- Role-based access control (RBAC) in Azure typically requires users in Microsoft Entra ID.
- On-premises users in Microsoft AD need access to Azure resources.

## Solution
- Sync on-premises AD identities to Microsoft Entra ID using **Microsoft Entra Cloud Sync**.
- This allows users to exist in both:
  - On-premises Microsoft AD.
  - Microsoft Entra ID.

## Purpose of Microsoft Entra Cloud Sync
- Enables continuous synchronization of identities from on-premises Microsoft AD to Microsoft Entra ID.
- Ensures on-premises users can access Azure resources using RBAC.

## Chapter Focus
- Explains the concept and process of syncing on-premises identities to Microsoft Entra ID using Microsoft Entra Cloud Sync.
