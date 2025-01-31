
Using Azure PowerShell modules - Resources
The following can be used as a reference for the prior chapter

1. The following link can be used as a reference to install Azure PowerShell modules

https://learn.microsoft.com/en-us/powershell/azure/install-azps-windows?view=azps-11.4.0&tabs=windowspowershell&pivots=windows-psgallery

2. The following command can be used to create a virtual machine using PowerShell

3. 
[ learn.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-powershell](https://learn.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-powershell)


Connect-AzAccount

New-AzVm -ResourceGroupName 'app-grp' -Name 'appvm' -Location 'uksouth' -Image 'MicrosoftWindowsServer:WindowsServer:2022-datacenter-azure-edition:latest' -VirtualNetworkName 'app-network' -SubnetName 'default' -SecurityGroupName 'app-nsg' -PublicIpAddressName 'app-ip' -OpenPorts 80,3389 -Size "Standard_D2s_v3"



