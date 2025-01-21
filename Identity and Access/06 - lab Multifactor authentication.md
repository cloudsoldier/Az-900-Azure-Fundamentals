# Notes and Lab: Multi-Factor Authentication (MFA) in Microsoft Entra ID

## Overview
Multi-Factor Authentication (MFA) in Microsoft Entra ID adds an extra layer of security during the authentication process by requiring an additional form of identification beyond just a username and password.



<img width="702" alt="image" src="https://github.com/user-attachments/assets/4670da21-de8f-499b-ae5c-1befa2f1d5c2" />

---

## Key Features of MFA
1. **Purpose**:
   - Protects against unauthorized access even if login credentials are compromised.
   - Ensures only genuine users can complete the authentication process.

2. **Common MFA Methods**:
   - **Microsoft Authenticator App**
   - **Windows Hello for Business**
   - **Security Keys**
   - **SMS and Voice Call**

3. **Use Case**:
   - Elevated privilege accounts or users with access to critical resources should have MFA enabled.

---

## Steps to Enable and Configure MFA

### Step 1: Enable MFA for a User
1. Log in to the [Azure Portal](https://portal.azure.com) as an **admin account**.
2. Navigate to **Microsoft Entra ID** (or search for "Azure Active Directory").
3. Go to **Users** > **Per-user MFA**:
   - If you cannot see the option, access it through the **context menu** in the top-right corner.
4. On the **Multi-Factor Authentication** screen, select the user (e.g., `userA`).
5. Click **Enable** to activate MFA for the selected user.

---

### Step 2: Configure MFA for the User
1. Log out as the admin and log in as the user (e.g., `userA`).
2. Enter the username and password. You will be prompted with a message saying **"More information is required."**
3. Follow the prompts to register for MFA:
   - **Choose a verification method**:
     - Default: Microsoft Authenticator App.
     - Alternative: Use **Phone**.
   - **Enter phone details**: Provide a valid mobile number to receive verification codes via SMS.
4. Complete the verification:
   - Receive a code on your mobile device.
   - Enter the code in the prompt and confirm.

---

### Step 3: Test MFA
1. Log out as the user (`userA`).
2. Log back in and verify:
   - After entering the username and password, you should receive a code on your registered mobile device.
   - Enter the code to complete the authentication process.

---

### Step 4: Review and Manage MFA Settings
1. As an admin, return to the **Microsoft Entra ID** > **Per-user MFA** section.
2. Review the **MFA status** for users:
   - **Enforced**: MFA is enabled and required for the user.
3. Explore **Service Settings**:
   - Configure options such as allowed verification methods.
   - Set requirements for trusted IPs or remember MFA on trusted devices.

---

### Step 5: Disable MFA (Optional)
1. As an admin, navigate back to **Per-user MFA**.
2. Select the user (e.g., `userA`) and click **Disable**.
3. Confirm the action to turn off MFA for the user.

---

## Key Takeaways
1. **Enhanced Security**:
   - MFA adds an essential security layer for accounts with elevated privileges or sensitive resources.
2. **User Flexibility**:
   - Supports multiple verification methods tailored to user preferences.
3. **Configurable Policies**:
   - Admins can fine-tune MFA settings based on organizational needs.

---

## Lab Summary
This lab covered:
- Enabling MFA for users in Microsoft Entra ID.
- Configuring and testing MFA with SMS-based verification.
- Managing MFA settings and optionally disabling MFA.
- Understanding how MFA ensures robust security in Azure environments.

