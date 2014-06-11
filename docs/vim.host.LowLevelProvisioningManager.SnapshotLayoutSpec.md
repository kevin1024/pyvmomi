vim.host.LowLevelProvisioningManager.SnapshotLayoutSpec
=======================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


File layout spec of a snapshot, including path to the vmsn file of the  snapshot and the layout of virtual disks when the snapshot was taken.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | int | None | None | The unique identifier of the snapshot |
| srcFilename | string | None | None | Name of the source snapshot file in datastore path. |
| dstFilename | string | None | None | Name of the destination snapshot file in datastore path. |
| disk | [vim.host.LowLevelProvisioningManager.DiskLayoutSpec](vim.host.LowLevelProvisioningManager.DiskLayoutSpec.md "vim.host.LowLevelProvisioningManager.DiskLayoutSpec") | true | None | Layout of each virtual disk of the virtual machine when the   snapshot was taken. |


