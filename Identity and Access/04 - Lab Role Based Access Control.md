
# Lab: Assigning Roles at Different Levels in Azure RBAC

## Objective
This lab demonstrates how to assign roles at different levels within Azure Role-Based Access Control (RBAC) to manage access to multiple resources efficiently.

---

## Key Concepts

### RBAC Levels of Role Assignment
1. **Subscription Level**:
   - Roles assigned here apply to all resource groups and resources within the subscription.
2. **Resource Group Level**:
   - Roles assigned here apply to all resources within the specific resource group.
3. **Resource Level**:
   - Roles assigned here apply only to the individual resource.

### Default Access Behavior
- By default, a user with access to a single resource (e.g., a virtual machine) will not have access to related resources (e.g., public IP, network security group, or virtual network).

---

## Steps to Assign Roles for Access Across Resources

### Step 1: Verify Current User Permissions
1. Log in as **User A** in the Azure portal.
2. Navigate to **All Resources**:
   - **Expected Result**: Only the virtual machine (e.g., `appvm`) is visible.
3. Open the virtual machine details:
   - **Expected Result**: User A cannot see associated resources like the virtual network or public IP.

---

### Step 2: Assign a Role at the Resource Group Level
1. Log in as the **Azure admin** in the Azure portal.
2. Navigate to **Resource Groups** and select the resource group containing your virtual machine (e.g., `appGRP`).
3. Go to the **Access control (IAM)** section of the resource group.
4. Click **+ Add** > **Add role assignment**.
5. Configure the role assignment:
   - **Role**: Select `Reader`.
   - **Members**: Select **User A** from the Microsoft Entra ID user list.
6. Click **Review + Assign** to apply the role.

---

### Step 3: Verify Role Assignment Propagation
1. Wait for 1-2 minutes for the role assignment to propagate.
2. Log back in as **User A** and refresh the **All Resources** page:
   - **Expected Result**: User A should now see all resources in the resource group, including the public IP, virtual network, and network security group.
3. Open the virtual machine (`appvm`) and verify:
   - User A can now view associated resources like the virtual network and public IP.

---

## Additional Notes
- **Built-in Roles**: Azure provides a variety of built-in roles tailored for specific services, such as:
  - **Virtual Machine Contributor**: Manages virtual machines.
  - **Storage Account Contributor**: Manages storage accounts.
- **Inheritance**:
  - Roles assigned at higher levels (subscription/resource group) are inherited by lower levels (resource level).
- **Custom Roles**:
  - For specific requirements, custom roles can be defined to allow granular permissions.

---

## Key Takeaways
1. **Role Assignments**:
   - Assigning roles at the resource group or subscription level simplifies access management for multiple resources.
2. **Efficient Permission Management**:
   - Use RBAC to manage access for users across a hierarchy of resources.
3. **Granular Control**:
   - Assign roles at different levels based on organizational requirements and security best practices.

---

## Summary
- This lab demonstrated how roles assigned at the **resource group level** provide access to all resources within the group.
- You learned the hierarchical structure of RBAC in Azure and how roles can be assigned to simplify user permissions.
- RBAC is a critical component of Azure security, ensuring controlled and efficient access management.
```
