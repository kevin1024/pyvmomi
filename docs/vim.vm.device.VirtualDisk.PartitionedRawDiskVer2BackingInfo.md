vim.vm.device.VirtualDisk.PartitionedRawDiskVer2BackingInfo
===========================================================
inherits from [vim.vm.device.VirtualDisk.RawDiskVer2BackingInfo](docs/vim.vm.device.VirtualDisk.RawDiskVer2BackingInfo.md)


This data object type contains information about backing a virtual disk   using one or more partitions on a physical disk device. This type of   backing is supported for VMware Server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| partition | int | None | None | Array of partition indexes. This array identifies the   partitions that are used on the physical disk drive. |


