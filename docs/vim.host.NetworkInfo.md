vim.host.NetworkInfo
====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes networking host    configuration data objects.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vswitch | [vim.host.VirtualSwitch](vim.host.VirtualSwitch.md "vim.host.VirtualSwitch") | true | None | Virtual switches configured on the host. |
| proxySwitch | [vim.host.HostProxySwitch](vim.host.HostProxySwitch.md "vim.host.HostProxySwitch") | true | None | Proxy switches configured on the host. |
| portgroup | [vim.host.PortGroup](vim.host.PortGroup.md "vim.host.PortGroup") | true | None | Port groups configured on the host. |
| pnic | [vim.host.PhysicalNic](vim.host.PhysicalNic.md "vim.host.PhysicalNic") | true | None | Physical network adapters as seen by the primary operating system. |
| vnic | [vim.host.VirtualNic](vim.host.VirtualNic.md "vim.host.VirtualNic") | true | None | Virtual network adapters configured on the host (hosted products)    or the vmkernel.   In the hosted architecture, these network adapters are used by the    host to   communicate with the virtual machines running on that host.  In the   VMkernel architecture, these virtual network adapters provide the    ESX Server with    external network access through a virtual switch that is bridged to a   physical network adapter.  The VMkernel uses these network adapters   for features such as VMotion, NAS, iSCSI, and remote MKS connections. |
| consoleVnic | [vim.host.VirtualNic](vim.host.VirtualNic.md "vim.host.VirtualNic") | true | None | Virtual network adapters configured for use by the service console.   The service   console uses this network access for system management and bootstrapping   services like network boot.    The two sets of virtual network adapters are mutually exclusive.     A virtual network adapter   in this list cannot be used for things like VMotion.  Likewise, a   virtual network adapter in the other list cannot be used by the    service console. |
| dnsConfig | [vim.host.DnsConfig](vim.host.DnsConfig.md "vim.host.DnsConfig") | true | None | Client-side DNS configuration. |
| ipRouteConfig | [vim.host.IpRouteConfig](vim.host.IpRouteConfig.md "vim.host.IpRouteConfig") | true | None | IP route configuration. |
| consoleIpRouteConfig | [vim.host.IpRouteConfig](vim.host.IpRouteConfig.md "vim.host.IpRouteConfig") | true | None | IP route configuration of the service console. |
| routeTableInfo | [vim.host.IpRouteTableInfo](vim.host.IpRouteTableInfo.md "vim.host.IpRouteTableInfo") | true | None | IP routing table |
| dhcp | [vim.host.DhcpService](vim.host.DhcpService.md "vim.host.DhcpService") | true | None | DHCP Service instances configured on the host. |
| nat | [vim.host.NatService](vim.host.NatService.md "vim.host.NatService") | true | None | NAT service instances configured on the host. |
| ipV6Enabled | bool | true | None | Enable or disable IPv6 protocol on this system. |
| atBootIpV6Enabled | bool | true | None | If true then dual IPv4/IPv6 stack enabled else IPv4 only. |
| netStackInstance | [vim.host.NetStackInstance](vim.host.NetStackInstance.md "vim.host.NetStackInstance") | true | None | List of NetStackInstances |
| opaqueSwitch | [vim.host.OpaqueSwitch](vim.host.OpaqueSwitch.md "vim.host.OpaqueSwitch") | true | None | List of opaque switches configured on the host. |
| opaqueNetwork | [vim.host.OpaqueNetworkInfo](vim.host.OpaqueNetworkInfo.md "vim.host.OpaqueNetworkInfo") | true | None | List of opaque networks |


