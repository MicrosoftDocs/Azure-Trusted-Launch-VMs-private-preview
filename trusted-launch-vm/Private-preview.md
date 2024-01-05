
# Azure Site Recovery support for Azure trusted launch VMs - Private preview

Azure Site Recovery has launched Private Preview support for Azure Trusted Launch VMs.  To enroll in Private Preview, please share your interest by filling up the <enrolment form>. 

> [!NOTE]
>
> - [Learn more](https://learn.microsoft.com/azure/virtual-machines/trusted-launch) about Azure trusted launch VMs. 
> - To deploy an Azure Trusted Launch VM, you can follow [these steps](https://learn.microsoft.com/azure/virtual-machines/trusted-launch-portal). 

## Support matrix

Find the support matrix for Azure Trusted Launch VMs :

- Available in all Azure Site Recovery supported Public Regions. Azure Government regions and Azure in China regions are not supported
- Only Windows OS is supported. Linux OS is not supported. 
- Multi-VM consistency is not supported. 
- Configuration of Private endpoints with recovery services vault is not supported. 
- Configuration of Managed Identity with recovery services vault is not supported. 
- Migration of Gen 2 Azure VMs to Trusted VMs is not supported. 
- If you enable Azure Site Recovery on VM with disks have public access disabled and / or private access disabled, customers will need to configure these settings again on the disks of failed over and failed back VM.  
- Enabling “Site Recovery” option in the “Management” tab in Create a new Virtual machine flow is not supported.  

## Azure Site Recovery for Trusted VMs 

You can follow the same steps for Azure Site Recovery with Trusted VMs as for Azure Site Recovery with Standard Azure VMs. 

To configure Azure Site Recovery on Trusted VMs to another region, you can review the documentation.  

To failover, re-protect, and failback, you can review this documentation.  

> [!NOTE]
>
> We do not recommend Private Preview with production workloads. Please use private preview with dev / test workloads only. 
> There will be no migration channel supported from private preview to public preview / GA. So, customers might need to disable Azure Site Recovery on the Trusted VMs on which they have enabled it during private preview and re-enable Azure Site Recovery post the Public Preview / GA. 

## Contact 

In case of any queries, please reach out to askasr@microsoft.com. 