
# Lab: Creating an Azure Storage Account for Data Lake Storage Gen2

## Objective
Learn how to create an Azure Storage Account configured as **Data Lake Storage Gen2** for storing and managing large-scale data, such as application logs, which can later be analyzed.

---

## Key Concepts

1. **Azure Storage Account**:
   - A service for storing large amounts of data in the cloud.
   - Supports multiple data types such as blobs, files, and queues.

2. **Data Lake Storage Gen2**:
   - Built on Azure Blob Storage.
   - Designed for big data and analytics workloads.
   - Enables **hierarchical namespace**, which provides directory and file semantics for organizing data efficiently.

3. **Hierarchical Namespace**:
   - Allows the creation of directories and subdirectories.
   - Simplifies working with large datasets and analytics tools.

---

## Steps to Create an Azure Data Lake Storage Gen2 Account

### Step 1: Create a Storage Account
1. **Navigate to Storage Accounts**:
   - Open the Azure Portal.
   - Search for **Storage Accounts** in the search bar and click **Create**.

2. **Configure Basics**:
   - Choose your existing **Resource Group** or create a new one.
   - Provide a **unique name** for the Storage Account (e.g., `datalakestorage123`).
   - Select the **Region** as **North Europe**.
   - Choose the **Performance** tier as **Standard**.
   - Set the **Redundancy** to **Locally Redundant Storage (LRS)**.

3. **Enable Data Lake Storage Gen2**:
   - Go to the **Advanced** tab.
   - Enable the **Hierarchical Namespace** option to configure the account as a **Data Lake Storage Gen2**.

4. **Review and Create**:
   - Click on **Review + Create** and then **Create**.
   - Wait for the deployment to complete.

---

### Step 2: Upload a Log File
1. **Access the Storage Account**:
   - Once the Storage Account is created, navigate to it.

2. **Create a Container**:
   - Go to the **Containers** section under the Storage Account.
   - Click **+ Container** to create a new container.
   - Provide a **name** (e.g., `logs`) and click **Create**.

3. **Upload the Log File**:
   - Open the newly created container.
   - Click on the **Upload** button.
   - Select a log file from your local machine and upload it.
     - Example log file content:
       ```text
       CorrelationId, OperationName, Status
       abc123, CreateVM, Success
       xyz789, DeleteResource, Failed
       ```

---

## Benefits of Data Lake Storage Gen2
1. **Scalability**:
   - Handles massive datasets, making it ideal for big data analytics.
2. **Efficiency**:
   - Hierarchical namespace simplifies data organization and improves query performance.
3. **Integration**:
   - Works seamlessly with Azure analytics tools such as Azure Synapse Analytics and Databricks.

---

## Next Steps
In the next chapter, we will explore how to analyze the log file stored in the Data Lake using Azure analytics services.
