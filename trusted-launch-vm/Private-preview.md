
# Azure Site Recovery support for Azure Trusted Launch VMs (private preview)

[Azure Site Recovery](https://learn.microsoft.com/azure/site-recovery/site-recovery-overview) has launched private preview support for Azure Trusted Launch VMs.  To enroll in the private preview, share your interest by filling up this [enrolment form](https://aka.ms/AsrWindowsTrustedVmPrivatePreviewForm).

Trusted launch protects against advanced and persistent attack techniques. Trusted launch is composed of several, coordinated infrastructure technologies that can be enabled independently. Each technology provides another layer of defense against sophisticated threats.[Learn more about Trusted VMs](https://learn.microsoft.com/azure/virtual-machines/trusted-launch).

Deploy an Azure Trusted Launch VM, using [these steps](https://learn.microsoft.com/azure/virtual-machines/trusted-launch-portal).

## Support matrix

Find the support matrix for Azure Trusted Launch VMs with Azure Site Recovery:

- **Region**: Support for Azure Trusted Launch VMs is available in [all Azure Site Recovery supported public regions](https://learn.microsoft.com/azure/site-recovery/azure-to-azure-support-matrix#region-support). 
    > Support for Azure Trusted Launch VMs is not available in Azure Government regions and Azure in China regions.
- **Operating system**: Only Windows OS is supported. Linux OS is not supported.
- [Multi-VM consistency](https://learn.microsoft.com/azure/site-recovery/azure-to-azure-common-questions#multi-vm-consistency) is not supported.
- **Private endpoints**: [Configuration of Private endpoints](https://learn.microsoft.com/azure/site-recovery/azure-to-azure-how-to-enable-replication-private-endpoints) with recovery services vault is not supported.
- **Managed identity**: Configuration of Managed Identity with recovery services vault is not supported.
- Migration of Gen 2 Azure VMs to Trusted VMs is not supported.
- Azure Managed Disks with Public access disabled is not supported. 
- Enabling **Management** > **Site Recovery** option in *Create a new Virtual machine* flow isn't supported.  
- Replicating [Boot Integrity Monitoring](https://learn.microsoft.com/azure/virtual-machines/boot-integrity-monitoring-overview) state is not supported. Customers will need to enable it explicitly on the failed over VM, in case they want to use it. 

## Configure Azure Site Recovery for Trusted VMs

You can follow the same steps for configure Azure Site Recovery with Trusted VMs as you use for Azure Site Recovery with standard Azure VMs. 

- To configure Azure Site Recovery on Trusted VMs to another region, [follow these steps](https://learn.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-enable-replication).
- To failover, re-protect, and failback Azure VMs, [follow these steps](https://learn.microsoft.com/azure/site-recovery/azure-to-azure-tutorial-failover-failback).  

> [!NOTE]
>
> - We don't recommend Private Preview with production workloads. Use private preview with development or test workloads only. <br>
> - There'll be no migration channel supported from private preview to public preview or GA. So, customers might need to disable Azure Site Recovery on the Trusted VMs on which they have enabled it during private preview and re-enable Azure Site Recovery post the Public Preview / GA. 

## Contact 

In case of any queries, reach out to askasr@microsoft.com. 