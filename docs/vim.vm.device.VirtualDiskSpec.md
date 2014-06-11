vim.vm.device.VirtualDiskSpec
=============================
inherits from [vim.vm.device.VirtualDeviceSpec](docs/vim.vm.device.VirtualDeviceSpec.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The VirtualDiskSpec data object type encapsulates change   specifications for an individual virtual disk device. The virtual   disk being added or modified must be fully specified.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| migrateCache | bool | true | None | Manner in which to transfer the cache associated with the virtual disk to the   target host.   If left unset then migrate is used when the backing vFlash module version is   compatible with the specific vFalsh module on the target host; otherwise flush is   used for write back cache, or a no-op for write through cache. This setting can   avoid VM migration failure due to incompatibility.   If true then migrate is always used. VM migration may fail if the backing vFlash module   version is incompatible with the module on the target host.   If false then flush is used for write back cache. It is a no-op for write through   cache. This setting can avoid VM migration failure due to incompatibility, but cache   files have to be rebuilt on the target host.   Default is unset.   <p><br>See <a href="vim.host.VFlashManager.VFlashCacheConfigInfo.VFlashModuleConfigOption.md">HostVFlashManagerVFlashCacheConfigInfoVFlashModuleConfigOption</a><br> |


