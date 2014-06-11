vim.vm.DatastoreOption.FileSystemVolumeOption
=============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes a file system volume option for this  virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| fileSystemType | string | None | None | The type name of the file system volume information object for this  option.<br>See <a href="vim.host.FileSystemVolumeInfo.md">HostFileSystemVolumeInfo</a><br> |
| majorVersion | int | true | None | The major version of the file system volume information for this  option. If not specified, all versions of this file system are included  in this option. Currently, this value is set only for VMFS volumes. |


