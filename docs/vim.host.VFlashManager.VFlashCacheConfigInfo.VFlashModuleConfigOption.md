vim.host.VFlashManager.VFlashCacheConfigInfo.VFlashModuleConfigOption
=====================================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vFlashModule | string | None | None | Name of the vFlash module |
| vFlashModuleVersion | string | None | None | Version of the vFlash module |
| minSupportedModuleVersion | string | None | None | Minimum supported version |
| cacheConsistencyType | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | Cache data consistency types.   See <a href="vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.CacheConsistencyType.md">VirtualDiskVFlashCacheConfigInfoCacheConsistencyType</a> |
| cacheMode | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | Cache modes.   See <a href="vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.CacheMode.md">VirtualDiskVFlashCacheConfigInfoCacheMode</a> |
| blockSizeInKBOption | [vim.option.LongOption](vim.option.LongOption.md "vim.option.LongOption") | None | None | blockSizeInKBOption defines a range of virtual disk cache block size. |
| reservationInMBOption | [vim.option.LongOption](vim.option.LongOption.md "vim.option.LongOption") | None | None | reservationInMBOption defines a range of virtual disk cache size. |
| maxDiskSizeInKB | long | None | None | Maximal size of virtual disk supported in kilobytes. |


