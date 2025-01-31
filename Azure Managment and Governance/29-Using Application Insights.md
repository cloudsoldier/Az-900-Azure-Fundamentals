
<img width="618" alt="image" src="https://github.com/user-attachments/assets/8c955e27-562d-41ca-bf58-80f8923068a7" />


# Lecture Notes: Application Insights for Live Application Monitoring

---

## **1. Overview of Application Insights**
- **Purpose**:  
  A feature of Azure Monitor for **application performance management (APM)**.  
  Collects telemetry data (e.g., request rates, failures, dependencies) from live web apps.  
- **Supported Languages**:  
  .NET, .NET Core, Java, Node.js, Python.  
- **Key Features**:  
  - **Live Metrics**: Real-time monitoring of app health.  
  - **Performance Tracing**: Identify bottlenecks.  
  - **Failure Analysis**: Diagnose errors and exceptions.  

---

## **2. Key Concepts**  
### **A. Application Insights Resource**  
- Stores and analyzes telemetry data.  
- Linked to a **Log Analytics Workspace** for long-term log storage.  

### **B. Instrumentation**  
- **Connection String**: Authorizes your app to send data to Application Insights.  
- **SDK Integration**: Add Application Insights packages to your codebase.  

### **C. Live Metrics**  
- Real-time dashboard showing:  
  - Request rates.  
  - Response times.  
  - Server CPU/memory usage.  

---

## **3. Step-by-Step Guide**  

### **Step 1: Create an Azure Web App with Application Insights**  
1. **Navigate to Azure Portal** → **Create a Resource** → **Web App**.  
2. Configure:  
   - **Runtime Stack**: .NET 8.  
   - **Pricing Plan**: Free tier (F1).  
   - **Enable Application Insights**:  
     - Create a new Application Insights resource during setup.  
3. **Review + Create** → **Create**.  

### **Step 2: Instrument a .NET Core Application**  
1. **Add NuGet Package**:  
   Update the `.csproj` file to include:  
   ```xml
   <ItemGroup>
     <PackageReference Include="Microsoft.ApplicationInsights.AspNetCore" Version="2.21.0" />
   </ItemGroup>
   ```  
2. **Modify `Program.cs`**:  
   Add Application Insights telemetry:  
   ```csharp
   builder.Services.AddApplicationInsightsTelemetry();
   ```  
3. **Configure Connection String**:  
   Add to `appsettings.json`:  
   ```json
   "ApplicationInsights": {
     "ConnectionString": "<Your-Connection-String>"
   }
   ```  
   - **Get Connection String**:  
     Go to your Application Insights resource → **Overview** → Copy connection string.  

### **Step 3: Deploy the Application**  
1. **Publish from Visual Studio Code**:  
   - Build the project.  
   - Deploy to the Azure Web App via the **Azure App Service** extension.  
2. **Verify Deployment**:  
   Access the web app’s URL (e.g., `https://<your-webapp-name>.azurewebsites.net`).  

### **Step 4: Monitor Live Metrics**  
1. In the Application Insights resource, go to **Live Metrics**.  
2. Interact with your live app (e.g., refresh the page).  
3. Observe real-time data:  
   - Incoming requests.  
   - Server resource utilization.  
   - Dependency calls (e.g., database queries).  

![Live Metrics Dashboard](https://via.placeholder.com/600x300?text=Live+Metrics+View)  

---

## **4. Key Observations**  
- **Telemetry Data**:  
  - Requests, dependencies, exceptions, traces.  
  - Available under **Performance** and **Failures** tabs after ingestion (may take 5-10 minutes).  
- **Log Analytics Integration**:  
  All data is stored in the linked workspace for advanced querying with KQL.  

---

## **5. Cleanup**  
1. **Delete Resources**:  
   - Application Insights resource.  
   - Web App + App Service Plan.  
   - Log Analytics Workspace (if created).  

---

## **6. Best Practices**  
1. **Use Recommended Settings**:  
   Enable profiling and snapshot debugging during instrumentation.  
2. **Monitor Retention Policies**:  
   Adjust data retention in Log Analytics Workspace to balance cost and compliance.  
3. **Alerting**:  
   Create alerts for critical metrics (e.g., high failure rates).  

---

## **7. Summary**  
- Application Insights provides **real-time visibility** into web app performance.  
- Instrumentation involves adding SDK packages and a connection string.  
- Critical for troubleshooting live applications and optimizing user experience.  

> **Next**: Explore **[Application Maps](https://learn.microsoft.com/en-us/azure/azure-monitor/app/app-map)** to visualize app dependencies.  

---

**AZ-900 Exam Focus**  
- Understand Application Insights as part of Azure’s **monitoring and management** tools.  
- Recognize its role in **proactive performance monitoring** for cloud applications.  
```
