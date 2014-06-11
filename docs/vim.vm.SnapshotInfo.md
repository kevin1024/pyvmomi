vim.vm.SnapshotInfo
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The SnapshotInfo data object type provides all the information about the   hierarchy of snapshots in a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| currentSnapshot | [vim.vm.Snapshot](vim.vm.Snapshot.md "vim.vm.Snapshot") | true | None | Current snapshot of the virtual machine   <p>   This property is set by calling   <a href="vim.vm.Snapshot.md#revert">Snapshot.revert</a> or   <a href="vim.VirtualMachine.md#createSnapshot">VirtualMachine.createSnapshot</a>.   This property will be empty when the working snapshot is at the root   of the snapshot tree. |
| rootSnapshotList | [vim.vm.SnapshotTree](vim.vm.SnapshotTree.md "vim.vm.SnapshotTree") | None | None | Data for the entire set of snapshots for one virtual machine. |


