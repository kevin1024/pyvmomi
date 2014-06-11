vim.vm.SnapshotTree
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


SnapshotTree encapsulates all the read-only data produced by the snapshot.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| snapshot | [vim.vm.Snapshot](vim.vm.Snapshot.md "vim.vm.Snapshot") | None | None | The managed object for this snapshot. |
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | None | None | The virtual machine for which the snapshot was taken. |
| name | string | None | None | Name of the snapshot. |
| description | string | None | None | Description of the snapshot. |
| id | int | None | None | The unique identifier that distinguishes this snapshot from   other snapshots of the virtual machine. |
| createTime | datetime | None | None | The date and time the snapshot was taken. |
| state | [vim.VirtualMachine.PowerState](vim.VirtualMachine.PowerState.md "vim.VirtualMachine.PowerState") | None | None | The power state of the virtual machine when this snapshot was taken. |
| quiesced | bool | None | None | Flag to indicate whether or not the snapshot was created with   the "quiesce" option, ensuring a consistent state of the file system. |
| backupManifest | string | true | None | The relative path from the snapshotDirectory pointing to the backup   manifest. Available for certain quiesced snapshots only. |
| childSnapshotList | [vim.vm.SnapshotTree](vim.vm.SnapshotTree.md "vim.vm.SnapshotTree") | true | None | The snapshot data for all snapshots for which this snapshot is the parent. |
| replaySupported | bool | true | None | Flag to indicate whether this snapshot is associated with a recording  session on the virtual machine that can be replayed. |


