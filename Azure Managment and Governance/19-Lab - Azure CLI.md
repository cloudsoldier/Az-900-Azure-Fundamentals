 az vm create --resource-group kashrg --name linuxvm --image "Canonical:0001-com-ubuntu-minimal-jammy:minimal-22_04-lts-gen2:latest" --admin-username linuxadmin --admin-password AzureMicrosoft@123 --public-ip-sku Standard

 <img width="957" alt="image" src="https://github.com/user-attachments/assets/aab4538b-56b1-4df7-a446-e7404698df69" />

 az vm delete --resource-group kashrg --name linuxvm

 
# Azure Command-Line Interface (CLI) Lecture Notes

## Introduction

In this chapter, we will explore one of the ways to interact with Azure resources using the **Azure Command-Line Interface (Azure CLI)**. Azure CLI is a free command-line tool that allows users to manage and interact with Azure resources efficiently.

## Compatibility

Azure CLI is compatible with multiple operating systems:
- **Windows**
- **MacOS**
- **Linux**

It is especially useful for administrators who need to automate tasks and create scripts to manage Azure resources.

## Installing Azure CLI

To start using Azure CLI, it must be installed on your system. The installation process varies depending on the operating system:

### Installation on Windows
1. Download the latest **MSI installer** (64-bit version) from Microsoft's official site.
2. Save the installer to the **Downloads** folder.
3. Once the download is complete, start the installation process.
4. Accept the license agreement and click on the **Install** button.
5. Wait for the installation to complete.

## Using Azure CLI

Once installed, we can start using Azure CLI to manage Azure resources.

### Logging into Azure
To authenticate with Azure, open **Command Prompt** and run the following command:

```sh
az login
```

- This command prompts you to log in using your Azure credentials.
- Once logged in, Azure CLI will display details of your account and resources.

## Creating a Virtual Machine with Azure CLI

To create a virtual machine, use the following command:

```sh
az vm create \
  --resource-group MyResourceGroup \
  --name MyLinuxVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --admin-password MySecurePassword! \
  --public-ip-sku Standard
```

### Explanation of Parameters:
- `--resource-group` → Specifies the resource group name.
- `--name` → Defines the virtual machine name.
- `--image` → Specifies the OS image (Ubuntu 22.04 in this case).
- `--admin-username` → Sets the administrator username.
- `--admin-password` → Defines the administrator password (Note: Secure methods like SSH keys are recommended for production).
- `--public-ip-sku Standard` → Assigns a public IP address.

Once the command executes successfully, the virtual machine will be created.

## Verifying the Created Resources

After executing the VM creation command, you can verify the created resources:
1. Navigate to the **Azure Portal**.
2. Click on **Refresh** to see the newly created resources.
3. If the resource names were not explicitly provided, Azure will generate default names.

## Deleting the Virtual Machine

Once testing is complete, it's a good practice to delete unnecessary resources to avoid charges. Use the following command to delete the virtual machine:

```sh
az vm delete --resource-group MyResourceGroup --name MyLinuxVM --yes
```

This command removes the specified virtual machine and associated resources.

## Conclusion

Azure CLI provides a powerful way to manage Azure resources from the command line. It is widely used for scripting, automation, and resource management. In this chapter, we covered:
- What Azure CLI is
- How to install Azure CLI
- How to log in and create a virtual machine
- How to verify and delete resources

By mastering Azure CLI, administrators can efficiently manage their cloud infrastructure and automate workflows.
