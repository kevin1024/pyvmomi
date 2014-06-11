vim.host.InternetScsiHba.IPCapabilities
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The IP Capabilities for the host bus adapter

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| addressSettable | bool | None | None | True if the host bus adapter supports setting its IP address. |
| ipConfigurationMethodSettable | bool | None | None | True if the host bus adapter supports DHCP. |
| subnetMaskSettable | bool | None | None | True if the host bus adapter supports setting its subnet mask. |
| defaultGatewaySettable | bool | None | None | True if the host bus adapter supports setting its gateway. |
| primaryDnsServerAddressSettable | bool | None | None | True if the host bus adapter supports setting its primary DNS. |
| alternateDnsServerAddressSettable | bool | None | None | True if the host bus adapter supports setting its secondary DNS. |
| ipv6Supported | bool | true | None | True if the host bus adapter supports the use of IPv6 addresses |
| arpRedirectSettable | bool | true | None | True if the host bus adapter supports setting its ARP Redirect value |
| mtuSettable | bool | true | None | True if the host bus adapter supports setting its MTU, (for Jumbo   Frames, etc) |
| hostNameAsTargetAddress | bool | true | None | True if the discovery and static targets can be configured with   a host name as opposed to an IP address. |
| nameAliasSettable | bool | true | None | True if the host bus adapter supports setting its name and alias |


