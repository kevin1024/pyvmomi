vim.host.DiagnosticPartition
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type contains information about an available or active   diagnostic partition.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| storageType | string | None | None | Indicates the storage type of the diagnostic partition.<br>See <a href="vim.host.DiagnosticPartition.StorageType.md">DiagnosticPartitionStorageType</a><br> |
| diagnosticType | string | None | None | Indicates the type of the diagnostic partition.<br>See <a href="vim.host.DiagnosticPartition.DiagnosticType.md">DiagnosticPartitionType</a><br> |
| slots | int | None | None | The number of slots in the diagnostic partition. |
| id | [vim.host.ScsiDisk.Partition](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition") | None | None | Diagnostic partition identification information. |


