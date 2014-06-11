vim.vm.FileLayoutEx.SnapshotLayout
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Layout of a snapshot.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | [vim.vm.Snapshot](vim.vm.Snapshot.md "vim.vm.Snapshot") | None | None | Reference to the snapshot. |
| dataKey | int | None | None | Key to the snapshot data file in <a href="vim.vm.FileLayoutEx.md#file">file</a>. |
| disk | [vim.vm.FileLayoutEx.DiskLayout](vim.vm.FileLayoutEx.DiskLayout.md "vim.vm.FileLayoutEx.DiskLayout") | true | None | Layout of each virtual disk of the virtual machine when the   snapshot was taken. |


