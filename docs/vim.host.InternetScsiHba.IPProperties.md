vim.host.InternetScsiHba.IPProperties
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The IP properties for the host bus adapter

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| mac | string | true | None | The MAC address. |
| address | string | true | None | The current IPv4 address. |
| dhcpConfigurationEnabled | bool | None | None | True if the host bus adapter fetches its IP using DHCP. |
| subnetMask | string | true | None | The current IPv4 subnet mask. |
| defaultGateway | string | true | None | The current IPv4 gateway. |
| primaryDnsServerAddress | string | true | None | The current primary DNS address. |
| alternateDnsServerAddress | string | true | None | The current secondary DNS address. |
| ipv6Address | string | true | None | The current IPv6 address. |
| ipv6SubnetMask | string | true | None | The current IPv6 subnet mask. |
| ipv6DefaultGateway | string | true | None | The current IPv6 default gateway. |
| arpRedirectEnabled | bool | true | None | True if ARP Redirect is enabled |
| mtu | int | true | None | True if the host bus adapter supports setting its MTU, (for Jumbo   Frames, etc)   Setting enableJumboFrames and not a numeric mtu value implies   autoselection of appropriate MTU value for Jumbo Frames. |
| jumboFramesEnabled | bool | true | None |  |


