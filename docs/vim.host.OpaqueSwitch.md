vim.host.OpaqueSwitch
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The OpaqueSwitch contains basic information about virtual switches that are   managed by a management plane outside of vSphere.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The opaque switch key. |
| name | string | true | None | The opaque switch name. |
| pnic | [vim.host.PhysicalNic](vim.host.PhysicalNic.md "vim.host.PhysicalNic") | true | None | The set of physical network adapters associated with this switch. |


