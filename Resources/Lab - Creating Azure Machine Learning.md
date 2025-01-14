
# Lab: Creating an Azure Machine Learning Workspace

## Overview
In this lab, students will learn how to create an Azure Machine Learning workspace, which serves as the foundational setup for building, training, and deploying machine learning models in Azure. Follow the steps carefully to complete this task.

---

## Step-by-Step Instructions

### Step 1: Log in to Azure Portal
1. Open your web browser and go to [Azure Portal](https://portal.azure.com).
2. Log in with your Azure account credentials.

### Step 2: Navigate to All Resources
1. In the Azure Portal, click on **All Resources** from the left-hand menu.

### Step 3: Create a Machine Learning Workspace
1. Click on the **Create** button.
2. In the search bar, type **Machine Learning** and select **Machine Learning** from the results.
3. Click **Create** to start setting up the workspace.

### Step 4: Configure the Workspace
1. Choose your **Subscription** and **Resource Group**.
   - If you don't have an existing resource group, create one by clicking **Create New** and providing a name.
2. Enter a **Workspace Name** (e.g., `MLWorkspaceDemo`).
3. Select the **Region** as **North Europe**.
4. Review the details to ensure accuracy.

### Step 5: Additional Resources Setup
The Machine Learning workspace requires the following additional resources:
- Azure Storage Account
- Azure Key Vault
- Application Insights

Azure automatically creates these resources for you during the setup process.

### Step 6: Configure Networking
1. Under the **Networking** tab, set the workspace to **Public** access.
2. Skip the container registry configuration as it is not required for this lab.

### Step 7: Configure Encryption
1. Use **Microsoft Managed Keys** for encryption.
2. Leave all other settings as default.

### Step 8: Review and Create
1. Click on the **Review + Create** button.
2. Review all configurations.
3. Click **Create** to deploy the Machine Learning workspace.

### Step 9: Wait for Deployment
1. The deployment process will take a few minutes. Wait until the deployment is complete.
2. Once completed, navigate back to **All Resources**.

### Step 10: Launch Machine Learning Studio
1. In **All Resources**, locate and select your Machine Learning workspace.
2. Click on **Launch Studio** to open the Machine Learning Studio.

---

## Next Steps
In the next lab, you will:
- Explore the Machine Learning Studio.
- Create and configure a machine learning pipeline.
- Use historical data to train a machine learning model.
- Deploy and evaluate the model for predictions.

---

### Notes
- Ensure that you have the required permissions to create resources in Azure.
- If you encounter any issues, contact your instructor for assistance.

---

**Instructor Guidance:** This lab sets the foundation for using Azure Machine Learning services. Emphasize the importance of each step, particularly resource configurations and understanding the additional resources Azure sets up automatically.
