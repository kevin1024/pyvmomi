vim.host.SnmpSystem.AgentLimits
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| maxReadOnlyCommunities | int | None | None | number of allowed communities |
| maxTrapDestinations | int | None | None | number of allowed destinations for notifications |
| maxCommunityLength | int | None | None | Max length of community |
| maxBufferSize | int | None | None | SNMP input buffer size |
| capability | [vim.host.SnmpSystem.AgentLimits.Capability](vim.host.SnmpSystem.AgentLimits.Capability.md "vim.host.SnmpSystem.AgentLimits.Capability") | None | None | Supported Capability for this agent |


