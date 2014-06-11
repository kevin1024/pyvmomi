vim.host.HostProxySwitch
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The HostProxySwitch is a software entity which represents the component    of a DistributedVirtualSwitch on a particular host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dvsUuid | string | None | None | The uuid of the DistributedVirtualSwitch that the HostProxySwitch    is a part of. |
| dvsName | string | None | None | The name of the DistributedVirtualSwitch that the HostProxySwitch  is part of. |
| key | string | None | None | The proxy switch key. |
| numPorts | int | None | None | The number of ports that this switch currently has. |
| configNumPorts | int | true | None | The configured number of ports that this switch has.  If configured number of ports is changed,  a host reboot is required for the new value to take effect. |
| numPortsAvailable | int | None | None | The number of ports that are available on this virtual switch. |
| uplinkPort | [vim.KeyValue](vim.KeyValue.md "vim.KeyValue") | true | None | The list of ports that can be potentially used by physical nics.   This property contains the keys and names of such ports. |
| mtu | int | true | None | The maximum transmission unit (MTU) associated with this switch   in bytes. |
| pnic | [vim.host.PhysicalNic](vim.host.PhysicalNic.md "vim.host.PhysicalNic") | true | None | The set of physical network adapters associated with this switch. |
| spec | [vim.host.HostProxySwitch.Specification](vim.host.HostProxySwitch.Specification.md "vim.host.HostProxySwitch.Specification") | None | None | The specification of the switch. |
| hostLag | [vim.host.HostProxySwitch.HostLagConfig](vim.host.HostProxySwitch.HostLagConfig.md "vim.host.HostProxySwitch.HostLagConfig") | true | None | The Link Aggregation Control Protocol group and   Uplink ports in the group. |
| networkReservationSupported | bool | true | None | Indicates whether network reservation is supported on this switch |


