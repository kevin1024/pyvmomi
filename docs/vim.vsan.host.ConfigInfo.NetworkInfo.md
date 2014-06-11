vim.vsan.host.ConfigInfo.NetworkInfo
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Host-local VSAN network configuration.  This data object is used  both for specifying and retrieving network configuration for a  host participating in the VSAN service.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| port | [vim.vsan.host.ConfigInfo.NetworkInfo.PortConfig](vim.vsan.host.ConfigInfo.NetworkInfo.PortConfig.md "vim.vsan.host.ConfigInfo.NetworkInfo.PortConfig") | true | None | Set of PortConfig entries for use by the VSAN service, one per  "virtual network" as used by VSAN. |


