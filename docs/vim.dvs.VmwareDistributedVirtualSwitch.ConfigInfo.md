vim.dvs.VmwareDistributedVirtualSwitch.ConfigInfo
=================================================
inherits from [vim.DistributedVirtualSwitch.ConfigInfo](docs/vim.DistributedVirtualSwitch.ConfigInfo.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This class defines the VMware specific configuration for   DistributedVirtualSwitch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vspanSession | [vim.dvs.VmwareDistributedVirtualSwitch.VspanSession](vim.dvs.VmwareDistributedVirtualSwitch.VspanSession.md "vim.dvs.VmwareDistributedVirtualSwitch.VspanSession") | true | None | The Distributed Port Mirroring sessions in the switch. |
| pvlanConfig | [vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry](vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry.md "vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry") | true | None | The PVLAN configured in the switch. |
| maxMtu | int | None | None | The maximum MTU in the switch. |
| linkDiscoveryProtocolConfig | [vim.host.LinkDiscoveryProtocolConfig](vim.host.LinkDiscoveryProtocolConfig.md "vim.host.LinkDiscoveryProtocolConfig") | true | None | See <a href="vim.host.LinkDiscoveryProtocolConfig.md">LinkDiscoveryProtocolConfig</a>. |
| ipfixConfig | [vim.dvs.VmwareDistributedVirtualSwitch.IpfixConfig](vim.dvs.VmwareDistributedVirtualSwitch.IpfixConfig.md "vim.dvs.VmwareDistributedVirtualSwitch.IpfixConfig") | true | None | Configuration for ipfix monitoring of the switch traffic. This must be   set before ipfix monitoring can be enabled for the switch, or for any   portgroup or port of the switch.<br>See <a href="vim.dvs.VmwareDistributedVirtualSwitch.VmwarePortConfigPolicy.md#ipfixEnabled">ipfixEnabled</a><br> |
| lacpGroupConfig | [vim.dvs.VmwareDistributedVirtualSwitch.LacpGroupConfig](vim.dvs.VmwareDistributedVirtualSwitch.LacpGroupConfig.md "vim.dvs.VmwareDistributedVirtualSwitch.LacpGroupConfig") | true | None | The Link Aggregation Control Protocol groups in the switch. |
| lacpApiVersion | string | true | None | The Link Aggregation Control Protocol group version in the switch.   See LacpApiVersion for valid values. |


