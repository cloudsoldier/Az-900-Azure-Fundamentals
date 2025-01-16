
# Lab: Creating and Using Azure DevTest Labs

## Overview
Azure DevTest Labs allow you to quickly provision development and test environments, implement quotas and policies, and enable automatic shutdown for cost management. In this lab, you will create a DevTest Lab and add virtual machines to simulate a virtual lab environment.

---

## Step-by-Step Instructions

### Step 1: Log in to Azure Portal
1. Open your web browser and navigate to [Azure Portal](https://portal.azure.com).
2. Log in with your Azure account credentials.

### Step 2: Create a DevTest Lab
1. In the Azure Portal, click on **Create a resource**.
2. Search for **DevTest Labs** and select it from the results.
3. Click **Create** to start setting up the lab.

### Step 3: Configure the Lab
1. Provide the following details:
   - **Lab Name**: Enter a unique name for your lab.
   - **Resource Group**: Select an existing resource group or create a new one.
   - **Region**: Choose the appropriate region.
2. (Optional) Enable **Automatic Shutdown** to save costs by shutting down unused machines.
3. Click **Next: Networking**.

### Step 4: Configure Networking
1. The service will automatically create a virtual network and subnet for managing the lab machines.
2. Review the networking settings and click **Next: Tags**.

### Step 5: Review and Create
1. Add any tags for organizational purposes.
2. Click **Review + Create** and then **Create**.
3. Wait for the lab to be deployed (this may take a few minutes).

### Step 6: Add Virtual Machines to the Lab
1. Navigate to your newly created DevTest Lab from **All Resources**.
2. Click on **+ Add** to create a new virtual machine.
3. Configure the virtual machine:
   - **Base Template**: Select an image (e.g., Windows 11 Enterprise).
   - **Username and Password**: Provide credentials for the VM.
   - **Size**: Select the desired VM size.
4. (Optional) Add artifacts:
   - Click on **Artifacts** to include additional software or configurations to the VM (e.g., Oracle Database).
5. Click **Create** to provision the virtual machine.

### Step 7: Manage and Use the Lab
1. Once the virtual machine is deployed, access it via Remote Desktop Protocol (RDP) or SSH, depending on the operating system.
2. Explore the features of DevTest Labs, such as:
   - Adding additional VMs.
   - Monitoring resource usage.
   - Implementing policies and quotas.

### Step 8: Clean Up Resources
1. Once you have completed the lab, delete the virtual machines and the DevTest Lab to avoid incurring additional charges.
2. Navigate to **All Resources** in the Azure Portal.
3. Delete the DevTest Lab and any associated resources.

---

## Key Features of DevTest Labs
- Quickly provision and manage virtual lab environments.
- Cost management features, such as automatic shutdown.
- Support for both Windows and Linux-based virtual machines.
- Integration with Azure Marketplace images and custom artifacts.

---

## Next Steps
- Experiment with different base templates and artifacts.
- Explore quota and policy configurations to better control resource usage.

---

**Instructor Guidance:** Highlight the cost-saving benefits of automatic shutdown and the flexibility of DevTest Labs for various development and testing scenarios. Encourage students to explore how this service can replace traditional physical lab environments.
