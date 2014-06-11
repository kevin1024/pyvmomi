vim.host.DiagnosticPartition.CreateOption
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object describes a disk that can be used to create a   diagnostic partition.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| storageType | string | None | None | Indicates the storage type of diagnostic partition to be created.<br>See <a href="vim.host.DiagnosticPartition.StorageType.md">DiagnosticPartitionStorageType</a><br> |
| diagnosticType | string | None | None | Indicates the type of the diagnostic partition to be created.<br>See <a href="vim.host.DiagnosticPartition.DiagnosticType.md">DiagnosticPartitionType</a><br> |
| disk | [vim.host.ScsiDisk](vim.host.ScsiDisk.md "vim.host.ScsiDisk") | None | None | The disk which has sufficient free space to contain a diagnostic   partition. |


