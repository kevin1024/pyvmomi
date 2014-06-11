vim.vm.device.VirtualDisk
=========================
inherits from [vim.vm.device.VirtualDevice](docs/vim.vm.device.VirtualDevice.md)


This data object type contains information about a disk in a virtual machine.   <p>   The virtual disk backing object types describe the different virtual disk backings   available.   The disk format version in each case describes   the version of the format that is used.   <p>   Supported virtual disk backings:   <table>   <dt>Sparse disk format, version 1 and 2</dt>   <dd>The virtual disk backing grows when needed.       Supported only for VMware Server.</dd>   <dt>Flat disk format, version 1 and 2</dt>   <dd>The virtual disk backing is preallocated.       Version 1 is supported only for VMware Server.</dd>   <dt>Space efficient sparse disk format</dt>   <dd>The virtual disk backing grows on demand and       incorporates additional space optimizations.</dd>   <dt>Raw disk format, version 2</dt>   <dd>The virtual disk backing uses a full physical disk drive       to back the virtual disk. Supported only for VMware Server.</dd>   <dt>Partitioned raw disk format, version 2</dt>   <dd>The virtual disk backing uses one or more partitions on a       physical disk drive to back a virtual disk. Supported only for VMware Server.</dd>   <dt>Raw disk mapping, version 1</dt>   <dd>The virtual disk backing uses a raw device mapping to back the virtual disk.       Supported for ESX Server 2.5 and 3.x.</dd>   </table>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| capacityInKB | long | None | None | Capacity of this virtual disk in kilobytes.  Information might be lost when actual disk size is rounded off to kilobytes.  <p /> |
| capacityInBytes | long | true | None | Capacity of this virtual disk in bytes.   Server will always populate this property. Clients must initialize it when   creating a new non -RDM disk or in case they want to change the current   capacity of an existing virtual disk, but can omit it otherwise. |
| shares | [vim.SharesInfo](vim.SharesInfo.md "vim.SharesInfo") | true | None | Disk shares, used for resource scheduling. |
| storageIOAllocation | [vim.StorageResourceManager.IOAllocationInfo](vim.StorageResourceManager.IOAllocationInfo.md "vim.StorageResourceManager.IOAllocationInfo") | true | None | Resource allocation for storage I/O. |
| diskObjectId | string | true | None | Virtual disk durable and unmutable identifier.   Virtual disk has a UUID field but that can be set through  VirtualDiskManager APIs.   This identifier is a universally unique identifier which is not settable.  VirtualDisk can remain in existence even if it is not associated with VM. |
| vFlashCacheConfigInfo | [vim.vm.device.VirtualDisk.VFlashCacheConfigInfo](vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.md "vim.vm.device.VirtualDisk.VFlashCacheConfigInfo") | true | None | vFlash cache configuration supported on this virtual disk |


