vim.DistributedVirtualSwitch.CreateSpec
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Specification to create a <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| configSpec | [vim.DistributedVirtualSwitch.ConfigSpec](vim.DistributedVirtualSwitch.ConfigSpec.md "vim.DistributedVirtualSwitch.ConfigSpec") | None | None | Configuration data. |
| productInfo | [vim.dvs.ProductSpec](vim.dvs.ProductSpec.md "vim.dvs.ProductSpec") | true | None | Product information for this switch implementation. If you  do not specify this property, the Server will use the latest  version to create the <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>. |
| capability | [vim.DistributedVirtualSwitch.Capability](vim.DistributedVirtualSwitch.Capability.md "vim.DistributedVirtualSwitch.Capability") | true | None | Capability of the switch. |


