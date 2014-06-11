vim.host.DatastoreBrowser.VmDiskInfo
====================================
inherits from [vim.host.DatastoreBrowser.FileInfo](docs/vim.host.DatastoreBrowser.FileInfo.md)


This data object type describes a virtual disk primary file.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskType | string | true | None | Disk type of the virtual disk.   <p>   The specified disk type is one of the backing information types for a virtual   disk.<br>See <a href="vim.vm.device.VirtualDisk.md">VirtualDisk</a><br> |
| capacityKb | long | true | None | The capacity of a virtual disk from the point of view of a virtual machine. |
| hardwareVersion | int | true | None | The hardware version of the virtual disk file. |
| controllerType | string | true | None | The controller type suitable for this virtual disk. |
| diskExtents | string | true | None | The extents of this virtual disk specified in absolute DS paths |
| thin | bool | true | None | Indicates if the disk is thin-provisioned |


