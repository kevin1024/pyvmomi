vim.DistributedVirtualSwitch.BackupRestoreCapability
====================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


The <a href="vim.DistributedVirtualSwitch.BackupRestoreCapability.md">DVSBackupRestoreCapability</a> data object   describes backup, restore, and rollback capabilities for distributed virtual   switches and distributed virtual portgroups.   Backup and restore capabilities are indicated for <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.   Rollback capability is indicated for <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>   and <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| backupRestoreSupported | bool | None | None | Indicates whether backup, restore, and rollback are supported. |


