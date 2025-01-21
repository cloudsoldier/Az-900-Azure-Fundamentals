
# Introduction to Role-Based Access Control (RBAC) in Azure

## Overview
Role-Based Access Control (RBAC) in Azure allows fine-grained access management for Azure resources. It ensures that users only have the permissions explicitly assigned to them, enhancing security and control in large organizations.

---

## Key Concepts

### Authentication and Authorization
1. **Authentication**: Verifies the user's identity using Microsoft Entra ID (Azure AD).
2. **Authorization**: Determines the user's permissions for accessing Azure resources.

### RBAC Roles
- **Owner**:
  - Complete access to manage resources.
  - Can delegate access to other users.
- **Contributor**:
  - Can manage resources but cannot delegate access.
- **User Access Administrator**:
  - Can delegate access but cannot manage resources.
- **Reader**:
  - Read-only access to resource properties.

### Key Points:
- By default, new users have **no permissions**.
- Permissions must be explicitly assigned using RBAC roles.

---

## Steps to Assign a Role to a User

### Step 1: Create a Resource
1. Log in to Azure with the **admin account**.
2. Navigate to **Virtual Machines** and click **+ Create** to create a new VM.
3. Specify the details:
   - **Image**: Ubuntu Server.
   - **Size**: Choose a smaller size for the demo.
4. Click **Review + Create** and then **Create**.
5. Wait for the deployment to complete.

---

### Step 2: Verify Access as a New User
1. In another browser tab, log in with the newly created user (e.g., `userA`).
2. Navigate to **All Resources** or **Virtual Machines**.
   - **Expected Behavior**: The user will not see any resources because no permissions have been assigned.

---

### Step 3: Assign a Role Using RBAC
1. Log back in as the Azure admin.
2. Go to the resource you want to assign permissions to (e.g., the virtual machine).
3. Navigate to the **Access control (IAM)** section.
4. Click **+ Add** > **Add role assignment**.
5. Configure the role assignment:
   - **Role**: Choose the desired role (e.g., `Reader`).
   - **Members**: Select the user (e.g., `userA`).
6. Click **Review + Assign** to save the changes.

---

### Step 4: Verify Permissions
1. Wait a few minutes for the role assignment to take effect.
2. Log in as `userA` and refresh the page.
3. Navigate to **Virtual Machines**:
   - The user should now see the assigned resource (e.g., the virtual machine) with the appropriate permissions based on the assigned role.

---

## Key Takeaways
1. **RBAC Enhances Security**:
   - Limits resource access based on roles.
   - Reduces the risk of unauthorized actions.

2. **Built-In Roles**:
   - Azure provides a wide range of in-built roles for various scenarios.
   - Custom roles can be created for specific requirements.

3. **Practical Use Case**:
   - Demonstrated assigning the `Reader` role to a user to allow viewing a virtual machine without modifying it.

---

## Further Learning
- Explore advanced RBAC concepts and custom roles in Azure documentation.
- Study the **AZ-500** exam for in-depth knowledge of Azure security practices.

---

## Summary
In this chapter, we:
- Learned how RBAC ensures secure and controlled access to Azure resources.
- Explored assigning roles to users and verifying access.
- Highlighted the importance of using RBAC for managing permissions in a large organization.
