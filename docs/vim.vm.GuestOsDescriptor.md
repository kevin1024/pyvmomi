vim.vm.GuestOsDescriptor
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type contains information to describe a   particular guest operating system.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | Identifier (short name) for the guest operating system. |
| family | string | None | None | Family to which this guest operating system belongs. |
| fullName | string | None | None | Full name of the guest operating system.   For example, if the value of "id" is "win2000Pro", then   the value of "fullName" is "Windows 2000 Professional". |
| supportedMaxCPUs | int | None | None | Maximum number of processors supported for this guest. |
| numSupportedPhysicalSockets | int | None | None | Maximum number of sockets supported for this guest. |
| numSupportedCoresPerSocket | int | None | None | Maximum number of cores per socket for this guest. |
| supportedMinMemMB | int | None | None | Minimum memory requirements supported for this guest, in MB. |
| supportedMaxMemMB | int | None | None | Maximum memory requirements supported for this guest, in MB. |
| recommendedMemMB | int | None | None | Recommended default memory size for this guest, in MB. |
| recommendedColorDepth | int | None | None | Recommended default color depth for this guest. |
| supportedDiskControllerList | string | None | None | List of supported disk controller types for this guest. |
| recommendedSCSIController | string | true | None | Recommended default SCSI controller type for this guest. |
| recommendedDiskController | string | None | None | Recommended default disk controller type for this guest. |
| supportedNumDisks | int | None | None | Number of disks supported for this guest. |
| recommendedDiskSizeMB | int | None | None | Recommended default disk size for this guest, in MB. |
| recommendedCdromController | string | None | None | Recommended default CD-ROM type for this guest. |
| supportedEthernetCard | string | None | None | List of supported ethernet cards for this guest. |
| recommendedEthernetCard | string | true | None | Recommended default ethernet controller type for this guest. |
| supportsSlaveDisk | bool | true | None | Flag to indicate whether or not this guest can support   a disk configured as a slave. |
| cpuFeatureMask | [vim.host.CpuIdInfo](vim.host.CpuIdInfo.md "vim.host.CpuIdInfo") | true | None | Specifies the CPU feature compatibility masks. |
| smcRequired | bool | None | None | Flag that indicates wether the guest requires an SMC (Apple hardware).  This is logically equivalent to GuestOS = Mac OS |
| supportsWakeOnLan | bool | None | None | Flag to indicate whether or not this guest can support Wake-on-LAN. |
| supportsVMI | bool | None | None | Flag indicating whether or not this guest supports the virtual   machine interface. |
| supportsMemoryHotAdd | bool | None | None | Whether the memory size for this guest can be changed   while the virtual machine is running. |
| supportsCpuHotAdd | bool | None | None | Whether virtual CPUs can be added to this guest   while the virtual machine is running. |
| supportsCpuHotRemove | bool | None | None | Whether virtual CPUs can be removed from this guest   while the virtual machine is running. |
| supportedFirmware | string | None | None | Supported firmware types for this guest.    Possible values are described in   <a href="vim.vm.GuestOsDescriptor.FirmwareType.md">GuestOsDescriptorFirmwareType</a> |
| recommendedFirmware | string | None | None | Recommended firmware type for this guest.    Possible values are described in   <a href="vim.vm.GuestOsDescriptor.FirmwareType.md">GuestOsDescriptorFirmwareType</a> |
| supportedUSBControllerList | string | true | None | List of supported USB controllers for this guest. |
| recommendedUSBController | string | true | None | Recommended default USB controller type for this guest. |
| supports3D | bool | None | None | Whether this guest supports 3D graphics. |
| recommended3D | bool | None | None | Recommended 3D graphics for this guest. |
| smcRecommended | bool | None | None | Whether SMC (Apple hardware) is recommended for this guest. |
| ich7mRecommended | bool | None | None | Whether I/O Controller Hub is recommended for this guest. |
| usbRecommended | bool | None | None | Whether USB controller is recommended for this guest. |
| supportLevel | string | None | None | Support level of this Guest    Possible values are described in   <a href="vim.vm.GuestOsDescriptor.SupportLevel.md">GuestOsDescriptorSupportLevel</a> |
| supportedForCreate | bool | None | None | Whether or not this guest should be allowed for selection  during virtual machine creation. |
| vRAMSizeInKB | [vim.option.IntOption](vim.option.IntOption.md "vim.option.IntOption") | None | None | Video RAM size limits supported by this guest, in KB. |


