
# Lab: Introduction to Azure Key Vault Service

---

## **Objective**
Learn how to use Azure Key Vault to securely store and manage secrets, encryption keys, and certificates.


<img width="656" alt="image" src="https://github.com/user-attachments/assets/e9a70b37-127b-4b1b-bdb5-e38ebb5dfb4f" />

---

## **Steps**

### **Step 1: Overview of Azure Key Vault**
1. Azure Key Vault is a managed service that provides secure storage for:
   - **Secrets**: Securely store credentials like usernames and passwords.
   - **Encryption Keys**: Safeguard keys used to encrypt and decrypt sensitive data.
   - **Certificates**: Manage certificates for secure data transport (e.g., HTTPS protocol).

#### **Key Concepts**:
- **Secrets**:
  - Storing credentials directly in application code poses security risks.
  - Use Azure Key Vault to securely store database credentials and retrieve them via secure calls.
- **Encryption Keys**:
  - Used with encryption algorithms to protect data from unauthorized access.
  - Store keys securely in Key Vault to prevent malicious users from decrypting data.
- **Certificates**:
  - Facilitate secure communication between application servers using protocols like HTTPS.
  - Key Vault serves as a certificate manager, eliminating the need for separate tools.

---

### **Step 2: Create a Key Vault**
1. Log in to the **Azure Portal**.
2. Navigate to **Create a Resource** and search for **Key Vault**.
3. Configure the Key Vault:
   - **Resource Group**: Select an existing resource group or create a new one.
   - **Key Vault Name**: Provide a unique name for your Key Vault.
   - **Region**: Choose your preferred Azure region.
   - **Retention Period**: Set the number of days (minimum 7) to retain deleted vaults.
4. Permissions:
   - Choose either **Azure Role-Based Access Control (RBAC)** or **Access Policies**.
5. Click **Review + Create** to validate the configuration.
6. Once validation is complete, click **Create**.
7. Wait for the Key Vault to be deployed.

---

### **Step 3: Add Secrets to the Key Vault**
1. Navigate to the created Key Vault in the **Azure Portal**.
2. On the left-hand menu, go to **Secrets**.
3. Click **Generate/Import** and configure the secret:
   - **Name**: Provide a unique name for the secret (e.g., `DBPassword`).
   - **Value**: Enter the value for the secret (e.g., `MySecurePassword123`).
4. Click **Create** to save the secret.

---

### **Step 4: Add Encryption Keys**
1. In the Key Vault, navigate to **Keys**.
2. Click **Generate** to create a new key.
3. Configure the key:
   - **Name**: Provide a unique name for the key.
   - **Key Type**: Select the key type (e.g., RSA).
   - **Key Size**: Choose the desired key size (e.g., 2048).
4. Click **Create** to save the encryption key.

---

### **Step 5: Add Certificates**
1. In the Key Vault, navigate to **Certificates**.
2. Click **Generate/Import** to create or import a certificate.
3. Configure the certificate:
   - **Name**: Provide a unique name.
   - **Certificate Policy**: Define the policy or use the default settings.
4. Click **Create** to save the certificate.

---

### **Step 6: Access Secrets Securely**
1. Applications can retrieve secrets using secure API calls to Azure Key Vault.
2. Ensure the application is configured with proper permissions to access the Key Vault.

---

### **Step 7: Clean Up Resources**
1. Navigate to the **Azure Portal**.
2. Go to **All Resources** and locate your Key Vault.
3. Select the Key Vault and click **Delete**.
4. Confirm the deletion to avoid unnecessary costs.

---

## **Key Learnings**
- Azure Key Vault provides a secure way to manage secrets, encryption keys, and certificates.
- Secrets and keys are stored securely and can be accessed programmatically by authorized applications.
- Certificates are managed efficiently without requiring additional tools.

---

## **Further Learning**
- Learn the basics of Azure security services with the **AZ-900 exam**.
- For an in-depth understanding of security in Azure, explore the **AZ-500 exam**.

