vim.vm.FileLayoutEx.DiskUnit
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Information about a single unit of a virtual disk, such as   the base-disk or a delta-disk.   <p>   A disk-unit consists of at least one descriptor   file, and zero or more extent files.   <p>   Sometimes, a disk-unit is also referred to as a <I>backing</I>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| fileKey | int | None | None | Array of keys of the files that make up the disk unit. Values here   correspond to property <a href="vim.vm.FileLayoutEx.FileInfo.md#key">key</a> in   <a href="vim.vm.FileLayoutEx.md#file">file</a>.   <p>   At least one entry always exists in this array. Property   <a href="vim.vm.FileLayoutEx.FileInfo.md#type">type</a> of the referenced file   can be used to distinguish the disk descriptor (type <a href="vim.vm.FileLayoutEx.FileType.md#diskDescriptor">diskDescriptor</a>) from the extents. |


