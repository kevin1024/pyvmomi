vim.vm.device.VirtualDiskOption
===============================
inherits from [vim.vm.device.VirtualDeviceOption](docs/vim.vm.device.VirtualDeviceOption.md)


The VirtualDiskOption data class contains the options for the   virtual disk data object type.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| capacityInKB | [vim.option.LongOption](vim.option.LongOption.md "vim.option.LongOption") | None | None | Minimum, maximum, and default capacity of the disk. |
| ioAllocationOption | [vim.StorageResourceManager.IOAllocationOption](vim.StorageResourceManager.IOAllocationOption.md "vim.StorageResourceManager.IOAllocationOption") | None | None | Minumum, maximum, and default values for Storage I/O allocation.<br>See <a href="vim.StorageResourceManager.IOAllocationInfo.md">StorageIOAllocationInfo</a><br> |
| vFlashCacheConfigOption | [vim.vm.device.VirtualDiskOption.VFlashCacheConfigOption](vim.vm.device.VirtualDiskOption.VFlashCacheConfigOption.md "vim.vm.device.VirtualDiskOption.VFlashCacheConfigOption") | true | None | vFlash cache configuration on the disk |


