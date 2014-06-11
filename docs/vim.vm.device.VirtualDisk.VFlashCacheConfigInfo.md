vim.vm.device.VirtualDisk.VFlashCacheConfigInfo
===============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Data object describes the vFlash cache configuration on this virtual disk.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vFlashModule | string | true | None | Name of vFlash module which manages the cache. If not specified, default setting  <a href="vim.host.VFlashManager.VFlashCacheConfigSpec.md#defaultVFlashModule">defaultVFlashModule</a>  will be used. |
| reservationInMB | long | true | None | Amount of vFlash resource that is guaranteed available to the cache. If not specified,  default reservation will be used. |
| cacheConsistencyType | string | true | None | Cache data consistency types after a crash.  See <a href="vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.CacheConsistencyType.md">VirtualDiskVFlashCacheConfigInfoCacheConsistencyType</a>  for supported types. If not specified, the default value used is  <a href="vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.CacheConsistencyType.md#strong">strong</a> |
| cacheMode | string | true | None | Cache modes.  See <a href="vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.CacheMode.md">VirtualDiskVFlashCacheConfigInfoCacheMode</a>  for supported modes. If not specified, the default value used is  <a href="vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.CacheMode.md#write_thru">write_thru</a>. |
| blockSizeInKB | long | true | None | Cache block size. This parameter allows the user to control how much  data gets cached on a single access to the VMDK. Max block size is 1MB.  Default is 4KB. |


