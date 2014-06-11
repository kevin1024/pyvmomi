vim.host.UnresolvedVmfsExtent
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Information about an unresolved VMFS volume extent   An unresolved VMFS volume extent is a device partition which is   detected to have copy of an extent of a VMFS volume.   Such a copy can be created via replication or snapshots, for example.<br>See <a href="vim.host.UnresolvedVmfsVolume.md">HostUnresolvedVmfsVolume</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| device | [vim.host.ScsiDisk.Partition](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition") | None | None | The device information |
| devicePath | string | None | None | The device path of an VMFS extent |
| vmfsUuid | string | None | None | The UUID of the VMFS volume read from to the partition. |
| isHeadExtent | bool | None | None | Is this a copy of the head extent of the VMFS volume? |
| ordinal | int | None | None | A number indicating the order of an extent in a volume.  An extent with   a lower ordinal value than another extent provides a range of blocks to   a volume at an earlier block address range.  Extents with the same   ordinal provide the same range of blocks to a volume.  A zero ordinal   indicates that the extent is a head extent.   <p>   In the case each extent in the <a href="vim.host.UnresolvedVmfsVolume.md">HostUnresolvedVmfsVolume</a> is   represented in the list of <a href="vim.host.UnresolvedVmfsExtent.md">HostUnresolvedVmfsExtent</a> data objects,   the ordinal will refer to the absolute index of the extent in the   volume.  For example, ordinal "1" refers to the second extent;   ordinal "2" refers to the third extent.   <p>   In the case that some extents of the volume are not represented in   the <a href="vim.host.UnresolvedVmfsExtent.md">HostUnresolvedVmfsExtent</a> list, the ordinal will not precisely   describe the position in the list of extents.  A number will be skipped   to indicate holes in the extent order.  For example, given a volume with   five extents with the second and third extents missing, the ordinal   values in use will be {0, 2, 3}.  The missing second and third extent   are represented by the missing ordinal value "1" while the fourth and   fifth extents will be assigned an ordinal of "2" and "3" respectively.   <p>   The reason the ordinals are not reliable in the case of missing extents   is because the extents are identified by their start and end blocks.   The ordinals are just a hint used to help indicate extents that   correspond to the same start and end blocks. |
| startBlock | int | None | None | Index of the first block that this extent provides. |
| endBlock | int | None | None | Index of the last block that this extent provides. |
| reason | string | None | None | Reason as to why the partition is marked as copy  of a VMFS volume's extent.  Possible reasons are the disk id is not matching with what  the scsi inq is saying or disk uuid is not matching<br>See <a href="vim.host.UnresolvedVmfsExtent.UnresolvedReason.md">HostUnresolvedVmfsExtentUnresolvedReason</a><br> |


