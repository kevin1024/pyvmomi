vim.host.PlugStoreTopology.Target
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object represents target information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The identifier of the target.  This will be a string representing the   transport information of the target. |
| transport | [vim.host.TargetTransport](vim.host.TargetTransport.md "vim.host.TargetTransport") | true | None | Detailed, transport-specific information about the target of a path. |


