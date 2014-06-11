vim.host.DiagnosticPartition.CreateSpec
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The diagnostic create specification is used by the system to create a new   diagnostic partition on a SCSI disk.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| storageType | string | None | None | Indicates the storage type where the diagnostic partition   will be created.<br>See <a href="vim.host.DiagnosticPartition.StorageType.md">DiagnosticPartitionStorageType</a><br> |
| diagnosticType | string | None | None | Indicates the type of the diagnostic partition to be created.<br>See <a href="vim.host.DiagnosticPartition.DiagnosticType.md">DiagnosticPartitionType</a><br> |
| id | [vim.host.ScsiDisk.Partition](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition") | None | None | Diagnostic partition identification information. |
| partition | [vim.host.DiskPartitionInfo.Specification](vim.host.DiskPartitionInfo.Specification.md "vim.host.DiskPartitionInfo.Specification") | None | None | Partitioning specification. |
| active | bool | true | None | Indicates if the created diagnostic partition should be made the   active diagnostic partition.  If not supplied, the system will   decide whether or not the created specification is active. |


