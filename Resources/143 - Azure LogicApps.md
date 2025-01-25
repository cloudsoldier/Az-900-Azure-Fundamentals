
# Azure Logic Apps Lab: Creating a Workflow for Blob Upload Notifications

## Objective
This lab demonstrates how to use Azure Logic Apps to create a no-code workflow that sends an email notification whenever a blob is uploaded to an Azure Storage container.

---

## Prerequisites
1. An active Azure subscription.
2. Access to the Azure Portal.
3. An Outlook email account (e.g., free Outlook.com account).

---

## Step 1: Create an Azure Storage Account
1. Go to the [Azure Portal](https://portal.azure.com).
2. Navigate to **Create a Resource** and search for **Storage Account**.
3. Click **Create** and fill in the following:
   - **Resource Group**: Create a new resource group or select an existing one.
   - **Storage Account Name**: Enter a unique name for your storage account (e.g., `mylogicappstorage`).
   - **Region**: Choose a preferred region.
   - **Redundancy**: Select **Locally Redundant Storage (LRS)**.
4. Click **Review + Create** and then **Create**.
5. Once created, open the Storage Account and navigate to **Containers**.
6. Create a new container:
   - **Name**: Enter `data`.
   - **Public Access Level**: Leave at default (private).
   - Click **Create**.

---

## Step 2: Create an Azure Logic App
1. Navigate to **Create a Resource** and search for **Logic App**.
2. Click **Create** and configure the following:
3. - **Plan Type**: Select **Consumption** for a simple, pay-as-you-go plan.
  
   - <img width="447" alt="image" src="https://github.com/user-attachments/assets/352e15db-ec08-496a-b3c3-d3973f7a012b" />

   - **Resource Group**: Use the same resource group as the Storage Account.
   - **Logic App Name**: Enter a unique name (e.g., `MyBlobWorkflow`).
   - **Region**: Choose the same region as your Storage Account.
   
4. Click **Review + Create** and then **Create**.

---

## Step 3: Design the Logic App Workflow
1. Open the Logic App and navigate to **Logic App Designer**.
2. Select **Blank Logic App**.
3. Add a **Trigger**:
   - Search for **Azure Blob Storage** in the connectors list.
   - Select **When a blob is added or modified**.
   - Provide the following:
     - **Connection Name**: Enter a descriptive name (e.g., `BlobConnection`).
     - **Authentication Type**: Select **Access Key**.
     - **Storage Account Name**: Enter your storage account name.
     - **Access Key**: Obtain the key from **Access Keys** in the Storage Account settings and paste it here.
   - Click **Create** to establish the connection.
   - Select your container (`data`) from the list.


# Go to your logicapp app

4. Add an **Action**:
   - Click **+ New Step**.
   - Search for **Outlook.com**.
   - Select **Send an email (V2)**.
   - Sign in to your Outlook account.
   - Configure the email:
     - **To**: Enter your Outlook email address.
     - **Subject**: Enter `Blob Details`.
     - Click blue fx and choose dynamic
     - <img width="184" alt="image" src="https://github.com/user-attachments/assets/a3c8a948-3e55-4a80-81bc-9f076a3709cb" />
- Add list of Files Item
- <img width="584" alt="image" src="https://github.com/user-attachments/assets/a94ea0e6-9f48-4b6d-8a9d-c2e90d2928de" />
- click Add
     - **Body**: Click **Dynamic Content** and add the relevant blob information (e.g., file name, size, and container name).

5. Click **Save**.

---

## Step 4: Test the Workflow
1. Navigate to the Storage Account **Containers** > `data`.
2. Upload files:
   - Click **Upload**, browse your local machine, and select files (e.g., `access.txt` and `deployment.yaml`).
   - Click **Open** and then **Upload**.
3. Wait for a few minutes. The Logic App will run and send emails with details of the uploaded blobs.

---

<img width="1525" alt="image" src="https://github.com/user-attachments/assets/d7675823-0820-46bc-8fc4-37bfe9ba93b5" />


## Step 5: Verify Email Notifications
1. Open your Outlook email account.
2. Check for new emails:
   - Each email should contain:
     - **File Name**
     - **Container Name**
     - **File Size**

---

## Step 6: Clean Up Resources
1. Navigate to **Resource Groups** in the Azure Portal.
2. Select the resource group used for this lab.
3. Click **Delete Resource Group**.
4. Confirm the deletion by typing the resource group name.

---

## Lab Summary
- You successfully created a Logic App workflow to send email notifications for blob uploads.
- Azure Logic Apps simplify workflow automation without requiring coding expertise.
