vim.host.VirtualSwitch.Config
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the VirtualSwitch configuration   containing both the configurable   properties on a VirtualSwitch and identification information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| changeOperation | string | true | None | This property indicates the change operation to apply on   this configuration specification.<br>See <a href="vim.host.ConfigChange.Operation.md">HostConfigChangeOperation</a><br> |
| name | string | None | None | The name of the virtual switch.   Maximum length is 32 characters. |
| spec | [vim.host.VirtualSwitch.Specification](vim.host.VirtualSwitch.Specification.md "vim.host.VirtualSwitch.Specification") | true | None | The specification of the VirtualSwitch. |


