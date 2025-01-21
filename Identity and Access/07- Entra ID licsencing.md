https://www.microsoft.com/en-us/security/business/microsoft-entra-pricing


# Notes and Lab: Microsoft Entra ID Licensing and Conditional Access

## Overview
Microsoft Entra ID (formerly Azure Active Directory) offers advanced security features like **Conditional Access** that require specific licenses. This chapter discusses licensing options, how to activate trial licenses, and considerations for using them effectively.

---

## Key Concepts

### Microsoft Entra ID Licensing Tiers
1. **Free Tier**:
   - Available by default when creating an Azure account.
   - Includes basic functionalities like user and group management.
2. **P1 License** ($6/user/month):
   - Adds features such as Azure AD Connect, self-service password reset, and basic Conditional Access.
3. **P2 License** ($9/user/month):
   - Includes advanced features like risk-based Conditional Access, identity protection, and governance tools.

### Licensing Features
- Licensing is separate from Azure's pay-as-you-go subscription model.
- Licenses apply to Microsoft Entra ID as a product used across Azure, Microsoft 365, and other services.

---

## Lab: Activating a Free Trial for Microsoft Entra ID P2 License

### Step 1: Access Licenses in Microsoft Entra ID
1. Log in to the [Azure Portal](https://portal.azure.com).
2. Navigate to **Microsoft Entra ID** (or search for "Azure Active Directory").
3. Go to **Licenses** > **All Products**.

### Step 2: Activate a Free Trial
1. On the **All Products** page, click **Try/Buy**.
2. Select **Microsoft Entra ID P2 Free Trial**:
   - This trial provides 100 licenses valid for 30 days.
   - Features will deactivate after the trial period without incurring charges.
3. Click **Activate** to enable the trial.

### Step 3: Assign Licenses to Users
1. Go to **Licenses** > **Assignments**.
2. Click **+ Assign** and select the P2 license.
3. Choose the users you want to assign the license to (e.g., `UserA`).
4. Click **Assign** to complete the process.

---

## Best Practices for Activating Licenses
1. **Timing**:
   - Activate the trial when you are ready to explore advanced features like Conditional Access.
   - Consider saving the trial for advanced studies (e.g., preparing for the AZ-500 exam).
2. **Plan Usage**:
   - Use the 30-day period to experiment with and understand the features included in the license.
3. **Maximize Value**:
   - Activate only when you have specific learning goals or projects requiring these features.

---

## Key Takeaways
1. **License Tiers**:
   - Understand the differences between Free, P1, and P2 tiers and their features.
2. **Conditional Access**:
   - Conditional Access is an advanced security feature available in P1 and P2 licenses.
3. **Free Trial**:
   - The free trial is a risk-free way to explore P2 features for 30 days.

---

## Summary
- Microsoft Entra ID licenses are separate from Azure's pay-as-you-go subscription and provide additional security features.
- You can activate a 30-day free trial for the P2 license to explore features like Conditional Access.
- Plan the activation of licenses to ensure maximum value and effectiveness in your learning or projects.

