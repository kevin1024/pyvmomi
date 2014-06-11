vim.host.Ruleset.Rule
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes a port (or range of ports),   identified by port number(s), direction and protocol.  It is   used as a convenient way for users to express what ports they   want to permit through the firewall.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| port | int | None | None | The port number. |
| endPort | int | true | None | For a port range, the ending port number. |
| direction | [vim.host.Ruleset.Rule.Direction](vim.host.Ruleset.Rule.Direction.md "vim.host.Ruleset.Rule.Direction") | None | None | The port direction. |
| portType | [vim.host.Ruleset.Rule.PortType](vim.host.Ruleset.Rule.PortType.md "vim.host.Ruleset.Rule.PortType") | true | None | The port type. |
| protocol | string | None | None | The port protocol.  Valid values are defined by the    <a href="vim.host.Ruleset.Rule.Protocol.md">HostFirewallRuleProtocol</a> enumeration. |


