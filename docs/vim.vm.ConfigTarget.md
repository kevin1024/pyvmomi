vim.vm.ConfigTarget
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The ConfigTarget class contains information about "physical" devices that can   be used to back virtual devices.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| numCpus | int | None | None | Number of logical CPUs that can be used to run virtual machines. |
| numCpuCores | int | None | None | Number of physical CPU cores that are available to run virtual machines. |
| numNumaNodes | int | None | None | Number of NUMA nodes. |
| smcPresent | bool | None | None | Presence of System Management Controller, indicates the host is  Apple hardware, and thus capable of running Mac OS guest as VM. |
| datastore | [vim.vm.DatastoreInfo](vim.vm.DatastoreInfo.md "vim.vm.DatastoreInfo") | true | None | List of datastores available for virtual disks and associated storage. |
| network | [vim.vm.NetworkInfo](vim.vm.NetworkInfo.md "vim.vm.NetworkInfo") | true | None | List of networks available for virtual network adapters. |
| opaqueNetwork | [vim.vm.OpaqueNetworkInfo](vim.vm.OpaqueNetworkInfo.md "vim.vm.OpaqueNetworkInfo") | true | None | List of opaque networks available for virtual network adapters. |
| distributedVirtualPortgroup | [vim.dvs.DistributedVirtualPortgroupInfo](vim.dvs.DistributedVirtualPortgroupInfo.md "vim.dvs.DistributedVirtualPortgroupInfo") | true | None | List of networks available from DistributedVirtualSwitch for virtual    network adapters. |
| distributedVirtualSwitch | [vim.dvs.DistributedVirtualSwitchInfo](vim.dvs.DistributedVirtualSwitchInfo.md "vim.dvs.DistributedVirtualSwitchInfo") | true | None | List of distributed virtual switch available for virtual network    adapters. |
| cdRom | [vim.vm.CdromInfo](vim.vm.CdromInfo.md "vim.vm.CdromInfo") | true | None | List of CD-ROM devices available for use by virtual CD-ROMs.   Used for   <a href="vim.vm.device.VirtualCdrom.AtapiBackingInfo.md">VirtualCdromAtapiBackingInfo</a>. |
| serial | [vim.vm.SerialInfo](vim.vm.SerialInfo.md "vim.vm.SerialInfo") | true | None | List of serial devices available to support virtualization.   Used for   <a href="vim.vm.device.VirtualSerialPort.DeviceBackingInfo.md">VirtualSerialPortDeviceBackingInfo</a>. |
| parallel | [vim.vm.ParallelInfo](vim.vm.ParallelInfo.md "vim.vm.ParallelInfo") | true | None | List of parallel devices available to support virtualization.   Used for   <a href="vim.vm.device.VirtualParallelPort.DeviceBackingInfo.md">VirtualParallelPortDeviceBackingInfo</a>. |
| sound | [vim.vm.SoundInfo](vim.vm.SoundInfo.md "vim.vm.SoundInfo") | true | None | List of sound devices available to support virtualization.  Used for  <a href="vim.vm.device.VirtualSoundCard.DeviceBackingInfo.md">VirtualSoundCardDeviceBackingInfo</a>. |
| usb | [vim.vm.UsbInfo](vim.vm.UsbInfo.md "vim.vm.UsbInfo") | true | None | List of USB devices on the host that are available to support  virtualization.  Used for  <a href="vim.vm.device.VirtualUSB.USBBackingInfo.md">VirtualUSBUSBBackingInfo</a>. |
| floppy | [vim.vm.FloppyInfo](vim.vm.FloppyInfo.md "vim.vm.FloppyInfo") | true | None | List of floppy devices available for use by virtual floppies.   Used for   <a href="vim.vm.device.VirtualFloppy.DeviceBackingInfo.md">VirtualFloppyDeviceBackingInfo</a>. |
| legacyNetworkInfo | [vim.vm.LegacyNetworkSwitchInfo](vim.vm.LegacyNetworkSwitchInfo.md "vim.vm.LegacyNetworkSwitchInfo") | true | None | Legacy switch names when using the LegacyNetworkBacking types. |
| scsiPassthrough | [vim.vm.ScsiPassthroughInfo](vim.vm.ScsiPassthroughInfo.md "vim.vm.ScsiPassthroughInfo") | true | None | List of generic SCSI devices. |
| scsiDisk | [vim.vm.ScsiDiskDeviceInfo](vim.vm.ScsiDiskDeviceInfo.md "vim.vm.ScsiDiskDeviceInfo") | true | None | List of physical SCSI disks that can be used as targets for raw disk mapping   backings. |
| ideDisk | [vim.vm.IdeDiskDeviceInfo](vim.vm.IdeDiskDeviceInfo.md "vim.vm.IdeDiskDeviceInfo") | true | None | List of physical IDE disks that can be used as targets for raw disk backings. |
| maxMemMBOptimalPerf | int | None | None | Maximum recommended memory size, in MB, for creating a new virtual machine. |
| resourcePool | [vim.ResourcePool.RuntimeInfo](vim.ResourcePool.RuntimeInfo.md "vim.ResourcePool.RuntimeInfo") | true | None | Information about the current available resources on the current resource pool   for a virtual machine. This field is only populated from an Environment browser   obtained from a virtual machine. |
| autoVmotion | bool | true | None | Information whether a virtual machine with this ConfigTarget can auto vmotion.  This field is only populated from an Environment browser obtained from a   virtual machine. |
| pciPassthrough | [vim.vm.PciPassthroughInfo](vim.vm.PciPassthroughInfo.md "vim.vm.PciPassthroughInfo") | true | None | List of generic PCI devices. |
| sriov | [vim.vm.SriovInfo](vim.vm.SriovInfo.md "vim.vm.SriovInfo") | true | None | List of SRIOV devices. |
| vFlashModule | [vim.vm.VFlashModuleInfo](vim.vm.VFlashModuleInfo.md "vim.vm.VFlashModuleInfo") | true | None | List of vFlash modules. |


