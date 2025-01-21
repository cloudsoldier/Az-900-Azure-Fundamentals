# Introduction to Microsoft Entra ID (Azure AD)

## Overview
Microsoft Entra ID (formerly Azure Active Directory) is a cloud-based identity and access management service. It provides secure access to Azure resources, Microsoft 365, and other software as a service (SaaS) applications.


![Uploading image.png…]()

---

## Key Features
1. **User Management**:
   - Define and manage user identities.
   - Users can log in to the Azure account with their credentials (username and password) and access assigned resources.

2. **Application Authentication**:
   - Create application identities in Microsoft Entra ID.
   - Applications can authenticate themselves to access resources securely.

3. **Centralized Identity Provider**:
   - Used across Azure, Microsoft 365, and other SaaS platforms for seamless identity management.

---

## Why Use Microsoft Entra ID?
- In large organizations, managing access using a single admin account is not scalable.
- Microsoft Entra ID allows delegation of access control by creating unique user credentials for employees and defining their permissions.

---

## Authentication and Authorization
### Authentication
- Verifies the identity of the user or application.
- Ensures the user is part of the identity provider (Microsoft Entra ID).

### Authorization
- Checks if the user or application has the necessary permissions to access specific Azure resources.
- Examples:
  - Is the user authorized to access a virtual machine?
  - Is the user authorized to view or modify a storage account?

---

## Use Cases
1. **Access Management**:
   - Manage access for employees, applications, and third-party services.
   - Assign roles and permissions to users based on their job functions.

2. **Application Integration**:
   - Securely integrate applications with Azure resources using managed identities.

3. **Single Sign-On (SSO)**:
   - Provide seamless access to multiple services and applications using one set of credentials.

4. **Secure Azure Resource Management**:
   - Enable employees to manage resources securely without sharing administrative credentials.

---

## Importance for AZ-900
- Understanding Microsoft Entra ID is critical for managing access and ensuring security in Azure.
- Key concepts include:
  - Defining users and permissions.
  - Differ

