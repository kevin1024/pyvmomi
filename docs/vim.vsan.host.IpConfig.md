vim.vsan.host.IpConfig
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


An <a href="vim.vsan.host.IpConfig.md">VsanHostIpConfig</a> is a pair of multicast IP addresses for use by the VSAN  service.  For VSAN there is one such IpConfig pair per "virtual network" as  represented by <a href="vim.vsan.host.ConfigInfo.NetworkInfo.PortConfig.md">VsanHostConfigInfoNetworkInfoPortConfig</a>.<br>See <a href="vim.vsan.host.ConfigInfo.NetworkInfo.md">VsanHostConfigInfoNetworkInfo</a><br>See <a href="vim.vsan.host.ConfigInfo.NetworkInfo.md#port">port</a><br>See <a href="vim.vsan.host.ConfigInfo.NetworkInfo.PortConfig.md">VsanHostConfigInfoNetworkInfoPortConfig</a><br>See <a href="vim.host.VsanSystem.md#update">UpdateVsan_Task</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| upstreamIpAddress | string | None | None | Agent-to-master multicast IP address. |
| downstreamIpAddress | string | None | None | Master-to-agent multicast IP address. |


