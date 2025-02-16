

# Lab: Creating and Configuring an Azure CDN Profile

## Objective
In this lab, you will learn how to create an Azure CDN profile, register the required resource provider, and add an Azure Web App as an endpoint. The CDN profile will enhance global accessibility by caching content closer to users.

---

## Steps

### Step 1: Create a CDN Profile
1. **Navigate to All Resources**:
   - Open the Azure Portal.
   - Go to **All Resources** and click on **Create**.

2. **Search for CDN**:
   - In the search bar, type **CDN**.
   - Select **Front Door and CDN profiles** and click **Create**.

3. **Choose Azure CDN Offering**:
   - Under **Create a Front Door and CDN Profile**, select **Explore other offerings**.
   - Choose **Azure CDN** and select **Standard from Microsoft**.
   - Click **Continue**.

4. **Configure Basics**:
   - Select your **Resource Group**.
   - Provide a unique **Profile Name** for the CDN profile.
   - Note: The CDN profile is a global-level service.

5. **Review and Create**:
   - Click **Next: Tags** and then **Review + Create**.
   - If validation fails, proceed to Step 2 to resolve the issue.

---

### Step 2: Register the Resource Provider
1. **Navigate to Subscriptions**:
   - Go to **Subscriptions** in the Azure Portal.
   - Select your subscription.

2. **Register Resource Provider**:
   - Scroll down to **Resource Providers**.
   - Search for `Microsoft.CDN`.
   - Click **Register** to enable the resource provider.

3. **Verify Registration**:
   - Wait for the registration process to complete.
   - Refresh the page to ensure the provider is registered.

4. **Retry Creating the CDN Profile**:
   - Go back to creating the CDN profile.
   - Re-enter your settings and click **Review + Create**.
   - Click **Create** once validation passes.

---

### Step 3: Add an Endpoint to the CDN Profile
1. **Access the CDN Profile**:
   - Once the CDN profile is created, go to its **Overview** page.

2. **Add an Endpoint**:
   - Click on **Add Endpoint**.
   - Provide a unique **Name** for the endpoint.
   - Under **Origin Type**, select **App Service**.
   - Choose your **Primary Web App** as the origin.

3. **Save Endpoint**:
   - Leave other settings as default and click **Add**.
   - Wait for the endpoint to be added behind the CDN profile.

---

### Step 4: Test the CDN Profile
1. **Wait for Propagation**:
   - Wait for 5-10 minutes to ensure the CDN profile is fully configured and operational.

2. **Access the Web App via CDN Profile**:
   - Go to the **Overview** section of your CDN profile.
   - Copy the **DNS Name** of the endpoint.
   - Open the URL in a new tab and append `/Default.html` to access your web app.

3. **Verify Functionality**:
   - Confirm that the web application is accessible through the CDN profile.

---

## Notes
- **Global Performance Improvement**:
  - Users accessing the web application via the CDN profile will experience better response times, especially when located far from the original web app region.
- **CDN Caching**:
  - The CDN profile caches content at global PoP locations, improving accessibility and reducing latency for users across the world.

---

## Conclusion
You have successfully created an Azure CDN profile, registered the required resource provider, and added your Azure Web App as an endpoint. This configuration enables global users to access your application with reduced latency and improved performance.

