vim.vm.FileLayoutEx.FileInfo
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Basic information about a file.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | int | None | None | Key to reference this file. |
| name | string | None | None | Name of the file, including the complete datastore path. |
| type | string | None | None | Type of the file. <a href="vim.vm.FileLayoutEx.FileType.md">VirtualMachineFileLayoutExFileType</a> lists   all valid values. |
| size | long | None | None | Size of the file in bytes. |
| uniqueSize | long | true | None | Size of the file in bytes corresponding to the file blocks  that were allocated uniquely. In other words, if the underlying  storage supports sharing of file blocks across disk files, the  property corresponds to the size of the file blocks that were  allocated only in context of this file, i.e. it does not include  shared blocks that were allocated in other files.   This property will be unset if the underlying implementation  is unable to compute this information. One example of this  is when the file resides on a NAS datastore whose underlying  storage doesn't support this metric. In some cases the field  might be set but the value could be over-estimated due to  the inability of the NAS based storage to provide an  accurate value. |


