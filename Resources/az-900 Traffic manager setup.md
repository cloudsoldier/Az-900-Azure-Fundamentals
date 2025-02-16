
# Lab: Azure Traffic Manager Service with Azure Web Apps

## Objective
In this lab, you will deploy two Azure Web Apps in different regions, simulate a primary and secondary web application setup, and configure a simple HTML page for each web app. These apps will later be integrated with Azure Traffic Manager.

---

## Steps

### Step 1: Deploy the Primary Azure Web App
1. **Navigate to All Resources**:
   - In the Azure Portal, go to **All Resources**.
   - Click on **Create**.

2. **Create the Azure Web App**:
   - Choose **Azure Web App**.
   - Select an existing **Resource Group** or create a new one.
   - Provide a **unique name** for your primary web app (e.g., `primary-web-app`).
   - Choose **Runtime Stack** as `.NET 8`.
   - Select the **Region** as `North Europe`.
   - For **App Service Plan**:
     - Ensure the **pricing plan** is set to **Standard** (S1 or higher). 
     - If you're using a free trial and cannot select Standard, proceed with the Free Plan.

3. **Disable Monitoring**:
   - Skip **Application Insights**.

4. **Review and Create**:
   - Click on **Review + Create**, then **Create** to deploy the web app.

---

### Step 2: Deploy the Secondary Azure Web App
1. **Create a New Azure Web App**:
   - Repeat the steps in Step 1 to create another Azure Web App.
   - Use the same **Resource Group** as the primary app.
   - Provide a **unique name** for your secondary web app (e.g., `secondary-web-app`).
   - Choose `.NET 8` for the runtime stack.
   - Select the **Region** as `UK South`.

2. **Ensure Separate App Service Plan**:
   - Create a new **App Service Plan** for this region.
   - Set the plan to **Standard**.

3. **Disable Monitoring**:
   - Skip **Application Insights**.

4. **Review and Create**:
   - Click on **Review + Create**, then **Create** to deploy the secondary web app.

---

### Step 3: Configure the Primary Azure Web App
1. **Access the App Service Editor**:
   - Once the primary web app is deployed, go to its **Overview** page.
   - Scroll down to **Development Tools** and click on **App Service Editor (Preview)**.
   - Open the editor.

2. **Create a Default HTML Page**:
   - Navigate to the `WWWROOT` folder.
   - Right-click and select **Create New File**.
   - Name the file `Default.html`.

3. **Edit the HTML Page**:
   - Add the following code:
     ```html
     <html>
       <body>
         <h1>This is the Primary Web Application</h1>
       </body>
     </html>
     ```
   - The file is auto-saved.

4. **Test the Web App**:
   - Go to the **Overview** page.
   - Copy the **Default Domain URL** (e.g., `https://primary-web-app.azurewebsites.net`).
   - Append `/Default.html` to the URL and open it in a browser to verify the page.

---

### Step 4: Configure the Secondary Azure Web App
1. **Access the App Service Editor**:
   - Once the secondary web app is deployed, go to its **Overview** page.
   - Scroll down to **Development Tools** and click on **App Service Editor (Preview)**.
   - Open the editor.

2. **Create a Default HTML Page**:
   - Navigate to the `WWWROOT` folder.
   - Right-click and select **Create New File**.
   - Name the file `Default.html`.

3. **Edit the HTML Page**:
   - Add the following code:
     ```html
     <html>
       <body>
         <h1>This is the Secondary Web Application</h1>
       </body>
     </html>
     ```
   - The file is auto-saved.

4. **Test the Web App**:
   - Go to the **Overview** page.
   - Copy the **Default Domain URL** (e.g., `https://secondary-web-app.azurewebsites.net`).
   - Append `/Default.html` to the URL and open it in a browser to verify the page.

---

### Step 5: Verify the Setup
1. Open both the primary and secondary web applications in your browser using their respective URLs.
   - **Primary Web App**: `https://<primary-web-app>.azurewebsites.net/Default.html`
   - **Secondary Web App**: `https://<secondary-web-app>.azurewebsites.net/Default.html`

2. Ensure the HTML pages display the correct content for each app.

---

### Next Steps
Proceed to the next chapter to integrate these web applications with the **Azure Traffic Manager Service**.

