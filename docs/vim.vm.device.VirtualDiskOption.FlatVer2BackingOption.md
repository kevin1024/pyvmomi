vim.vm.device.VirtualDiskOption.FlatVer2BackingOption
=====================================================
inherits from [vim.vm.device.VirtualDeviceOption.FileBackingOption](docs/vim.vm.device.VirtualDeviceOption.FileBackingOption.md)


This data object type contains the available options when backing a virtual   disk using a host file with the flat file format used in VMware Server and   in ESX Server 2.x and greater.   Flat disks are pre-allocated, whereas sparse disks are grown as needed.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskMode | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | The disk mode. Valid disk modes are:   <ul>   <li><a href="vim.vm.device.VirtualDiskOption.DiskMode.md#persistent">persistent</a>   <li><a href="vim.vm.device.VirtualDiskOption.DiskMode.md#independent_persistent">independent_persistent</a>   <li><a href="vim.vm.device.VirtualDiskOption.DiskMode.md#independent_nonpersistent">independent_nonpersistent</a>   </ul><br>See <a href="vim.vm.device.VirtualDiskOption.DiskMode.md">VirtualDiskMode</a><br> |
| split | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate whether or not the host supports   allowing the client to select whether or not a disk   should be split. |
| writeThrough | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate whether or not the host supports   allowing the client to select "writethrough" as a mode for   virtual disks. Typically, this is available only for VMware Server Linux hosts. |
| growable | bool | None | None | Indicates whether or not this disk backing can be   extended to larger sizes through a reconfigure operation.   <p>   If set to true, reconfiguring this virtual disk   with a <a href="vim.vm.device.VirtualDisk.md#capacityInKB">capacityInKB</a> value greater   than its current value will grow the disk to the newly specified size. |
| hotGrowable | bool | None | None | Indicates whether or not this disk backing can be   extended to larger sizes through a reconfigure operation while   the virtual machine is powered on.   <p>   If set to true, reconfiguring this virtual disk   with a <a href="vim.vm.device.VirtualDisk.md#capacityInKB">capacityInKB</a> value greater   than its current value will grow the disk to the newly specified size   while the virtual machine is powered on. |
| uuid | bool | None | None | Flag to indicate whether this backing supports disk UUID property. |
| thinProvisioned | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate if this backing supports thin-provisioned disks.   <p>   When creating a thin-provisioned disk (or converting an existing disk to   to a thin-provisioned one), both the target datastore and the   host accessing it must support thin-provisioning. This flag indicates only   the host capability. See <a href="vim.Datastore.Capability.md#perFileThinProvisioningSupported">perFileThinProvisioningSupported</a>   for datastore capability. |
| eagerlyScrub | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate if this backing supports eager scrubbing. |
| deltaDiskFormat | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | Delta disk formats supported. Valid values are:   <ul>   <li><a href="vim.vm.device.VirtualDisk.DeltaDiskFormat.md#redoLogFormat">redoLogFormat</a>   <li><a href="vim.vm.device.VirtualDisk.DeltaDiskFormat.md#nativeFormat">nativeFormat</a>   </ul>   <p> |
| deltaDiskFormatsSupported | [vim.vm.device.VirtualDiskOption.DeltaDiskFormatsSupported](vim.vm.device.VirtualDiskOption.DeltaDiskFormatsSupported.md "vim.vm.device.VirtualDiskOption.DeltaDiskFormatsSupported") | None | None | Delta disk formats supported for each datastore type. |


