vim.dvs.HostMember.RuntimeInfo
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


The <a href="vim.dvs.HostMember.RuntimeInfo.md">HostMemberRuntimeInfo</a> data object  contains healthcheck and status information about a host  member of a distributed virtual switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | The host. |
| status | string | true | None | Host proxy switch status. See   <a href="vim.dvs.HostMember.HostComponentState.md">HostComponentState</a> for valid values.   This property replaces the deprecated   <a href="vim.dvs.HostMember.md">DistributedVirtualSwitchHostMember</a>.<a href="vim.dvs.HostMember.md#status">status</a>. |
| statusDetail | string | true | None | Additional information regarding the current membership status of the host.  This property replaces the deprecated  <a href="vim.dvs.HostMember.md">DistributedVirtualSwitchHostMember</a>.<a href="vim.dvs.HostMember.md#statusDetail">statusDetail</a>. |
| healthCheckResult | [vim.dvs.HostMember.HealthCheckResult](vim.dvs.HostMember.HealthCheckResult.md "vim.dvs.HostMember.HealthCheckResult") | true | None | Health check result for the host that joined the distributed virtual switch. |


