vim.vsan.host.ClusterStatus
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The <a href="vim.vsan.host.ClusterStatus.md">VsanHostClusterStatus</a> data object contains a host's cluster status  information for the VSAN service.  This data object is used to represent  read-only state whose values may change during operation.<br>See <a href="vim.host.VsanSystem.md#queryHostStatus">QueryHostStatus</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| uuid | string | true | None | VSAN service cluster UUID. |
| nodeUuid | string | true | None | VSAN node UUID for this host. |
| health | string | None | None | VSAN health state for this host.<br>See <a href="vim.vsan.host.HealthState.md">VsanHostHealthState</a><br> |
| nodeState | [vim.vsan.host.ClusterStatus.State](vim.vsan.host.ClusterStatus.State.md "vim.vsan.host.ClusterStatus.State") | None | None | VSAN node state for this host. |
| memberUuid | string | true | None | List of UUIDs for VSAN nodes known to this host. |


