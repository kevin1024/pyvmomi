vim.host.LowLevelProvisioningManager.DiskLayoutSpec
===================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


File layout spec of a virtual disk. The disk could be either a base-disk  or a delta disk.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| controllerType | string | None | None | Disk controller type, e.g. vim.vm.device.VirtualSCSIController or  vim.vm.device.VirtualIDEController. |
| busNumber | int | None | None | Bus number associated with the controller for this disk. |
| unitNumber | int | None | None | Unit number of this disk on its controller. |
| srcFilename | string | None | None | Source disk filename in datastore path. |
| dstFilename | string | None | None | Destination filename in datastore path. |


