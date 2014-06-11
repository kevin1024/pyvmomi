vim.Datastore.MountPathDatastorePair
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Contains a mapping of an old mount path and its corresponding   resignatured or remounted datastore

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| oldMountPath | string | None | None | Old file path where file system volume is mounted, which   should be <a href="vim.host.MountInfo.md#path">path</a> value in   <a href="vim.host.MountInfo.md">HostMountInfo</a> |
| datastore | [vim.Datastore](vim.Datastore.md "vim.Datastore") | None | None | The resignatured or remounted datastore corresponding to the oldMountPath |


