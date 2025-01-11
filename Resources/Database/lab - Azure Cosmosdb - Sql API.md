
# Step-by-Step Guide: Working with Azure Cosmos DB

## Objective
Learn how to create an Azure Cosmos DB account, set up a database and container, and work with JSON-based documents.

---

## Steps

### Step 1: Create an Azure Cosmos DB Account
1. **Go to All Resources**:
   - Open the Azure Portal and click on **Create**.
   
2. **Search for Azure Cosmos DB**:
   - Search for **Azure Cosmos DB** in the Marketplace.
   - Choose **Azure Cosmos DB for NoSQL** as the API.

3. **Configure the Account**:
   - Select an existing **Resource Group**.
   - Provide a **unique account name** (e.g., `myappaccount123`).
   - Choose the **Region** (e.g., North Europe).
   - Leave the default **Free Tier** (1000 RUs and 25GB storage).

4. **Review and Create**:
   - Click on **Review + Create**.
   - Once validated, click **Create** and wait for deployment.

---

### Step 2: Set Up the Database and Container
1. **Access the Azure Cosmos DB Account**:
   - Once deployment is complete, go to the resource.

2. **Open Data Explorer**:
   - Click on **Data Explorer** in the left-hand menu.

3. **Create a New Database**:
   - In Data Explorer, select **New Container**.
   - Provide:
     - **Database Name**: e.g., `customersdb`.
     - **Container Name**: e.g., `customers`.

4. **Set Partition Key**:
   - Choose an attribute as the partition key (e.g., `customercity`).
     - Partitioning improves search efficiency by grouping data logically (e.g., all customers in "Chicago" in one partition).

5. **Create Database and Container**:
   - Scroll down and click **OK** to create the database and container.

---

### Step 3: Add Data to the Container
1. **Navigate to the Container**:
   - In Data Explorer, click on the **customers** container.

2. **Add Items**:
   - Go to the **Items** tab and click **New Item**.
   - Add JSON-based documents, e.g.:
     ```json
     {
       "customerid": "1",
       "customername": "John Doe",
       "customercity": "Chicago"
     }
     ```
   - Click **Save** to store the document.

3. **Repeat for Multiple Items**:
   - Add additional items as needed, e.g.:
     ```json
     {
       "customerid": "2",
       "customername": "Jane Smith",
       "customercity": "New York"
     }
     ```

---

### Step 4: Query the Data
1. **Execute Queries**:
   - Use SQL-like queries in the Data Explorer to retrieve data, e.g.:
     ```sql
     SELECT * FROM c
     ```
   - This retrieves all documents in the container.

---

### Step 5: Clean Up Resources
1. **Delete the Azure Cosmos DB Account**:
   - Go to **All Resources** and select the Azure Cosmos DB account.
   - Click **Delete**, enter the account name for confirmation, and click **Delete** again.

---

## Notes
- **Partitioning**:
  - Helps organize and retrieve large datasets efficiently.
- **JSON-Based Storage**:
  - Unlike traditional SQL databases, data is stored as JSON documents instead of rows and columns.
- **Free Tier**:
  - Suitable for small projects or learning, with 1000 RUs and 25GB included.

---

## Conclusion
You have successfully created an Azure Cosmos DB account, added data, and executed queries. This service is ideal for applications requiring high-speed, flexible, and globally distributed data storage.



# Lab: Azure Cosmos DB - SQL API - Resources

You can use the JSON items below to add to a Cosmos DB database based on the SQL API.

---

### JSON Items

1. **Item 1**:
   ```json
   {
     "customerid": "C1",
     "customername": "UserA",
     "customercity": "Chicago"
   }
   ```

2. **Item 2**:
   ```json
   {
     "customerid": "C2",
     "customername": "UserB",
     "customercity": "Chicago"
   }
   ```

3. **Item 3**:
   ```json
   {
     "customerid": "C3",
     "customername": "UserC",
     "customercity": "New York"
   }
   ```

---

## Instructions

1. Open your Azure Cosmos DB account in the Azure Portal.
2. Navigate to the **Data Explorer** section.
3. Select your **Database** and **Container**.
4. Add the above JSON items one by one:
   - Click **New Item**.
   - Copy and paste the JSON content.
   - Click **Save** to store each item in the container.
5. Repeat for all three items.
