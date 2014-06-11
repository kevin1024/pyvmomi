vim.vm.FileLayout.SnapshotLayout
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Enumerates the set of files that make up a snapshot or redo-point

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | [vim.vm.Snapshot](vim.vm.Snapshot.md "vim.vm.Snapshot") | None | None | Identification of the snapshot |
| snapshotFile | string | None | None | A list of files that make up the snapshot state. These are relative   paths from the snapshotDirectory. A slash is always used as a   separator. |


