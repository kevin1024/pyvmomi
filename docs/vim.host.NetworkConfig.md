vim.host.NetworkConfig
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes networking host configuration data objects.   These objects contain only the configuration information for networking.     The runtime information is available from the    <a href="vim.host.NetworkInfo.md">NetworkInfo</a> data object type.<br>See <a href="vim.host.NetworkInfo.md">HostNetworkInfo</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vswitch | [vim.host.VirtualSwitch.Config](vim.host.VirtualSwitch.Config.md "vim.host.VirtualSwitch.Config") | true | None | Virtual switches configured on the host. |
| proxySwitch | [vim.host.HostProxySwitch.Config](vim.host.HostProxySwitch.Config.md "vim.host.HostProxySwitch.Config") | true | None | Host proxy switches configured on the host. |
| portgroup | [vim.host.PortGroup.Config](vim.host.PortGroup.Config.md "vim.host.PortGroup.Config") | true | None | Port groups configured on the host. |
| pnic | [vim.host.PhysicalNic.Config](vim.host.PhysicalNic.Config.md "vim.host.PhysicalNic.Config") | true | None | Physical network adapters as seen by the primary operating system. |
| vnic | [vim.host.VirtualNic.Config](vim.host.VirtualNic.Config.md "vim.host.VirtualNic.Config") | true | None | Virtual network adapters configured for use by the host    operating system network adapter. |
| consoleVnic | [vim.host.VirtualNic.Config](vim.host.VirtualNic.Config.md "vim.host.VirtualNic.Config") | true | None | Virtual network adapters configured for use by the Service    Console. |
| dnsConfig | [vim.host.DnsConfig](vim.host.DnsConfig.md "vim.host.DnsConfig") | true | None | Client-side DNS configuration for the host.  The DNS configuration is   global to the entire host. |
| ipRouteConfig | [vim.host.IpRouteConfig](vim.host.IpRouteConfig.md "vim.host.IpRouteConfig") | true | None | IP route configuration of the host. |
| consoleIpRouteConfig | [vim.host.IpRouteConfig](vim.host.IpRouteConfig.md "vim.host.IpRouteConfig") | true | None | IP route configuration of the service console. |
| routeTableConfig | [vim.host.IpRouteTableConfig](vim.host.IpRouteTableConfig.md "vim.host.IpRouteTableConfig") | true | None | IP routing table configuration of the host. |
| dhcp | [vim.host.DhcpService.Config](vim.host.DhcpService.Config.md "vim.host.DhcpService.Config") | true | None | Dynamic Host Control Protocol (DHCP) Service instances configured   on the host. |
| nat | [vim.host.NatService.Config](vim.host.NatService.Config.md "vim.host.NatService.Config") | true | None | Network address translation (NAT) Service instances configured    on the host. |
| ipV6Enabled | bool | true | None | Enable or disable IPv6 protocol on this system.   This property must be set by itself, no other property can accompany  this change. Following the successful change, the system should be rebooted to   have the change take effect. |
| netStackSpec | [vim.host.NetworkConfig.NetStackSpec](vim.host.NetworkConfig.NetStackSpec.md "vim.host.NetworkConfig.NetStackSpec") | true | None | The list of network stack instance spec |


