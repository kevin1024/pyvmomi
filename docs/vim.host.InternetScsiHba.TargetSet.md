vim.host.InternetScsiHba.TargetSet
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A collection of one or more static targets or discovery addresses.   At least one of the arrays must be non-empty.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| staticTargets | [vim.host.InternetScsiHba.StaticTarget](vim.host.InternetScsiHba.StaticTarget.md "vim.host.InternetScsiHba.StaticTarget") | true | None |  |
| sendTargets | [vim.host.InternetScsiHba.SendTarget](vim.host.InternetScsiHba.SendTarget.md "vim.host.InternetScsiHba.SendTarget") | true | None |  |


