
# Lab: Publishing Source Code to Azure Repos

## Overview
In this lab, you will learn how to push source code to an Azure Repos repository using Git and Visual Studio Code. This is a beginner-friendly guide designed to demonstrate the integration of Git and Azure DevOps for source code versioning.

---

## Step-by-Step Instructions

### Step 1: Log in to Azure DevOps
1. Open your web browser and navigate to [Azure DevOps](https://dev.azure.com/).
2. Log in with your Azure DevOps account credentials.
3. Navigate to an existing Azure DevOps project or create a new one.

### Step 2: Set Up Git on Your Local Machine
1. Download and install Git:
   - Visit the [Git homepage](https://git-scm.com/).
   - Download the appropriate version for your operating system (e.g., Windows, MacOS).
   - Run the installer and accept the default settings.
2. Verify the installation:
   - Open a terminal or command prompt.
   - Run the command `git --version` to confirm Git is installed.

### Step 3: Create a New .NET Project in Visual Studio Code
1. Open **Visual Studio Code**.
2. Create a new .NET project:
   - Open the terminal in Visual Studio Code.
   - Run the command: `dotnet new webapp -n LearningApp`.
3. Navigate to the newly created project directory:
   - `cd LearningApp`
4. Launch the default web application:
   - Run the command: `dotnet run`.
   - Open the browser to view the running application.

### Step 4: Initialize Git in the Project Directory
1. Open the terminal in Visual Studio Code.
2. Navigate to your project directory (if not already there).
3. Run the following commands:
   - Initialize a Git repository: `git init`
   - Add project files: `git add .`
   - Commit files to the repository: `git commit -m "Initial commit"`

### Step 5: Add Azure Repos as a Remote Repository
1. In Azure DevOps, navigate to **Repos** > **Files**.
2. Copy the URL for the repository from the **Clone** section.
3. In the terminal, set the remote origin for your local repository:
   - `git remote add origin <repository_url>`
   - Replace `<repository_url>` with the URL copied from Azure DevOps.

### Step 6: Push Source Code to Azure Repos
1. Push the local repository to Azure Repos:
   - `git push -u origin master`
2. Verify the push by refreshing the Azure Repos page in your browser.
   - You should see all your source code files uploaded to the repository.

### Step 7: Explore Azure Repos Features
1. Navigate through the Azure Repos interface to explore:
   - File management.
   - Version history.
   - Branching and pull requests.

---

## Key Takeaways
- Azure Repos provides a centralized Git repository within Azure DevOps.
- Git enables version control and collaboration on code development.
- Visual Studio Code integrates seamlessly with Git for source control.

---

## Next Steps
- Explore advanced Git features such as branching and merging.
- Study for the **AZ-400** certification to gain deeper knowledge of Azure DevOps tools, including Azure Repos and Git integration.

---

## Clean Up
No cleanup is required for this lab.

---

**Instructor Guidance:** Emphasize the importance of source control and versioning in software development. Encourage students to practice using Git commands and explore Azure Repos featu
