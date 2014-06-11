vim.host.LowLevelProvisioningManager.VmMigrationStatus
======================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


The status of a virtual machine migration operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| migrationId | long | None | None | Unique identifier for this operation, currently it's unique   within one virtual center instance. |
| type | string | None | None | Manner in which the migration process is performed. The set of   possible values is described in   <a href="vim.host.VMotionManager.VMotionType.md">HostVMotionManagerVMotionType</a>. |
| source | bool | None | None | Whether the virtual machine is the source of the migration.   For disk only migration, the value is always true. |
| consideredSuccessful | bool | None | None | Whether the operation is considered successful. A migration   operation is considered successful if its switch over phase has   completed successfully.   <p>   More specifically, for an in-progress migration, it is considered   successful if it has had a sucessful switch over, otherwise it is   considered unsuccessful. Likewise, the status of a completed   migration operation is also based on the switch over completion   status.   <p>   The difference between a completed vs. in-progress migration with   the same consideredSuccessful property is that in the former case   the server is able to complete the clean up process thus leaves   nothing for the recovery process to clean up. |


