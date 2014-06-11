vim.dvs.VmwareDistributedVirtualSwitch.ConfigSpec
=================================================
inherits from [vim.DistributedVirtualSwitch.ConfigSpec](docs/vim.DistributedVirtualSwitch.ConfigSpec.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This class defines the VMware specific configuration for   DistributedVirtualSwitch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| pvlanConfigSpec | [vim.dvs.VmwareDistributedVirtualSwitch.PvlanConfigSpec](vim.dvs.VmwareDistributedVirtualSwitch.PvlanConfigSpec.md "vim.dvs.VmwareDistributedVirtualSwitch.PvlanConfigSpec") | true | None | The PVLAN configuration specification.   <p>   A <a href="vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry.md">VMwareDVSPvlanMapEntry</a>   that has the same value for   <a href="vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry.md#primaryVlanId">primaryVlanId</a> and   <a href="vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry.md#secondaryVlanId">secondaryVlanId</a>   is referred to as a primary PVLAN entry.   Otherwise, the <a href="vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry.md">VMwareDVSPvlanMapEntry</a>   is referred to as a secondary PVLAN entry.   <p>   The <a href="vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry.md#pvlanType">pvlanType</a>   of a primary PVLAN entry must be   <a href="vim.dvs.VmwareDistributedVirtualSwitch.PvlanPortType.md#promiscuous">promiscuous</a>.   A secondary PVLAN entry can have a   <a href="vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry.md#pvlanType">pvlanType</a>   of either   <a href="vim.dvs.VmwareDistributedVirtualSwitch.PvlanPortType.md#community">community</a> or   <a href="vim.dvs.VmwareDistributedVirtualSwitch.PvlanPortType.md#isolated">isolated</a>.   <p>   Primary PVLAN entries must be explicitly added.   If there is no primary PVLAN entry corresponding to the   <a href="vim.dvs.VmwareDistributedVirtualSwitch.PvlanMapEntry.md#primaryVlanId">primaryVlanId</a>   of a secondary PVLAN entry, a fault is thrown.   <p>   While deleting a primary PVLAN entry, any associated secondary PVLAN   entries must be explicitly deleted. |
| vspanConfigSpec | [vim.dvs.VmwareDistributedVirtualSwitch.VspanConfigSpec](vim.dvs.VmwareDistributedVirtualSwitch.VspanConfigSpec.md "vim.dvs.VmwareDistributedVirtualSwitch.VspanConfigSpec") | true | None | The Distributed Port Mirroring configuration specification. The VSPAN   sessions in the array cannot be of the same key. |
| maxMtu | int | true | None | The maximum MTU in the switch. |
| linkDiscoveryProtocolConfig | [vim.host.LinkDiscoveryProtocolConfig](vim.host.LinkDiscoveryProtocolConfig.md "vim.host.LinkDiscoveryProtocolConfig") | true | None | See <a href="vim.host.LinkDiscoveryProtocolConfig.md">LinkDiscoveryProtocolConfig</a>. |
| ipfixConfig | [vim.dvs.VmwareDistributedVirtualSwitch.IpfixConfig](vim.dvs.VmwareDistributedVirtualSwitch.IpfixConfig.md "vim.dvs.VmwareDistributedVirtualSwitch.IpfixConfig") | true | None | Configuration for ipfix monitoring of the switch traffic. This must be   set before ipfix monitoring can be enabled for the switch, or for any   portgroup or port of the switch.<br>See <a href="vim.dvs.VmwareDistributedVirtualSwitch.VmwarePortConfigPolicy.md#ipfixEnabled">ipfixEnabled</a><br> |
| lacpApiVersion | string | true | None | The Link Aggregation Control Protocol group version in the switch.   See LacpApiVersion for valid values. |


