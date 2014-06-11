vim.vsan.host.MembershipInfo
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The <a href="vim.vsan.host.MembershipInfo.md">VsanHostMembershipInfo</a> data object contains VSAN cluster  membership information for a single host, as observed from a  given host.  This data object is used to represent read-only  state whose values may change during operation.<br>See <a href="vim.host.RuntimeInfo.md#vsanRuntimeInfo">vsanRuntimeInfo</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| nodeUuid | string | None | None | VSAN node UUID for the host of this MembershipInfo.<br>See <a href="vim.vsan.host.ClusterStatus.md#nodeUuid">nodeUuid</a><br> |
| hostname | string | None | None | Hostname for the host of this MembershipInfo.   May be the empty string "" if the hostname is unavailable. |


