vim.cluster.DpmHostConfigInfo
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


DPM configuration for a single host. This makes   it possible to override the default behavior for an individual   host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | Reference to the host. |
| enabled | bool | true | None | Flag to indicate whether or not VirtualCenter is allowed to perform any   power related operations or recommendations for this host.    If this flag is false, the host is effectively excluded from   DPM service.   <p>   If no individual DPM specification exists for a host,   this property defaults to true. |
| behavior | [vim.cluster.DpmConfigInfo.DpmBehavior](vim.cluster.DpmConfigInfo.DpmBehavior.md "vim.cluster.DpmConfigInfo.DpmBehavior") | true | None | Specifies the particular DPM behavior for this host.<br>See <a href="vim.cluster.DpmConfigInfo.md">ClusterDpmConfigInfo</a><br> |


