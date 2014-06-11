vim.vm.ReplicationConfigSpec.DiskSettings
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The ReplicationConfigSpec.DiskSettings object type encapsulates  the replication properties of a replicated disk of a replicated  virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | int | None | None | The disk's device key in the VM's configuration. Used to  uniquely identify the disk to be configured for replication  in the primary VM. |
| diskReplicationId | string | None | None | An opaque identifier that uniquely identifies a replicated  disk between primary and secondary sites. |


