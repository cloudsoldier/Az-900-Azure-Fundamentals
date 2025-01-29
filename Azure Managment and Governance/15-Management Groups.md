
<img width="879" alt="image" src="https://github.com/user-attachments/assets/bfae41df-13fc-4034-9042-e8ac31348c2a" />
# Azure Management Groups

## Overview
In this chapter, we explore **Management Groups**, which are used to manage multiple **Azure Subscriptions** efficiently. They provide an additional layer of organization beyond **Resource Groups** and **Resource Tags**.

---

## Key Topics Covered
### 1. **Understanding Management Groups**
   - **Purpose**:
     - Used to manage and group multiple subscriptions.
     - Provide a hierarchy for better **governance and access control**.
   - **Comparison with Resource Groups**:
     - **Resource Groups**: Group resources logically.
     - **Resource Tags**: Add metadata to resources.
     - **Management Groups**: Group multiple **subscriptions** together.

---

### 2. **Use Cases for Management Groups**
   - Large enterprises often have multiple Azure subscriptions:
     - Example:
       - **Research Subscription**
       - **Main Subscription**
       - **Logistics Subscription**
       - **Human Resources Subscription**
   - These can be grouped under different **Management Groups**:
     - **IT Management Group**: Holds IT-related subscriptions.
     - **Business Management Group**: Holds business-related subscriptions.

---

### 3. **Hierarchy of Management Groups**
   - **Top-Level Root Management Group**:
     - Every Azure account has a **root management group**.
     - Under this, multiple management groups can be created.
     - Subscriptions are added to management groups as needed.

---

### 4. **Benefits of Management Groups**
   - **Role-Based Access Control (RBAC)**:
     - Assign permissions at the **management group level**.
     - RBAC roles apply to:
       - All **subscriptions** under the management group.
       - All **resource groups** and **resources** within those subscriptions.
   - **Azure Policies**:
     - Define and enforce governance policies at the **management group level**.
     - Policies apply to all subscriptions within the management group.
   - **Improved Organization**:
     - Helps structure large cloud environments efficiently.

---

### 5. **Creating and Managing Management Groups**
   - Navigate to **Management Groups** in the Azure portal.
   - Create a new **Management Group**.
   - Add subscriptions under the group.
   - Apply **RBAC roles** and **Azure Policies** for governance.

---

## Summary
- **Management Groups** allow **logical grouping of Azure Subscriptions**.
- They help in **organizing, governing, and managing access control** across multiple subscriptions.
- **RBAC roles and Azure Policies** can be applied at the **management group level**, affecting all resources within the group.
- **For AZ-900**, understanding the concept and purpose of management groups is essential.

---
**Tip**: Use **Management Groups** to simplify access management and governance across multiple subscriptions in large organizations.
