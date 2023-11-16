# az-104

Exam AZ-104

q11 :
Note: The question is included in a number of questions that depicts the identical set-up. However, every question has a distinctive result. Establish if the solution satisfies the requirements.
Your company has an Azure Active Directory (Azure AD) tenant named weyland.com that is configured for hybrid coexistence with the on-premises Active
Directory domain.
You have a server named DirSync1 that is configured as a DirSync server.
You create a new user account in the on-premise Active Directory. You now need to replicate the user information to Azure AD immediately.
Solution: You restart the NetLogon service on a domain controller.
Does the solution meet the goal?
    • A. Yes
    • B. No
       
If you need to manually run a sync cycle, then from PowerShell run Start-ADSyncSyncCycle -PolicyType Delta.


Q12:i1
Your company has a Microsoft Azure subscription.
The company has datacenters in Los Angeles and New York.
You are configuring the two datacenters as geo-clustered sites for site resiliency.
You need to recommend an Azure storage redundancy option.
You have the following data storage requirements:
✑ Data must be stored on multiple nodes.
✑ Data must be stored on nodes in separate geographic locations.
✑ Data can be read from the secondary location as well as from the primary location.
Which of the following Azure stored redundancy options should you recommend?
    • A. Geo-redundant storage
    • B. Read-only geo-redundant storage Most Voted
    • C. Zone-redundant storage
    • D. Locally redundant storage


Question #13Topic 1
Note: The question is included in a number of questions that depicts the identical set-up. However, every question has a distinctive result. Establish if the solution satisfies the requirements.
Your company has an azure subscription that includes a storage account, a resource group, a blob container and a file share.
A colleague named Jon Ross makes use of a solitary Azure Resource Manager (ARM) template to deploy a virtual machine and an additional Azure Storage account.
You want to review the ARM template that was used by Jon Ross.
Solution: You access the Virtual Machine blade.
Does the solution meet the goal?
    • A. Yes
    • B. No Most Voted

Question #14Topic 1
Note: The question is included in a number of questions that depicts the identical set-up. However, every question has a distinctive result. Establish if the solution satisfies the requirements.
Your company has an azure subscription that includes a storage account, a resource group, a blob container and a file share.
A colleague named Jon Ross makes use of a solitary Azure Resource Manager (ARM) template to deploy a virtual machine and an additional Azure Storage account.
You want to review the ARM template that was used by Jon Ross.
Solution: You access the Resource Group blade.
Does the solution meet the goal?
    • A. Yes Most Voted
    • B. No

Question #15Topic 1
Note: The question is included in a number of questions that depicts the identical set-up. However, every question has a distinctive result. Establish if the solution satisfies the requirements.
Your company has an azure subscription that includes a storage account, a resource group, a blob container and a file share.
A colleague named Jon Ross makes use of a solitary Azure Resource Manager (ARM) template to deploy a virtual machine and an additional Azure Storage account.
You want to review the ARM template that was used by Jon Ross.
Solution: You access the Container blade.
Does the solution meet the goal?
    • A. Yes
    • B. No Most Voted

Question #16Topic 1
Your company has three virtual machines (VMs) that are included in an availability set.
You try to resize one of the VMs, which returns an allocation failure message.
It is imperative that the VM is resized.
Which of the following actions should you take?
A. You should only stop one of the VMs.
B. You should stop two of the VMs.
C. You should stop all three VMs. Most Voted
D. You should remove the necessary VM from the availability set.
Correct Answer: C 🗳️
If the VM you wish to resize is part of an availability set, then you must stop all VMs in the availability set before changing the size of any VM in the availability set.
The reason all VMs in the availability set must be stopped before performing the resize operation to a size that requires different hardware is that all running VMs in the availability set must be using the same physical hardware cluster. Therefore, if a change of physical hardware cluster is required to change the VM size then all VMs must be first stopped and then restarted one-by-one to a different physical hardware clusters.
Reference:
https://azure.microsoft.com/es-es/blog/resize-virtual-machines/


Question #17Topic 1
You have an Azure virtual machine (VM) that has a single data disk. You have been tasked with attaching this data disk to another Azure VM.
You need to make sure that your strategy allows for the virtual machines to be offline for the least amount of time possible.
Which of the following is the action you should take FIRST?
A. Stop the VM that includes the data disk. correct
B. Stop the VM that the data disk must be attached to.
C. Detach the data disk. Most Voted
D. Delete the VM that includes the data disk


