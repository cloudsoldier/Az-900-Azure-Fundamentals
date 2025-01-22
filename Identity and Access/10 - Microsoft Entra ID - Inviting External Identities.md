# Lab: Business-to-Business Collaboration in Microsoft Entra ID

## Objective
Understand how to invite and manage external identities (guest users) in Microsoft Entra ID for secure business-to-business collaboration.

---

## Steps

### 1. **Setup: Access Microsoft Entra ID**
- Log in to the **Azure portal** with your Azure admin account.
- Navigate to **Microsoft Entra ID** from the left-hand menu.

---

### 2. **Invite External User**
- In the **Microsoft Entra ID** blade:
  - Go to **Users**.
  - Click on **+ New guest user**.
- Fill in the following details:
  - **Email address**: `examusr1000@outlook.com` (or any external identity email).
  - **Display name**: Provide a display name for the user (e.g., `Exam User 1000`).
  - **Personal message (optional)**: Add an optional message to the invitation.
- Click **Next** to review additional settings:
  - Configure properties (optional).
  - Set up assignments (optional).
- Click **Invite**.

---

### 3. **Accept the Invitation as the External User**
- The invited user (`examusr1000@outlook.com`) will receive an invitation email.
- Steps for the invited user:
  - Open the email and click **Accept Invitation**.
  - Log in with their existing credentials (e.g., Outlook).
  - Review the requested permissions:
    - **Profile data**
    - **Activity tracking**
  - Click **Accept** to grant permissions.

---

### 4. **Verify External User in Directory**
- As the Azure admin:
  - Return to the **Users** section in **Microsoft Entra ID**.
  - Confirm that the external user (`examusr1000@outlook.com`) is listed.

---

### 5. **Assign Permissions**
- To grant access to resources:
  - Use **Role-Based Access Control (RBAC)**.
  - Assign appropriate roles to the external user.

---

### 6. **Sign In as External User**
- Log out of the Azure admin account.
- Log in as the external user (`examusr1000@outlook.com`) at [myapplications.microsoft.com](https://myapplications.microsoft.com).
- Confirm access permissions. If no permissions are granted, the user will not see available resources.

---

### 7. **Cleanup**
- As the Azure admin:
  - Sign back into the Azure portal.
  - Navigate to **Microsoft Entra ID > Users**.
  - Select the external user (`examusr1000@outlook.com`).
  - Click **Delete** to remove the user.

---

## Conclusion
This lab demonstrated how to:
1. Invite external identities into Microsoft Entra ID.
2. Enable business-to-business collaboration.
3. Assign and manage permissions for external users.
4. Clean up resources after the session.

--- 

**End of Lab**
