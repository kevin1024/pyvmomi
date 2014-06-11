vim.host.MountInfo
==================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.host.MountInfo.md">HostMountInfo</a> data object provides information related    to a configured mount point. This object does not include information    about the mounted file system. (See <a href="vim.host.FileSystemMountInfo.md">HostFileSystemMountInfo</a>.)

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| path | string | true | None | Local file path where file system volume is mounted, if applicable.   This path identifies the file system volume from the point of view   of the host. |
| accessMode | string | None | None | Access mode to the underlying file system for this host. |
| mounted | bool | true | None | The mount state of this mount point. For a discovered   volume, which is mounted, this is true. When this value is   unset, the default value is true. |
| accessible | bool | true | None | Flag that indicates if the datastore is currently accessible from   the host.   <p>   For the case of a standalone host, this property has the same value as   <a href="vim.Datastore.Summary.md">DatastoreSummary</a>.<a href="vim.Datastore.Summary.md#accessible">accessible</a>.   You can use the <a href="vim.Datastore.Summary.md">DatastoreSummary</a> property if the <a href="vim.host.MountInfo.md">HostMountInfo</a>   property is not set. The VirtualCenter Server will always make   sure the <a href="vim.Datastore.Summary.md">DatastoreSummary</a> property is set correctly. |
| inaccessibleReason | string | true | None | This optional property for inaccessible reason is reported only if   a datastore becomes inaccessible as reported by   <a href="vim.host.MountInfo.md#accessible">accessible</a> and   <a href="vim.Datastore.Summary.md">DatastoreSummary</a>.<a href="vim.Datastore.Summary.md#accessible">accessible</a>.    The values for inaccessible reason are defined in the enum   InaccessibleReason   This helps to determine host specific reason for datastore inaccessibility.    If the datastore becomes accessible following an inaccessible condition,   the property <a href="vim.host.MountInfo.md#inaccessibleReason">inaccessibleReason</a> will be unset. |


