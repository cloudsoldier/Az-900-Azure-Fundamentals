# Lab: Creating a Release Pipeline in Azure DevOps

## Overview
In this lab, you will create a release pipeline in Azure DevOps to automate the deployment of your build artifacts to an Azure Web App. This complements the build pipeline created earlier, demonstrating a complete CI/CD process.

---

## Step-by-Step Instructions

### Step 1: Prerequisites
- Ensure you have:
  - A build pipeline set up in Azure DevOps.
  - An Azure Web App created in your Azure account.

### Step 2: Log in to Azure DevOps
1. Open your web browser and navigate to [Azure DevOps](https://dev.azure.com/).
2. Log in using your Azure DevOps account credentials.

### Step 3: Navigate to Releases
1. In your Azure DevOps project, click on **Pipelines** > **Releases**.
2. Click **New Pipeline** to create a release pipeline.

### Step 4: Configure the Release Pipeline
1. Select a template:
   - Choose **Azure App Service deployment** and click **Apply**.
2. Name your pipeline for identification.

### Step 5: Add an Artifact
1. Click **Add an artifact**.
2. Select the build pipeline from which the release pipeline will consume artifacts.
3. Ensure the **Continuous Deployment Trigger** is enabled.
   - This ensures the release pipeline runs automatically after the build pipeline completes.

### Step 6: Configure the Deployment Stage
1. Click on the stage (e.g., **Stage 1**) to configure the deployment job.
2. Select **Azure App Service Deployment** as the task type.
3. Authorize your Azure subscription:
   - Click **Authorize** and log in with your Azure credentials.
4. Select the target Azure Web App.
5. Save your configuration.

### Step 7: Modify the Build Pipeline (if needed)
1. Navigate to your build pipeline and click **Edit**.
2. Ensure the YAML definition includes tasks to publish build artifacts for the release pipeline.
3. Save the changes and trigger the build pipeline.

### Step 8: Run the Release Pipeline
1. Return to your release pipeline and click **Create a release**.
2. Monitor the release process:
   - Navigate to **Releases** and select the running pipeline.
   - Verify that the deployment completes successfully.

### Step 9: Test the Deployment
1. Go to your Azure Web App in the Azure Portal.
2. Access the default domain for your web app.
3. Verify that the deployed application is running as expected.

### Step 10: Demonstrate Continuous Deployment
1. Make a change to your source code in Azure Repos (e.g., modify the index page of your application).
2. Commit the changes to trigger the build pipeline automatically.
3. Verify that the release pipeline is triggered after the build pipeline completes.
4. Check the Azure Web App to confirm the updated application is live.

### Step 11: Clean Up Resources
1. If no longer needed, delete your Azure DevOps project:
   - Go to **Project Settings** > **Delete Project**.
   - Enter the project name and confirm deletion.
2. Remove any associated Azure resources to avoid charges.

---

## Key Features of Release Pipelines
- Automates deployment to target environments.
- Integrates seamlessly with build pipelines for a CI/CD workflow.
- Supports various Azure services, including Azure Web Apps.

---

## Next Steps
- Explore advanced features such as approvals, deployment gates, and multi-environment deployments.
- Consider studying for the **AZ-400** certification to deepen your understanding of DevOps practices in Azure.

---

**Instructor Guidance:** Emphasize the importance of automating both build and release processes to ensure efficient and error-free deployments. Encourage students to experiment with changes in the source code to see how the pipelines handle updates.

