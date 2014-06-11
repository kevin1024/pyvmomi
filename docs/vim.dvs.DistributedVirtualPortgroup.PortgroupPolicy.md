vim.dvs.DistributedVirtualPortgroup.PortgroupPolicy
===================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The DistributedVirtualPortgroup policies. This field is not applicable   when queried directly against an ESX host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| blockOverrideAllowed | bool | None | None | Allow the <a href="vim.dvs.DistributedVirtualPort.Setting.md#blocked">blocked</a> setting   of an individual port to override the setting in   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#defaultPortConfig">defaultPortConfig</a> of   a portgroup. |
| shapingOverrideAllowed | bool | None | None | Allow the <a href="vim.dvs.DistributedVirtualPort.Setting.md#inShapingPolicy">inShapingPolicy</a> or   <a href="vim.dvs.DistributedVirtualPort.Setting.md#outShapingPolicy">outShapingPolicy</a> settings   of an individual port to override the setting in   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#defaultPortConfig">defaultPortConfig</a> of   a portgroup. |
| vendorConfigOverrideAllowed | bool | None | None | Allow the <a href="vim.dvs.DistributedVirtualPort.Setting.md#vendorSpecificConfig">vendorSpecificConfig</a>   setting of an individual port to override the setting in   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#defaultPortConfig">defaultPortConfig</a> of   a portgroup. |
| livePortMovingAllowed | bool | None | None | Allow a live port to be moved in and out of the portgroup. |
| portConfigResetAtDisconnect | bool | None | None | If true, reset the port network setting back to the portgroup setting   (thus removing the per-port setting) when the port is disconnected from   the connectee. |
| networkResourcePoolOverrideAllowed | bool | true | None | Allow the setting of   <a href="vim.dvs.DistributedVirtualPort.Setting.md#networkResourcePoolKey">networkResourcePoolKey</a> of an   individual port to override the setting in   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#defaultPortConfig">defaultPortConfig</a>   of a portgroup. |
| trafficFilterOverrideAllowed | bool | true | None | Allow the setting of   <a href="vim.dvs.DistributedVirtualPort.Setting.md#filterPolicy">filterPolicy</a>,   for an individual port to override the setting in   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#defaultPortConfig">defaultPortConfig</a> of   a portgroup. |


