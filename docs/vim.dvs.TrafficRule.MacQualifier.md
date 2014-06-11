vim.dvs.TrafficRule.MacQualifier
================================
inherits from [vim.dvs.TrafficRule.Qualifier](docs/vim.dvs.TrafficRule.Qualifier.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines the MAC Rule Qualifier. Here MAC addresses of source    and destination will be used for classifying packets.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sourceAddress | [vim.MacAddress](vim.MacAddress.md "vim.MacAddress") | true | None | MAC address for source.    If this property is NULL, it will match "any MAC address". |
| destinationAddress | [vim.MacAddress](vim.MacAddress.md "vim.MacAddress") | true | None | MAC address for destination.    If this property is NULL, it will match "any MAC address". |
| protocol | [vim.IntExpression](vim.IntExpression.md "vim.IntExpression") | true | None | Protocol used. This corresponds to the EtherType field in Ethernet    frame. The valid values can be found from IEEE list at:    http://standards.ieee.org/regauth/ as mentioned in RFC 5342. |
| vlanId | [vim.IntExpression](vim.IntExpression.md "vim.IntExpression") | true | None | vlan id. |


