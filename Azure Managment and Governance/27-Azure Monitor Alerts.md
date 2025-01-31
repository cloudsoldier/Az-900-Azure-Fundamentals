
<img width="749" alt="image" src="https://github.com/user-attachments/assets/36c0cff9-a593-4518-8939-f19c714095c5" />



# Lab: Create Metrics Alerts in Azure Monitor

---

## **Objective**  
Learn to monitor Azure VM metrics and create threshold-based alerts using Azure Monitor.

---

## **Prerequisites**  
- An active Azure account.  
- A deployed Azure Virtual Machine (VM).  

---

## **Lab Steps**  

### **1. Access Metrics in Azure Monitor**  
1. **Navigate to Azure Portal** → **Virtual Machines** → Select your VM.  
2. Under **Monitoring**, click **Metrics**.  
3. **Explore Metrics**:  
   - Select **Percentage CPU** to view CPU utilization.  
   - Switch to **Available Memory Bytes** or **Network In Total** (bytes received).  

![Azure Metrics Explorer](https://via.placeholder.com/600x300?text=Azure+Metrics+Explorer+View)

---

### **2. Create an Alert Rule for Network Traffic**  
1. In your VM’s **Monitoring** section, click **Alerts** → **New Alert Rule**.  
2. **Select Resource**: Confirm your VM is the target resource.  
3. **Condition**:  
   - Click **Add Condition** → Search for **Network In Total** → Select it.  
   - Set the threshold to **Greater than 50 bytes** (⚠️ Note: This is intentionally low for testing).  
   - Configure evaluation: **1 minute** frequency over **5 minutes**.  
4. **Action Group**:  
   - Click **Create Action Group**.  
   - Name: `HighNetworkAlert-Group`.  
   - **Notifications**:  
     - Notification Type: **Email/SMS/Push/Voice**.  
     - Enter your email address.  
   - **Save** the action group.  
5. **Alert Details**:  
   - Name: `High-Network-Traffic-Alert`.  
   - Severity: **Sev 3** (for testing).  
6. **Review + Create**: Validate settings and create the alert.  

---

### **3. Test the Alert**  
1. **Trigger the Alert**:  
   - Generate network traffic to your VM (e.g., SSH/RDP into the VM and download a file).  
2. **Check Email**:  
   - Within 5-10 minutes, you’ll receive an email notification.  
   - Example email content:  
     ```plaintext
     Alert: High-Network-Traffic-Alert  
     Condition: Network In Total > 50 bytes  
     Resource: <your-vm-name>  
     Observed Value: 1024 bytes  
     ```

---

### **4. Cleanup**  
1. **Delete the Alert Rule**:  
   - Go to **Alerts** → **Alert Rules** → Select `High-Network-Traffic-Alert` → **Delete**.  
2. **Delete the Action Group**:  
   - Navigate to **Alerts** → **Action Groups** → Select `HighNetworkAlert-Group` → **Delete**.  

---

## **Key Concepts**  
- **Metrics**: Real-time numerical data (e.g., CPU, network traffic).  
- **Alerts**: Notifications triggered by metric thresholds.  
- **Action Groups**: Define who/how to notify when alerts fire.  

---

## **Notes**  
- ⚠️ **Low Threshold Warning**: 50 bytes is impractical for real-world use. Adjust thresholds based on actual needs (e.g., 1 MB).  
- **Activity Logs**: Track administrative actions (e.g., VM start/stop) under **Monitoring** → **Activity Log**.  

---

## **Next Steps**  
- Explore **Log Analytics Workspace** for advanced log queries.  
- Create dashboards in **Azure Monitor** to visualize multiple metrics.  
``` 

---

**Lab Success Criteria**  
- Receive an email alert when VM network traffic exceeds 50 bytes.  
- Understand how to configure metric thresholds and action groups.
