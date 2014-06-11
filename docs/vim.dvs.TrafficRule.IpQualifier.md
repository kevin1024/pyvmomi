vim.dvs.TrafficRule.IpQualifier
===============================
inherits from [vim.dvs.TrafficRule.Qualifier](docs/vim.dvs.TrafficRule.Qualifier.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines the IP Rule Qualifier. Here IP addresses of source    and destination will be used for classifying packets.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sourceAddress | [vim.IpAddress](vim.IpAddress.md "vim.IpAddress") | true | None | IP qualifier for source.    If this property is NULL, it will match "any IPv4 or any IPv6 address". |
| destinationAddress | [vim.IpAddress](vim.IpAddress.md "vim.IpAddress") | true | None | IP qualifier for destination.    If this property is NULL, it will match "any IPv4 or any IPv6 address". |
| protocol | [vim.IntExpression](vim.IntExpression.md "vim.IntExpression") | true | None | Protocols like TCP, UDP, ICMP etc. The valid value for a protocol    is got from IANA assigned value for the protocol. This can be got    from RFC 5237 and IANA website section related to protocol numbers. |
| sourceIpPort | [vim.dvs.TrafficRule.IpPort](vim.dvs.TrafficRule.IpPort.md "vim.dvs.TrafficRule.IpPort") | true | None | Source IP Port. |
| destinationIpPort | [vim.dvs.TrafficRule.IpPort](vim.dvs.TrafficRule.IpPort.md "vim.dvs.TrafficRule.IpPort") | true | None | Destination IP Port. |
| tcpFlags | [vim.IntExpression](vim.IntExpression.md "vim.IntExpression") | true | None | TCP flags. The valid values can be found at RFC 3168. |


