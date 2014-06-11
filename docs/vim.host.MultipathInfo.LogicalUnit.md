vim.host.MultipathInfo.LogicalUnit
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.host.MultipathInfo.LogicalUnit.md">HostMultipathInfoLogicalUnit</a> data object   represents a storage entity that provides disk blocks to a host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Linkable identifier. |
| id | string | None | None | Identifier of LogicalUnit.   <p>   Use this id to configure LogicalUnit multipathing policy using <a href="vim.host.StorageSystem.md#setMultipathLunPolicy">SetMultipathLunPolicy</a>. |
| lun | [vim.host.ScsiLun](vim.host.ScsiLun.md "vim.host.ScsiLun") | None | None | SCSI device corresponding to logical unit. |
| path | [vim.host.MultipathInfo.Path](vim.host.MultipathInfo.Path.md "vim.host.MultipathInfo.Path") | None | None | Array of paths available to access this LogicalUnit. |
| policy | [vim.host.MultipathInfo.LogicalUnitPolicy](vim.host.MultipathInfo.LogicalUnitPolicy.md "vim.host.MultipathInfo.LogicalUnitPolicy") | None | None | Policy that the logical unit should use when selecting a path. |
| storageArrayTypePolicy | [vim.host.MultipathInfo.LogicalUnitStorageArrayTypePolicy](vim.host.MultipathInfo.LogicalUnitStorageArrayTypePolicy.md "vim.host.MultipathInfo.LogicalUnitStorageArrayTypePolicy") | true | None | Policy used to determine how a storage device is accessed.  This policy   is currently immutable. |


