vim.host.PhysicalNic.CdpDeviceCapability
========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


The capability of the CDP-awared device that connects to a Physical NIC.   <a href="vim.host.PhysicalNic.CdpInfo.md">PhysicalNicCdpInfo</a>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| router | bool | None | None | The CDP-awared device has the capability of a routing for    at least one network layer protocol |
| transparentBridge | bool | None | None | The CDP-awared device has the capability of transparent    bridging |
| sourceRouteBridge | bool | None | None | The CDP-awared device has the capability of source-route    bridging |
| networkSwitch | bool | None | None | The CDP-awared device has the capability of switching. The    difference between this capability and transparentBridge is    that a switch does not run the Spanning-Tree Protocol. This    device is assumed to be deployed in a physical loop-free topology. |
| host | bool | None | None | The CDP-awared device has the capability of a host, which    Sends and receives packets for at least one network layer protocol. |
| igmpEnabled | bool | None | None | The CDP-awared device is IGMP-enabled, which does not forward IGMP    Report packets on nonrouter ports. |
| repeater | bool | None | None | The CDP-awared device has the capability of a repeater |


