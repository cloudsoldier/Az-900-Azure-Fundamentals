```markdown
# Lab: Azure Traffic Manager - Priority Routing with Azure Web Apps

## Objective
In this lab, you will configure Azure Traffic Manager to route traffic between two Azure Web Apps deployed in different regions using the priority routing method. You will simulate a failure of the primary endpoint to observe Traffic Manager directing traffic to the secondary endpoint.

---

## Steps

### Step 1: Create a Traffic Manager Profile
1. **Navigate to All Resources**:
   - Open the Azure Portal.
   - Go to **All Resources** and click on **Create**.

2. **Search for Traffic Manager**:
   - In the Marketplace, search for **Traffic Manager profile**.
   - Click on the result and select **Create**.

3. **Configure Traffic Manager Profile**:
   - Provide a **unique name** for the Traffic Manager profile (e.g., `my-traffic-manager`).
     - This name will be appended with `.trafficmanager.net`.
   - Select the **Resource Group** used for your web apps.
   - Note: You do not need to specify a location for Traffic Manager as it is a global service.

4. **Choose Routing Method**:
   - Select **Priority** as the routing method.
   - Click **Review + Create** and then **Create**.

---

### Step 2: Configure Traffic Manager Health Monitoring
1. **Go to Configuration**:
   - Once the Traffic Manager profile is deployed, go to its **Configuration** section.

2. **Set Health Monitoring Protocol**:
   - Change the protocol to **HTTPS**.
   - Set the port to **443**.
   - Click **Save**.

---

### Step 3: Add Endpoints to Traffic Manager
1. **Add Primary Endpoint**:
   - Go to the **Endpoints** section in your Traffic Manager profile.
   - Click **Add** and select the following:
     - **Type**: Azure endpoint.
     - **Name**: PrimaryEndpoint.
     - **Target Resource Type**: App Service.
     - **Target Resource**: Select your primary web app.
     - **Priority**: Set to **1** (highest priority).
   - Click **Add**.

2. **Add Secondary Endpoint**:
   - Click **Add** again and select the following:
     - **Type**: Azure endpoint.
     - **Name**: SecondaryEndpoint.
     - **Target Resource Type**: App Service.
     - **Target Resource**: Select your secondary web app.
     - **Priority**: Set to **2** (lower priority).
   - Click **Add**.

3. **Verify Endpoint Status**:
   - Ensure both endpoints are online in the **Endpoints** section.

---

### Step 4: Test Traffic Manager
1. **Access the Traffic Manager DNS**:
   - Go to the **Overview** section of your Traffic Manager profile.
   - Copy the **DNS Name** (e.g., `my-traffic-manager.trafficmanager.net`).
   - Open it in a browser and append `/Default.html` to verify the primary web app is displayed.

2. **Simulate a Failure**:
   - Navigate to your primary web app in the Azure Portal.
   - Click **Stop** to simulate a failure.

3. **Observe Traffic Redirection**:
   - Refresh the browser for the Traffic Manager DNS URL.
   - Once the primary endpoint is detected as unavailable, the secondary web app will be displayed.

---

### Step 5: Restore the Primary Endpoint
1. **Restart Primary Web App**:
   - Navigate to the primary web app in the Azure Portal.
   - Click **Start** to bring the web app back online.

2. **Verify Traffic Redirection**:
   - Refresh the Traffic Manager DNS URL in your browser.
   - Ensure traffic is now routed back to the primary web app.

---

### Step 6: Cleanup Resources
1. **Delete Resources**:
   - Navigate to **All Resources**.
   - Delete all resources except the primary web app in North Europe.
   - Retain the primary web app for use in subsequent labs.

---

## Conclusion
You successfully configured Azure Traffic Manager with the priority routing method, added endpoints, and tested failover scenarios. The lab demonstrated Traffic Manager's ability to route traffic globally and ensure high availability.
```
