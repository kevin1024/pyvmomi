vim.host.PortGroup.Config
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This describes the port group configuration containing both    the configurable properties on a port group and the associated    virtual switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| changeOperation | string | true | None | Indicates the change operation to apply on this configuration   specification.<br>See <a href="vim.host.ConfigChange.Operation.md">HostConfigChangeOperation</a><br> |
| spec | [vim.host.PortGroup.Specification](vim.host.PortGroup.Specification.md "vim.host.PortGroup.Specification") | true | None | The specification of the port group. |


