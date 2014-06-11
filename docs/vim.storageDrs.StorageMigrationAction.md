vim.storageDrs.StorageMigrationAction
=====================================
inherits from [vim.cluster.Action](docs/vim.cluster.Action.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Describes a single storage migration action. The storage migration   action applies either to a virtual machine or a set of virtual disks.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | None | None | Virtual machine reference. |
| relocateSpec | [vim.vm.RelocateSpec](vim.vm.RelocateSpec.md "vim.vm.RelocateSpec") | None | None | Specification for moving a virtual machine or a set of virtual disks   to a different datastore. |
| source | [vim.Datastore](vim.Datastore.md "vim.Datastore") | None | None | Source datastore. |
| destination | [vim.Datastore](vim.Datastore.md "vim.Datastore") | None | None | Destination datastore. |
| sizeTransferred | long | None | None | The amount of data to be transferred.   Unit: KB. |
| spaceUtilSrcBefore | float | true | None | Space utilization on the source datastore before storage migration.   Unit: percentage. For example, if set to 70.0, space utilization is 70%.   If not set, the value is not available. |
| spaceUtilDstBefore | float | true | None | Space utilization on the destination datastore before storage migration.   Unit: percentage. For example, if set to 70.0, space utilization is 70%.   If not set, the value is not available. |
| spaceUtilSrcAfter | float | true | None | Expected space utilization on the source datastore after storage migration.   Unit: percentage. For example, if set to 70.0, space utilization is 70%.   If not set, the value is not available. |
| spaceUtilDstAfter | float | true | None | Expected space utilization on the destination datastore after storage migration.   Unit: percentage. For example, if set to 70.0, space utilization is 70%.   If not set, the value is not available. |
| ioLatencySrcBefore | float | true | None | I/O latency on the source datastore before storage migration.   Unit: millisecond.   If not set, the value is not available. |
| ioLatencyDstBefore | float | true | None | I/O latency on the destination datastore before storage migration.   Unit: millisecond.   If not set, the value is not available. |


