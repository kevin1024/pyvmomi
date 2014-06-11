vim.profile.host.NetworkProfile
===============================
inherits from [vim.profile.ApplyProfile](docs/vim.profile.ApplyProfile.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.NetworkProfile.md">NetworkProfile</a> data object contains a set of subprofiles for   network configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vswitch | [vim.profile.host.VirtualSwitchProfile](vim.profile.host.VirtualSwitchProfile.md "vim.profile.host.VirtualSwitchProfile") | true | None | List of virtual switch subprofiles.  Use the <a href="vim.profile.host.VirtualSwitchProfile.md#key">key</a> property to access  a subprofile in the list. |
| vmPortGroup | [vim.profile.host.VmPortGroupProfile](vim.profile.host.VmPortGroupProfile.md "vim.profile.host.VmPortGroupProfile") | true | None | List of port groups for use by virtual machines.  Use the <a href="vim.profile.host.VmPortGroupProfile.md">VmPortGroupProfile</a>.<a href="vim.profile.host.PortGroupProfile.md#key">key</a>  property to access a port group in the list. |
| hostPortGroup | [vim.profile.host.HostPortGroupProfile](vim.profile.host.HostPortGroupProfile.md "vim.profile.host.HostPortGroupProfile") | true | None | List of port groups for use by the host.  Use the <a href="vim.profile.host.HostPortGroupProfile.md">HostPortGroupProfile</a>.<a href="vim.profile.host.PortGroupProfile.md#key">key</a> property  to access port groups in the list. |
| serviceConsolePortGroup | [vim.profile.host.ServiceConsolePortGroupProfile](vim.profile.host.ServiceConsolePortGroupProfile.md "vim.profile.host.ServiceConsolePortGroupProfile") | true | None | List of port groups for use by the service console.   The Profile Engine uses this field only when applying a profile   to a host that has a service console. |
| dnsConfig | [vim.profile.host.NetworkProfile.DnsConfigProfile](vim.profile.host.NetworkProfile.DnsConfigProfile.md "vim.profile.host.NetworkProfile.DnsConfigProfile") | true | None | DNS (Domain Name System) configuration subprofile. |
| ipRouteConfig | [vim.profile.host.IpRouteProfile](vim.profile.host.IpRouteProfile.md "vim.profile.host.IpRouteProfile") | true | None | Subprofile that describes the IP Route  configuration for the VMKernel gateway. |
| consoleIpRouteConfig | [vim.profile.host.IpRouteProfile](vim.profile.host.IpRouteProfile.md "vim.profile.host.IpRouteProfile") | true | None | Subprofile that describes the IP Route configuration  for the Service Console gateway. |
| pnic | [vim.profile.host.PhysicalNicProfile](vim.profile.host.PhysicalNicProfile.md "vim.profile.host.PhysicalNicProfile") | true | None | List of subprofiles that represent physical NIC configuration.  Use the <a href="vim.profile.host.PhysicalNicProfile.md#key">key</a> property to access a  subprofile in the list. |
| dvswitch | [vim.profile.host.DvsProfile](vim.profile.host.DvsProfile.md "vim.profile.host.DvsProfile") | true | None | List of subprofiles for distributed virtual switches to which this host is connected.  Use the <a href="vim.profile.host.DvsProfile.md#key">key</a> property to access a subprofile in the list. |
| dvsServiceConsoleNic | [vim.profile.host.DvsServiceConsoleVNicProfile](vim.profile.host.DvsServiceConsoleVNicProfile.md "vim.profile.host.DvsServiceConsoleVNicProfile") | true | None | List of subprofiles for service console Virtual NICs connected to a distributed virtual switch.  Use the <a href="vim.profile.host.DvsServiceConsoleVNicProfile.md">DvsServiceConsoleVNicProfile</a>.<a href="vim.profile.host.DvsVNicProfile.md#key">key</a> property  to access a subprofile in the list. |
| dvsHostNic | [vim.profile.host.DvsHostVNicProfile](vim.profile.host.DvsHostVNicProfile.md "vim.profile.host.DvsHostVNicProfile") | true | None | List of subprofiles for host Virtual NICs connected to a distributed virtual switch.  Use the <a href="vim.profile.host.DvsHostVNicProfile.md">DvsHostVNicProfile</a>.<a href="vim.profile.host.DvsVNicProfile.md#key">key</a> property  to access a subprofile in the list. |
| netStackInstance | [vim.profile.host.NetStackInstanceProfile](vim.profile.host.NetStackInstanceProfile.md "vim.profile.host.NetStackInstanceProfile") | true | None | List of NetStackInstance subprofiles.  Use the <a href="vim.profile.host.NetStackInstanceProfile.md#key">key</a> property to access  a subprofile in the list. |


