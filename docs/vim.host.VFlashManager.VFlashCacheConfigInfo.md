vim.host.VFlashManager.VFlashCacheConfigInfo
============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Data object describes host vFlash cache configuration information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vFlashModuleConfigOption | [vim.host.VFlashManager.VFlashCacheConfigInfo.VFlashModuleConfigOption](vim.host.VFlashManager.VFlashCacheConfigInfo.VFlashModuleConfigOption.md "vim.host.VFlashManager.VFlashCacheConfigInfo.VFlashModuleConfigOption") | true | None | Cache configuration options for the supported vFlash modules. |
| defaultVFlashModule | string | true | None | Name of the default vFlash module for the read-write cache associated   with the VMs of this host. This setting can be overridden by   <a href="vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.md#vFlashModule">vFlashModule</a>   per VMDK. |
| swapCacheReservationInGB | long | true | None | Amount of vFlash resource is allocated to the host swap cache. As long as set,   reservation will be permanent and retain regardless of host power state. The host   swap cache will be disabled if reservation is set to zero. |


