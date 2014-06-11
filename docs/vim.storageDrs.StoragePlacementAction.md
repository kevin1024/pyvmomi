vim.storageDrs.StoragePlacementAction
=====================================
inherits from [vim.cluster.Action](docs/vim.cluster.Action.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Describes a single storage initial placement action for placing a virtual  machine or a set of virtual disks on a datastore.  <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | true | None | Virtual machine reference.   It is possible that the VM has not been created, in which case,   this property is left unset. |
| relocateSpec | [vim.vm.RelocateSpec](vim.vm.RelocateSpec.md "vim.vm.RelocateSpec") | None | None | Specification for placing a virtual machine or a set of virtual disks   to a datastore. |
| destination | [vim.Datastore](vim.Datastore.md "vim.Datastore") | None | None | Target datastore. |
| spaceUtilBefore | float | true | None | Current space utilization on the target datastore.   Unit: percentage. For example, if set to 70.0, space utilization is 70%.   If not set, the value is not available. |
| spaceUtilAfter | float | true | None | Expected space utilization on the target datastore after placing the virtual disk.   Unit: percentage. For example, if set to 70.0, space utilization is 70%.   If not set, the value is not available. |
| ioLatencyBefore | float | true | None | Current I/O latency on the target datastore.   Unit: millisecond.   If not set, the value is not available. |


