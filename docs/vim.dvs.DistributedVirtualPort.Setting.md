vim.dvs.DistributedVirtualPort.Setting
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.dvs.DistributedVirtualPort.Setting.md">DVPortSetting</a> data object  describes the network configuration of a <a href="vim.dvs.DistributedVirtualPort.md">DistributedVirtualPort</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| blocked | [vim.BoolPolicy](vim.BoolPolicy.md "vim.BoolPolicy") | true | None | Indicates whether this port is blocked. If a port is blocked,  packet forwarding is stopped. |
| vmDirectPathGen2Allowed | [vim.BoolPolicy](vim.BoolPolicy.md "vim.BoolPolicy") | true | None | Indicates whether this port is allowed to do VMDirectPath Gen2 network passthrough.  Direct path capability is defined at host, switch, and device levels.  See the <code>vmDirectPathGen2Supported</code> properties on the  <a href="vim.DistributedVirtualSwitch.FeatureCapability.md">DVSFeatureCapability</a>,  <a href="vim.host.Capability.md">HostCapability</a>, <a href="vim.host.PhysicalNic.md">PhysicalNic</a>,  and <a href="vim.vm.device.VirtualEthernetCardOption.md">VirtualEthernetCardOption</a> objects. |
| inShapingPolicy | [vim.dvs.DistributedVirtualPort.TrafficShapingPolicy](vim.dvs.DistributedVirtualPort.TrafficShapingPolicy.md "vim.dvs.DistributedVirtualPort.TrafficShapingPolicy") | true | None | Network shaping policy for controlling throughput of inbound traffic. |
| outShapingPolicy | [vim.dvs.DistributedVirtualPort.TrafficShapingPolicy](vim.dvs.DistributedVirtualPort.TrafficShapingPolicy.md "vim.dvs.DistributedVirtualPort.TrafficShapingPolicy") | true | None | Network shaping policy for controlling throughput of outbound traffic. |
| vendorSpecificConfig | [vim.dvs.DistributedVirtualPort.VendorSpecificConfig](vim.dvs.DistributedVirtualPort.VendorSpecificConfig.md "vim.dvs.DistributedVirtualPort.VendorSpecificConfig") | true | None | Opaque binary blob that stores vendor specific configuration. |
| networkResourcePoolKey | [vim.StringPolicy](vim.StringPolicy.md "vim.StringPolicy") | true | None | The key of user defined network resource pool to be associated with a port.  The default value for this property is "-1", indicating that  this port is not associated with any network resource pool. |
| filterPolicy | [vim.dvs.DistributedVirtualPort.FilterPolicy](vim.dvs.DistributedVirtualPort.FilterPolicy.md "vim.dvs.DistributedVirtualPort.FilterPolicy") | true | None | Configuration for Network Filter Policy. |


