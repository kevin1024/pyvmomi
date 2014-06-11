vim.vm.GuestInfo.DiskInfo
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about each virtual disk configured in the guest operating system.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskPath | string | true | None | Name of the virtual disk in the guest operating system. For example: C:\ |
| capacity | long | true | None | Total capacity of the disk, in bytes.   This is part of the virtual machine configuration. |
| freeSpace | long | true | None | Free space on the disk, in bytes. This is retrieved by VMware Tools. |


