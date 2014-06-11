vim.vm.customization.Identification
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The Identification data object type provides information needed to join a workgroup   or domain.   <p>   The Identification data object type maps to the Identification key in the   <tt>sysprep.inf</tt> answer file. These values are transferred into the   <tt>sysprep.inf</tt> file that VirtualCenter stores on the target virtual disk. For   more detailed information, see the document <a href =  "http://www.microsoft.com/technet/prodtechnol/Windows2000Pro/deploy/unattend/default.mspx"   >Windows 2000 Unattended Setup Guide</a>.<br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| joinWorkgroup | string | true | None | The workgroup that the virtual machine should join. If this value is supplied,   then the domain name and authentication fields must be empty. |
| joinDomain | string | true | None | The domain that the virtual machine should join. If this value is supplied, then   domainAdmin and domainAdminPassword must also be supplied, and the workgroup   name must be empty. |
| domainAdmin | string | true | None | This is the domain user account used for authentication if the virtual machine   is joining a domain. The user does not need to be a domain administrator, but   the account must have the privileges required to add computers to the domain. |
| domainAdminPassword | [vim.vm.customization.Password](vim.vm.customization.Password.md "vim.vm.customization.Password") | true | None | This is the password for the domain user account used for authentication if the   virtual machine is joining a domain. |


