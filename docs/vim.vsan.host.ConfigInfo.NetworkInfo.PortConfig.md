vim.vsan.host.ConfigInfo.NetworkInfo.PortConfig
===============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


A PortConfig represents a virtual network adapter and its  configuration for use by the VSAN service.<br>See <a href="vim.host.VirtualNic.md">HostVirtualNic</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipConfig | [vim.vsan.host.IpConfig](vim.vsan.host.IpConfig.md "vim.vsan.host.IpConfig") | true | None | <a href="vim.vsan.host.IpConfig.md">VsanHostIpConfig</a> for this PortConfig. |
| device | string | None | None | Device name which identifies the network adapter for this  PortConfig.<br>See <a href="vim.host.VirtualNic.md#device">device</a><br> |


