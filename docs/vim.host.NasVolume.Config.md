vim.host.NasVolume.Config
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This describes the NAS Volume configuration containing   the configurable properties on a NAS Volume

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| changeOperation | string | true | None | Indicates the change operation to apply on this configuration   specification.<br>See <a href="vim.host.ConfigChange.Operation.md">HostConfigChangeOperation</a><br> |
| spec | [vim.host.NasVolume.Specification](vim.host.NasVolume.Specification.md "vim.host.NasVolume.Specification") | true | None | The specification volume. |


