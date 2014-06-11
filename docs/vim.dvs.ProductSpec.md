vim.dvs.ProductSpec
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type is a subset of <a href="vim.AboutInfo.md">AboutInfo</a>. An object of   this type can be used to describe the specification for a proxy switch module   of a <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | true | None | Short form of the product name. |
| vendor | string | true | None | Name of the vendor of this product. |
| version | string | true | None | Dot-separated version string. For example, "1.2". |
| build | string | true | None | Build string for the server on which this call is made. For example, x.y.z-num.   This string does not apply to the API. |
| forwardingClass | string | true | None | Forwarding class of the distributed virtual switch. |
| bundleId | string | true | None | The ID of the bundle if a host component bundle needs to be installed on   the host members to support the functionality of the switch. |
| bundleUrl | string | true | None | The URL of the bundle that VMware Update Manager will use to install   the bundle on the host members, if <a href="vim.dvs.ProductSpec.md#bundleId">bundleId</a> is set. |


