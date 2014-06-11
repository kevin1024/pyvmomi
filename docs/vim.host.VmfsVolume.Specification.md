vim.host.VmfsVolume.Specification
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the VMware File System (VMFS)   creation specification. Once created, these properties for the most   part cannot be changed.  There are a few exceptions.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| extent | [vim.host.ScsiDisk.Partition](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition") | None | None | Head extent of VMFS.  The head extent identifies the VMFS.  However,   the head extent should not be used to identify the VMFS across host   reboots.  The actual identifier is specified in "vmhbaI:T:L" format   which is not guaranteed to be stable across reboots.  Define a volume   name that is unique to the host and use it to refer to the VMFS.   Alternatively, the immutable UUID of the VMFS can be used after it   is created. |
| blockSizeMb | int | true | None | The block size of VMFS in megabytes (MB).  Determines the maximum file   size.  If this optional property is not set, the maximum   file size defaults to the maximum file size for the platform.   <p>    In VMFS2, the valid block sizes 1MB, 2MB, 4MB, 8MB, 16MB, 32MB, 64MB,   128MB, and 256MB.   In VMFS3, the valid block sizes are 1MB, 2MB, 4MB, and 8MB.   In VMFS5, the only valid block size is 1MB. |
| majorVersion | int | None | None | Major version number of VMFS.  This can be changed if the VMFS is   upgraded, but this is an irreversible change. |
| volumeName | string | None | None | Volume name of VMFS. |