Question #18Topic 1
Your company has an Azure subscription.
You need to deploy a number of Azure virtual machines (VMs) using Azure Resource Manager (ARM) templates. You have been informed that the VMs will be included in a single availability set.
You are required to make sure that the ARM template you configure allows for as many VMs as possible to remain accessible in the event of fabric failure or maintenance.
Which of the following is the value that you should configure for the platformFaultDomainCount property?
A. 10
B. 30
C. Min Value
D. Max Value Most Voted
 
Correct Answer: D 🗳️
The number of fault domains for managed availability sets varies by region - either two or three per region.
Reference:
https://docs.microsoft.com/en-us/azure/virtual-machines/windows/manage-availability
Community vote distribution


Question #19Topic 1
Your company has an Azure subscription.
You need to deploy a number of Azure virtual machines (VMs) using Azure Resource Manager (ARM) templates. You have been informed that the VMs will be included in a single availability set.
You are required to make sure that the ARM template you configure allows for as many VMs as possible to remain accessible in the event of fabric failure or maintenance.
Which of the following is the value that you should configure for the platformUpdateDomainCount property?
A. 10
B. 20 Most Voted
C. 30
D. 40
 
Correct Answer: B 🗳️
Each virtual machine in your availability set is assigned an update domain and a fault domain by the underlying Azure platform. For a given availability set, five non-user-configurable update domains are assigned by default (Resource Manager deployments can then be increased to provide up to 20 update domains) to indicate groups of virtual machines and underlying physical hardware that can be rebooted at the same time.



question 20 
DRAG DROP -
You have downloaded an Azure Resource Manager (ARM) template to deploy numerous virtual machines (VMs). The ARM template is based on a current VM, but must be adapted to reference an administrative password.
You need to make sure that the password cannot be stored in plain text.
You are preparing to create the necessary components to achieve your goal.
Which of the following should you create to achieve your goal? Answer by dragging the correct option from the list to the answer area.
sol: key volt + acces control

Question #21Topic 1
Your company has an Azure Active Directory (Azure AD) tenant that is configured for hybrid coexistence with the on-premises Active Directory domain.
The on-premise virtual environment consists of virtual machines (VMs) running on Windows Server 2012 R2 Hyper-V host servers.
You have created some PowerShell scripts to automate the configuration of newly created VMs. You plan to create several new VMs.
You need a solution that ensures the scripts are run on the new VMs.
Which of the following is the best solution?
A. Configure a SetupComplete.cmd batch file in the %windir%\setup\scripts directory. Most Voted
B. Configure a Group Policy Object (GPO) to run the scripts as logon scripts.
C. Configure a Group Policy Object (GPO) to run the scripts as startup scripts.
D. Place the scripts in a new virtual hard disk (VHD).
 
Correct Answer: A 🗳️
After you deploy a Virtual Machine you typically need to make some changes before it's ready to use. This is something you can do manually or you could use
Remote PowerShell to automate the configuration of your VM after deployment for example.
But now there's a third alternative available allowing you customize your VM: the CustomScriptextension.
This CustomScript extension is executed by the VM Agent and it's very straightforward: you specify which files it needs to download from your storage account and which file it needs to execute. You can even specify arguments that need to be passed to the script. The only requirement is that you execute a .ps1 file.
Reference:
https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/add-a-custom-script-to-windows-setup



Question #22Topic 1
Your company has an Azure Active Directory (Azure AD) tenant that is configured for hybrid coexistence with the on-premises Active Directory domain.
You plan to deploy several new virtual machines (VMs) in Azure. The VMs will have the same operating system and custom software requirements.
You configure a reference VM in the on-premise virtual environment. You then generalize the VM to create an image.
You need to upload the image to Azure to ensure that it is available for selection when you create the new Azure VMs.
Which PowerShell cmdlets should you use?
A. Add-AzVM
B. Add-AzVhd Most Voted
C. Add-AzImage
D. Add-AzImageDataDisk
 
Correct Answer: B 🗳️
The Add-AzVhd cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.
Reference:
https://docs.microsoft.com/en-us/azure/virtual-machines/windows/upload-generalized-managed

DRAG DROP -
Your company has an Azure subscription that includes a number of Azure virtual machines (VMs), which are all part of the same virtual network.
Your company also has an on-premises Hyper-V server that hosts a VM, named VM1, which must be replicated to Azure.
Which of the following objects that must be created to achieve this goal? Answer by dragging the correct option from the list to the answer area. 
sol : 
For physical servers
- Storage Account
- Azure Recovery Services Vault
- Replication policy
https://docs.microsoft.com/en-us/azure/site-recovery/physical-azure-disaster-recovery
For Hyper-v server
- Hyper-V site
- Azure Recovery Services Vault
- Replication policy
https://docs.microsoft.com/en-nz/azure/site-recovery/hyper-v-prepare-on-premises-tutorial

