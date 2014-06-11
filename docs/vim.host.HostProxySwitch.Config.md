vim.host.HostProxySwitch.Config
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type describes the HostProxySwitch configuration    containing both the configurable   properties on a HostProxySwitch and identification information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| changeOperation | string | true | None | This property indicates the change operation to apply on    this configuration specification. Valid values are:   <ul>   <li> <a href="vim.host.ConfigChange.Operation.md#edit">edit</a> </li>   <li> <a href="vim.host.ConfigChange.Operation.md#remove">remove</a> </li>   </ul><br>See <a href="vim.host.ConfigChange.Operation.md">HostConfigChangeOperation</a><br> |
| uuid | string | None | None | The uuid of the DistributedVirtualSwitch that the HostProxySwitch    is a part of. |
| spec | [vim.host.HostProxySwitch.Specification](vim.host.HostProxySwitch.Specification.md "vim.host.HostProxySwitch.Specification") | true | None | The specification of the HostProxySwitch. |


