vim.host.IpConfig.IpV6Address
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The ipv6 address specification

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipAddress | string | None | None | The ipv6 address. When DHCP is enabled, this property   reflects the current IP configuration and cannot be set. |
| prefixLength | int | None | None | The prefix length. An ipv6 prefixLength is a decimal value that indicates  the number of contiguous, higher-order bits of the address that make up the  network portion of the address.  For example, 10FA:6604:8136:6502::/64 is a possible IPv6 prefix. The prefix  length in this case is 64. |
| origin | string | true | None | The type of the ipv6 address configuration on the interface.  This can be one of the types defined my the enum  <a href="vim.host.IpConfig.IpV6AddressConfigType.md">HostIpConfigIpV6AddressConfigType</a>. |
| dadState | string | true | None | The state of this ipAddress. Can be one of  <a href="vim.host.IpConfig.IpV6AddressStatus.md">HostIpConfigIpV6AddressStatus</a> |
| lifetime | datetime | true | None | The time when will this address expire. If not set  the address lifetime is unlimited. |
| operation | string | true | None | Valid values are "add" and "remove".  See <a href="vim.host.ConfigChange.Operation.md">HostConfigChangeOperation</a>. |


