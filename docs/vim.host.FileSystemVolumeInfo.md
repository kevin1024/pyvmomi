vim.host.FileSystemVolumeInfo
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.host.FileSystemVolumeInfo.md">HostFileSystemVolumeInfo</a> data object describes the file system volume   information for the host.   <p>   A file system volume refers to a storage abstraction that allows files   to be created and organized.  A host can have multiple file system   volumes.  File system volumes are typically mounted into a file namespace   that allows all files in mounted file systems to be addressable from the   host.   <p>   A file system volume is backed by disk storage.  It could span one or more   disks but need not use an entire disk.   <p>   A file system volume by definition must be mounted on the file system   in order to exist.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| volumeTypeList | string | true | None | The list of supported file system volume types. |
| mountInfo | [vim.host.FileSystemMountInfo](vim.host.FileSystemMountInfo.md "vim.host.FileSystemMountInfo") | true | None | The list of file system volumes mounted on the host. |


