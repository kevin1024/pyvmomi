vim.vm.device.VirtualDiskOption.VFlashCacheConfigOption
=======================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Options for vFlash cache configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| cacheConsistencyType | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | Cache data consistency type.  See <a href="vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.CacheConsistencyType.md">VirtualDiskVFlashCacheConfigInfoCacheConsistencyType</a> |
| cacheMode | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | Cache mode  See <a href="vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.CacheMode.md">VirtualDiskVFlashCacheConfigInfoCacheMode</a> |
| reservationInMB | [vim.option.LongOption](vim.option.LongOption.md "vim.option.LongOption") | None | None | Cache reservation |
| blockSizeInKB | [vim.option.LongOption](vim.option.LongOption.md "vim.option.LongOption") | None | None | Cache block size |


