# Lecture Notes: Microsoft Sentinel Service

<img width="607" alt="image" src="https://github.com/user-attachments/assets/e4eacc33-ec4a-4890-958d-284c80d2091c" />

<img width="279" alt="image" src="https://github.com/user-attachments/assets/801d353d-24c0-47c8-b3ea-3e60f32412b5" />



## Overview
- **Microsoft Sentinel** is a cloud-based solution for:
  - **Security Information and Event Management (SIEM)**
  - **Security Orchestration, Automation, and Response (SOAR)**
- Key functionalities:
  - Collect logs from multiple sources.
  - Perform threat analysis using queries.
  - Automate responses to threats via Azure Logic Apps.

---

## Steps to Use Microsoft Sentinel

### Step 1: Create a Log Analytics Workspace
- Purpose: Collect data from various sources (e.g., software logs, audit logs, Azure activity logs).
- Process:
  1. Go to **Log Analytics Workspace**.
  2. Select an **existing resource group**.
  3. Provide a **unique name** for the workspace.
  4. Choose a **location** (e.g., North Europe).
  5. Add tags if needed, review, and create the workspace.

### Step 2: Set Up Microsoft Sentinel
- Attach Microsoft Sentinel to the log analytics workspace:
  1. Navigate to **Microsoft Sentinel**.
  2. Select the workspace created earlier.
  3. Enable Sentinel on top of the workspace.
  4. Start a **free trial** (if applicable).

---

## Features of Microsoft Sentinel

### Content Hub
- A centralized location for connecting data sources.
- Provides **solutions** to pull data from various platforms (e.g., Azure activity logs).
- Current solutions available: **343** (subject to growth).

### Example: Collecting Azure Activity Logs
1. Go to **Content Hub**.
2. Select **Azure Activity Logs**.
3. Install the solution to collect data.
4. Manage data and view collected logs in the workspace.

### Built-in Rules
- Monitor suspicious activities such as:
  - **Suspicious resource deployments**.
  - **Usage of Cloud Shell by new users**.
- Create custom rules to detect threats.

---

## Data Analysis
- Use the collected data for:
  - Monitoring activities in Azure.
  - Identifying and responding to suspicious behavior.
- Examples:
  - Collecting Azure activity logs via **Azure Monitor**.
  - Analyzing activities and safeguarding Azure resources.

---

## Summary
- Microsoft Sentinel enables:
  - Threat detection through data collection and analysis.
  - Automated responses via Azure Logic Apps.
- Workflow:
  - Collect data → Analyze logs → Respond to threats.
- Recommended for monitoring Azure resources and ensuring security compliance.

---

## Cleanup
- Delete all created resources after completing the tasks to avoid unnecessary costs.
