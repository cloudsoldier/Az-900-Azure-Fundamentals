# Lab: Creating a Build Pipeline in Azure DevOps

## Overview
In this lab, you will learn how to create and run a build pipeline in Azure DevOps to automatically build source code. This process is essential for preparing your code for deployment to production environments. The lab will use an ASP.NET project stored in Azure Repos as an example.

---

## Step-by-Step Instructions

### Step 1: Log in to Azure DevOps
1. Open your web browser and navigate to [Azure DevOps](https://dev.azure.com/).
2. Log in using your Azure DevOps account credentials.
3. Navigate to the Azure DevOps project containing your source code in Azure Repos.

### Step 2: Navigate to Pipelines
1. In the left-hand menu, click on **Pipelines**.
2. Click on **New Pipeline** to start creating your build pipeline.

### Step 3: Configure the Source Repository
1. When prompted, specify the location of your source code:
   - Choose **Azure Repos Git**.
   - Select the repository containing your ASP.NET project.

### Step 4: Define the Pipeline
1. Azure DevOps will suggest a pipeline template based on your project type.
   - Select the template for **ASP.NET** if not automatically chosen.
2. Review the generated YAML file:
   - The YAML file defines the steps required to build your source code.
   - It specifies the use of a **Windows-based agent** for the build process.
3. Optional: Delete any unnecessary tasks from the YAML file (e.g., test tasks if not needed).

### Step 5: Save and Run the Pipeline
1. Click on **Save and Run**.
2. Confirm by providing a commit message, and click **Save and Run** again.
3. Azure DevOps will create and start a job to build your source code.

### Step 6: Monitor the Build Process
1. Navigate to the **Jobs** section to monitor the progress of your build pipeline.
2. Wait for the build to complete (this may take a few minutes).

### Step 7: Verify the Build Output
1. Once the build is complete, review the output logs to ensure that the build was successful.
2. Confirm that the build artifacts were generated as expected.

---

## Key Takeaways
- Build pipelines in Azure DevOps enable automatic compilation and preparation of source code for deployment.
- YAML files provide a structured way to define build pipeline steps.
- The build process ensures that your source code is converted into a machine-executable format, ready for deployment.

---

## Next Steps
In the next lab, you will:
- Learn about release pipelines in Azure DevOps.
- Use the build artifacts generated in this lab to deploy your application to a production or staging environment.

---

## Clean Up
No cleanup is required for this lab as the build pipeline remains available for reuse.

