
#  Introduction to Role-Based Access Control (RBAC) in Azure

<img width="739" alt="image" src="https://github.com/user-attachments/assets/db7d0ccc-e33d-4628-92d8-01ee0a55d5b8" />



## Objective
This lab demonstrates how to use Azure Role-Based Access Control (RBAC) to assign permissions to a user, allowing them to access specific resources like a virtual machine in Azure.

---

## Key Concepts

### Authentication and Authorization
1. **Authentication**:
   - Verifies a user's identity via Microsoft Entra ID (Azure AD).
2. **Authorization**:
   - Determines what actions a user is allowed to perform on Azure resources.

### RBAC Roles
Azure provides several built-in roles to manage resource access:
- **Owner**: Full control over resources and can delegate access.
- **Contributor**: Can manage resources but cannot delegate access.
- **User Access Administrator**: Can delegate access but cannot manage resources.
- **Reader**: Can view resources but cannot make changes.

### Default Behavior
- New users do not have access to Azure resources unless explicitly assigned a role.

---

## Steps to Assign Permissions Using RBAC

### Step 1: Create a Virtual Machine
1. Log in to the Azure portal as the **admin account**.
2. Navigate to **Virtual Machines** and click **+ Create**.
3. Configure the virtual machine:
   - **Image**: Select Ubuntu Server.
   - **Size**: Choose a smaller size for this demo.
4. Click **Review + Create** and then **Create**.
5. Wait for the deployment to complete.

---

### Step 2: Verify Default Access for the New User
1. In another browser tab, log in as the newly created user (e.g., `userA`).
2. Navigate to **All Resources** or **Virtual Machines**.
   - **Expected Result**: The user should see the "Welcome to Azure!" page and no resources because no permissions have been assigned.

---

### Step 3: Assign a Role to the User
1. Log back into the Azure portal as the **admin account**.
2. Navigate to the **Virtual Machine** you created in Step 1.
3. Go to the **Access control (IAM)** section in the virtual machine's settings.
4. Click **+ Add** > **Add role assignment**.
5. Configure the role assignment:
   - **Role**: Select `Reader`.
   - **Members**: Click **Select members**, choose the user (e.g., `userA`) from Microsoft Entra ID, and click **Select**.
6. Click **Review + Assign** to complete the role assignment.

---

### Step 4: Verify Assigned Permissions
1. Wait for 1-2 minutes for the role assignment to propagate.
2. Log back in as the user (`userA`) and refresh the page.
3. Navigate to **Virtual Machines**:
   - **Expected Result**: The user should now see the virtual machine but with read-only access based on the `Reader` role.

---

## Key Takeaways
1. **RBAC Enhances Security**:
   - Ensures users only have permissions necessary for their tasks.
2. **Granular Access Control**:
   - Assign roles at the resource level, group level, or subscription level.
3. **Flexibility**:
   - Use built-in roles for common scenarios or define custom roles for specific requirements.

---

## Summary
- This lab demonstrated how to create a virtual machine and assign RBAC roles to a user.
- RBAC ensures secure and efficient management of resource access in Azure.
- Using roles like `Reader`, you can control who has access to view or modify resources.
```
