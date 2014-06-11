vim.host.VFlashManager.VFlashResourceConfigInfo
===============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


vFlash resource configuraiton Information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vffs | [vim.host.VffsVolume](vim.host.VffsVolume.md "vim.host.VffsVolume") | true | None | The contained VFFS volume |
| capacity | long | None | None | Capacity of the vFlash resource. It is the capacity   of the contained VFFS volume. |


