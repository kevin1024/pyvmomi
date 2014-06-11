vim.VirtualMachine.DiskChangeInfo
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Data structure to describe areas in a disk associated with this VM that have  been modified since a well-defined point in the past. Returned by  <a href="vim.VirtualMachine.md#queryChangedDiskAreas">QueryChangedDiskAreas</a>. This data structure describes  a subset of the disk identified by startOffset and length. All areas that  have been modified within this interval are listed under changedArea.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| startOffset | long | None | None | Start offset (in bytes) of disk area described by this data structure. |
| length | long | None | None | Length (in bytes) of disk area described by this data structure. |
| changedArea | [vim.VirtualMachine.DiskChangeInfo.DiskChangeExtent](vim.VirtualMachine.DiskChangeInfo.DiskChangeExtent.md "vim.VirtualMachine.DiskChangeInfo.DiskChangeExtent") | true | None | Modified disk areas. Might be empty if no parts of the disk between  startOffset and startOffset + length were modified. |


