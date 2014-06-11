vim.StoragePod.Summary
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The <a href="vim.StoragePod.Summary.md">StoragePodSummary</a> data object   encapsulates runtime properties of a <a href="vim.StoragePod.md">StoragePod</a>.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The name of the storage pod. |
| capacity | long | None | None | Total capacity of this storage pod, in bytes. This value is the sum of the   capacity of all datastores that are part of this storage pod, and is updated   periodically by the server. |
| freeSpace | long | None | None | Total free space on this storage pod, in bytes. This value is the sum of the   free space on all datastores that are part of this storage pod, and is updated   periodically by the server. |


