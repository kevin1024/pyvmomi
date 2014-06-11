vim.host.VFlashManager.VFlashCacheConfigSpec
============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Specification to configure vFlash cache on the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| defaultVFlashModule | string | None | None | Name of the default vFlash module for the read-write caches associated   with the VMs of this host. This setting can be overridden by   <a href="vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.md#vFlashModule">vFlashModule</a>   per VMDK. |
| swapCacheReservationInGB | long | None | None | Amount of vFlash resource is allocated to the host swap cache. As long as set,   reservation will be permanent and retain regardless of host power state. The host   swap cache will be disabled if the reservation is set to zero. |


