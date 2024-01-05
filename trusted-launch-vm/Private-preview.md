
# Azure Site Recovery support for Azure Trusted Launch VMs (private preview)

Azure Site Recovery has launched private preview support for Azure Trusted Launch VMs.  To enroll in the private preview, share your interest by filling up this <enrolment form>. 

- [Learn more](https://learn.microsoft.com/azure/virtual-machines/trusted-launch) about Azure trusted launch VMs. 
- Deploy an Azure Trusted Launch VM, using [these steps](https://learn.microsoft.com/azure/virtual-machines/trusted-launch-portal). 

## Support matrix

Find the support matrix for Azure Trusted Launch VMs with Azure Site Recovery:

- **Region**: Support for Azure Trusted Launch VMs is available in [all Azure Site Recovery supported public regions](https://learn.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix#region-support). 
    > Support for Azure Trusted Launch VMs is not available in Azure Government regions and Azure in China regions.
- **Operating system**: Only Windows OS is supported. Linux OS is not supported.
- [Multi-VM consistency](https://learn.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#multi-vm-consistency) is not supported.
- [Configuration of Private endpoints](https://learn.microsoft.com/azure/site-recovery/azure-to-azure-how-to-enable-replication-private-endpoints) with recovery services vault is not supported.
- Configuration of Managed Identity with recovery services vault is not supported.
- Migration of Gen 2 Azure VMs to Trusted VMs is not supported.
- If you enable Azure Site Recovery on VMs with disks have public access disabled and/or private access disabled, customers must configure these settings again on the disks of failed over and failed back VM.  
- Enabling **Management** > **Site Recovery** option in *Create a new Virtual machine* flow isn't supported.  

## Configure Azure Site Recovery for Trusted VMs

You can follow the same steps for configure Azure Site Recovery with Trusted VMs as you use for Azure Site Recovery with standard Azure VMs. 

- [Configure Azure Site Recovery on Trusted VMs to another region](https://learn.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-enable-replication).
- [Failover, re-protect, and failback Azure VMs](https://learn.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-failover-failback).  

> [!NOTE]
>
> We don't recommend Private Preview with production workloads. Use private preview with development or test workloads only. 
> There'll be no migration channel supported from private preview to public preview or GA. So, customers might need to disable Azure Site Recovery on the Trusted VMs on which they have enabled it during private preview and re-enable Azure Site Recovery post the Public Preview / GA. 

## Contact 

In case of any queries, reach out to askasr@microsoft.com. 