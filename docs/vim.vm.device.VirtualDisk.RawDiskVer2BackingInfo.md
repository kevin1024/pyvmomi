vim.vm.device.VirtualDisk.RawDiskVer2BackingInfo
================================================
inherits from [vim.vm.device.VirtualDevice.DeviceBackingInfo](docs/vim.vm.device.VirtualDevice.DeviceBackingInfo.md)


This data object type contains information about backing a virtual disk by   using a host device, as used by VMware Server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| descriptorFileName | string | None | None | The name of the raw disk descriptor file. |
| uuid | string | true | None | Disk UUID for the virtual disk, if available. |
| changeId | string | true | None | The change ID of the virtual disk for the corresponding  snapshot or virtual machine. This can be used to track  incremental changes to a virtual disk. See   <a href="vim.VirtualMachine.md#queryChangedDiskAreas">QueryChangedDiskAreas</a>. |


