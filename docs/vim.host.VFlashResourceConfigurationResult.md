vim.host.VFlashResourceConfigurationResult
==========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


vFlash resource configuration result returns the newly-configured backend    VFFS volume and operation result for each passed-in SSD device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| devicePath | string | true | None | The original array of device path which user had specified |
| vffs | [vim.host.VffsVolume](vim.host.VffsVolume.md "vim.host.VffsVolume") | true | None | Newly configured VffsVolume |
| diskConfigurationResult | [vim.host.DiskConfigurationResult](vim.host.DiskConfigurationResult.md "vim.host.DiskConfigurationResult") | true | None | Array of device operation results. |


