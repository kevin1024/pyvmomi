vim.vm.device.VirtualDiskOption.SparseVer2BackingOption
=======================================================
inherits from [vim.vm.device.VirtualDeviceOption.FileBackingOption](docs/vim.vm.device.VirtualDeviceOption.FileBackingOption.md)


This data object type contains the options available when backing a virtual   disk using a host file with the sparse file format from VMware Server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskMode | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | The disk mode. Valid disk modes are:   <ul>   <li><a href="vim.vm.device.VirtualDiskOption.DiskMode.md#persistent">persistent</a>   <li><a href="vim.vm.device.VirtualDiskOption.DiskMode.md#nonpersistent">nonpersistent</a>   <li><a href="vim.vm.device.VirtualDiskOption.DiskMode.md#undoable">undoable</a>   <li><a href="vim.vm.device.VirtualDiskOption.DiskMode.md#independent_persistent">independent_persistent</a>   <li><a href="vim.vm.device.VirtualDiskOption.DiskMode.md#independent_nonpersistent">independent_nonpersistent</a>   <li><a href="vim.vm.device.VirtualDiskOption.DiskMode.md#append">append</a>   </ul><br>See <a href="vim.vm.device.VirtualDiskOption.DiskMode.md">VirtualDiskMode</a><br> |
| split | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate whether or not the host supports   allowing the client to select whether or not a sparse disk   should be split. |
| writeThrough | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate whether or not the host supports   allowing the client to select "writethrough" as a mode for   virtual disks. Typically, this is available only for VMware Server Linux hosts. |
| growable | bool | None | None | Indicates whether or not this disk backing can be   extended to larger sizes through a reconfigure operation.   <p>   If set to true, reconfiguring this virtual disk   with a <a href="vim.vm.device.VirtualDisk.md#capacityInKB">capacityInKB</a> value greater   than its current value will grow the disk to the newly specified size. |
| hotGrowable | bool | None | None | Indicates whether or not this disk backing can be   extended to larger sizes through a reconfigure operation while   the virtual machine is powered on.   <p>   If set to true, reconfiguring this virtual disk   with a <a href="vim.vm.device.VirtualDisk.md#capacityInKB">capacityInKB</a> value greater   than its current value will grow the disk to the newly specified size   while the virtual machine is powered on. |
| uuid | bool | None | None | Flag to indicate whether this backing supports disk UUID property. |


