vim.Datastore.Info
==================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Detailed information about a datastore.  This is a base type for derived types   that have more specific details about a datastore.<br>See <a href="vim.host.VmfsVolume.md">HostVmfsVolume</a><br>See <a href="vim.host.NasVolume.md">HostNasVolume</a><br>See <a href="vim.host.LocalFileSystemVolume.md">HostLocalFileSystemVolume</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The name of the datastore. |
| url | string | None | None | The unique locator for the datastore. |
| freeSpace | long | None | None | Free space of this datastore, in bytes. The server periodically updates this   value. It can be explicitly refreshed with the Refresh operation. |
| maxFileSize | long | None | None | The maximum size of a file that can reside on this file system volume. |
| maxVirtualDiskCapacity | long | true | None | The maximum capacity of a virtual disk which can be created on this volume. |
| timestamp | datetime | true | None | Time when the free-space and capacity values in <a href="vim.Datastore.Info.md">DatastoreInfo</a> and   <a href="vim.Datastore.Summary.md">DatastoreSummary</a> were updated. |
| containerId | string | true | None | The unique container ID of the datastore, if applicable. |


