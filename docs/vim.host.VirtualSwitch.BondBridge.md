vim.host.VirtualSwitch.BondBridge
=================================
inherits from [vim.host.VirtualSwitch.Bridge](docs/vim.host.VirtualSwitch.Bridge.md)


This data object type describes a bridge that provides   network adapter teaming capabilities.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| nicDevice | string | None | None | The list of keys of the physical network adapters to be bridged. |
| beacon | [vim.host.VirtualSwitch.BeaconConfig](vim.host.VirtualSwitch.BeaconConfig.md "vim.host.VirtualSwitch.BeaconConfig") | true | None | The beacon configuration to probe for the validity of a link.   If this is set, beacon probing is configured and will be used.   If this is not set, beacon probing is disabled. |
| linkDiscoveryProtocolConfig | [vim.host.LinkDiscoveryProtocolConfig](vim.host.LinkDiscoveryProtocolConfig.md "vim.host.LinkDiscoveryProtocolConfig") | true | None | The link discovery protocol configuration for the virtual switch.<br>See <a href="vim.host.LinkDiscoveryProtocolConfig.md">LinkDiscoveryProtocolConfig</a><br> |


