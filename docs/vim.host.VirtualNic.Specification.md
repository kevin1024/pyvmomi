vim.host.VirtualNic.Specification
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.host.VirtualNic.Specification.md">HostVirtualNicSpec</a> data object   describes the <a href="vim.host.VirtualNic.md">HostVirtualNic</a> configuration    containing both the configured properties on a   virtual NIC and identification information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ip | [vim.host.IpConfig](vim.host.IpConfig.md "vim.host.IpConfig") | true | None | IP configuration on the virtual network adapter. |
| mac | string | true | None | Media access control (MAC) address of the virtual   network adapter. |
| distributedVirtualPort | [vim.dvs.PortConnection](vim.dvs.PortConnection.md "vim.dvs.PortConnection") | true | None | <a href="vim.dvs.DistributedVirtualPort.md">DistributedVirtualPort</a> or <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a>   connection. To specify a port connection, set the   <a href="vim.dvs.PortConnection.md#portKey">portKey</a> property.   To specify a portgroup connection, set the   <a href="vim.dvs.PortConnection.md#portgroupKey">portgroupKey</a> property. |
| portgroup | string | true | None | Portgroup (<a href="vim.dvs.DistributedVirtualPortgroup.md#key">key</a>)   to which the virtual NIC is connected.    <p>   When reconfiguring a virtual NIC, this property indicates the new portgroup   to which the virtual NIC should connect. You can specify this property   only if you do not specify <a href="vim.host.VirtualNic.Specification.md#distributedVirtualPort">distributedVirtualPort</a>. |
| mtu | int | true | None | Maximum transmission unit for packets size in bytes for the   virtual NIC. This property is applicable to VMkernel virtual   NICs and will be ignored if specified for service console virtual    NICs. If not specified, the Server will use the system default value. |
| tsoEnabled | bool | true | None | Flag enabling or disabling TCP segmentation offset for a virtual NIC.   This property is applicable to VMkernel virtual NICs and will be   ignored if specified for service console vitual nics. If not specified,   a default value of true shall be used. |
| netStackInstanceKey | string | true | None | The NetStackInstance that the vNic uses, the value of this property    is default to be <a href="vim.host.NetStackInstance.SystemStackKey.md#defaultTcpipStack">defaultTcpipStack</a> |


