vim.host.ResignatureRescanResult
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.host.ResignatureRescanResult.md">HostResignatureRescanResult</a> data object   identifies the newly created volume that is the result of a   resignature operation. This data object is contained in the   task object returned by the   <a href="vim.host.DatastoreSystem.md#resignatureUnresolvedVmfsVolume">ResignatureUnresolvedVmfsVolume_Task</a>   method.   <p>   When a client calls the resignature method, the Server   resignatures the volume, rescans the specified list of hosts,   and auto-mounts the volume on the other hosts that share the same   underlying storage LUNs.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| rescan | [vim.host.VmfsRescanResult](vim.host.VmfsRescanResult.md "vim.host.VmfsRescanResult") | true | None | List of VMFS Rescan operation results. |
| result | [vim.Datastore](vim.Datastore.md "vim.Datastore") | None | None | When an UnresolvedVmfsVolume has been resignatured, we want to return the   newly created VMFS Datastore. |


