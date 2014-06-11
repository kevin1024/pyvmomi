vim.host.DiskConfigurationResult
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Disk configuration result returns success or fault of the   operation on the disk.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| devicePath | string | true | None | The device path. See <a href="vim.host.ScsiDisk.md">ScsiDisk</a> |
| success | bool | true | None | Flag to indicate if the operation is successful |
| fault | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | 'fault' would be set if the operation was not successful |


