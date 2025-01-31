
# Lecture Notes: Using Azure Cloud Shell

## 1. **Overview of Azure Cloud Shell**
- **Purpose**: Browser-based shell to manage Azure services directly from the Azure portal.
- **Use Cases**:
  - No local installation of Azure CLI/PowerShell required.
  - Ideal for environments with restricted software installations.
- **Supported Shells**: Bash or PowerShell.

---

## 2. **Accessing Cloud Shell**
1. **Steps to Launch**:
   - Open the [Azure Portal](https://portal.azure.com).
   - Click the **Cloud Shell icon** (🖥️) in the top toolbar.
   - Choose **PowerShell** or **Bash**.
2. **Storage Setup**:
   - **Optional**: Mount an Azure Storage account to persist files (e.g., scripts, logs) across sessions.
   - Click **Apply** to start the session (no storage needed for temporary use).

---

## 3. **Key Features**
- **File Management**:
  - Upload/download files via the Cloud Shell toolbar.
  - Use `Upload/Download` buttons for file transfers.
- **Command Execution**:
  - Run Azure CLI, PowerShell, or Bash commands directly in the browser.
  - Example: Create a VM, manage storage, or deploy apps.
- **Session Persistence**:
  - Sessions timeout after 20 minutes of inactivity.
  - Use `az login` to reauthenticate if needed.

---

## 4. **Example: Create a VM with PowerShell**
```powershell
# Clear the screen
Clear-Host

# Create a new Azure VM
New-AzVm `
  -ResourceGroupName "DemoRG" `
  -Name "DemoVM" `
  -Location "EastUS" `
  -Image "Win2019Datacenter" `
  -Size "Standard_DS2_v2" `
  -Credential (Get-Credential) `
  -OpenPorts 3389
```
**Steps**:
1. Paste the command into Cloud Shell.
2. Enter a username and password when prompted.
3. Monitor deployment progress in the terminal.

---

## 5. **Best Practices**
- **Cleanup Resources**:
  - Delete temporary resources to avoid costs:
  ```powershell
  Remove-AzResourceGroup -Name "DemoRG" -Force
  ```
- **Storage Costs**:
  - Only mount storage accounts if file persistence is required.
- **Security**:
  - Always close the session after use (click **Disconnect**).

---

## 6. **Summary**
- Azure Cloud Shell enables browser-based Azure management.
- Use it for quick tasks, demos, or constrained environments.
- Supports both CLI and PowerShell with seamless Azure integration.

> **Next**: Explore Azure CLI commands in Cloud Shell or automate tasks with scripts.

