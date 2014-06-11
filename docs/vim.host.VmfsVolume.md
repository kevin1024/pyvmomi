vim.host.VmfsVolume
===================
inherits from [vim.host.FileSystemVolume](docs/vim.host.FileSystemVolume.md)


The VMFS file system.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| blockSizeMb | int | None | None | Block size of VMFS.  Determines maximum file size.  The maximum number   of blocks is typically fixed with each specific version of VMFS.  To   increase the maximum size of a VMFS file, increase the block size.   <p>   The minimum block size is 1MB. |
| maxBlocks | int | None | None | Maximum number of blocks.  Determines maximum file size along   with blockSize. See information about the blockSize.   <p> |
| majorVersion | int | None | None | Major version number of VMFS. |
| version | string | None | None | Version string.  Contains major and minor version numbers. |
| uuid | string | None | None | The universally unique identifier assigned to VMFS. |
| extent | [vim.host.ScsiDisk.Partition](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition") | None | None | The list of partition names that comprise this disk's   VMFS extents.   <p>   This property can be accessed via various enclosing objects.   In VirtualCenter, where it can be accessed from multiple   hosts, the value of this property may differ according to the context   in which it is accessed. When accessed from the   <a href="vim.host.VmfsDatastoreInfo.md">VmfsDatastoreInfo</a> object, in VirtualCenter, this   property reflects the extent information of any one of the hosts visible   to the datastore.   <p>   For a VirtualCenter system which manages ESX Server 2.x and   ESX Server 3.x hosts, this extent information is only correlatable   across hosts if the extents are exposed on the same adapter on all hosts   which can access them. To find the extent names for a specific host,   this same property should be accessed via the host's   <a href="vim.host.FileSystemVolume.md">HostFileSystemVolume</a> object, by correlating the uuid of   the VMFS datastore in the VmfsDatastoreInfo object to the uuid in the   FileSystemVolume object.   <p>   For a Virtual Center system which manages only ESX Server hosts with   versions 4.0 onwards , this extent information is correlatable across   hosts, irrespective of the adapters the extents are exposed on. |
| vmfsUpgradable | bool | None | None | Can the filesystem be upgraded to a newer version.<br>See <a href="vim.host.StorageSystem.md#upgradeVmfs">UpgradeVmfs</a><br> |
| forceMountedInfo | [vim.host.ForceMountedInfo](vim.host.ForceMountedInfo.md "vim.host.ForceMountedInfo") | true | None | Information about 'forceMounted' VmfsVolume.   When the system detects a copy of a VmfsVolume, it will not be   auto-mounted on the host and it will be detected as   'UnresolvedVmfsVolume'. If user decides to 'forceMount' the   VmfsVolume on the host, forceMountedInfo will be populated.   It will not be set for automounted VMFS volumes. |
| ssd | bool | true | None | Indicates whether the volume is SSD backed.  If unset, the information whether the volume is SSD backed is unknown. |
| local | bool | true | None | Indicates whether the volume is backed by local disk.  If unset, the information of the volume is local-disk backed is unknown. |


