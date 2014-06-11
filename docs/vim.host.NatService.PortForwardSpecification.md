vim.host.NatService.PortForwardSpecification
============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object type describes the   Network Address Translation (NAT) port forwarding specification.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| type | string | None | None | Either "tcp" or "udp". |
| name | string | None | None | The user-defined name to identify the service being forwarded.     No white spaces are allowed in the string. |
| hostPort | int | None | None | The port number on the host.  Network traffic sent to the host on this   TCP/UDP port is forwarded to the guest at the specified IP address   and port. |
| guestPort | int | None | None | The port number for the guest.  Network traffic from the host is   forwarded to this port. |
| guestIpAddress | string | None | None | The IP address for the guest.  Network traffic from the host is   forwarded to this IP address. |


