vim.dvs.HostProductSpec
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type is a subset of <a href="vim.AboutInfo.md">AboutInfo</a>. An object of   this type can be used to describe the specification for a host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| productLineId | string | true | None | The product-line name. |
| version | string | true | None | Dot-separated version string. For example, "1.2". |


