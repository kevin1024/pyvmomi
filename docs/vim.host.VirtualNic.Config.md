vim.host.VirtualNic.Config
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.host.VirtualNic.Config.md">HostVirtualNicConfig</a> data object describes the Virtual NIC configuration.    It represents both the configured properties on a <a href="vim.host.VirtualNic.md">HostVirtualNic</a> and identification information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| changeOperation | string | true | None | Change operation to apply on this configuration   specification.<br>See <a href="vim.host.ConfigChange.Operation.md">HostConfigChangeOperation</a><br> |
| device | string | true | None | Virtual NIC device to which configuration applies  (<a href="vim.host.VirtualNic.md">HostVirtualNic</a>.<a href="vim.host.VirtualNic.md#device">device</a>). |
| portgroup | string | None | None | If the Virtual NIC is connecting to a vSwitch, this property is the name of   portgroup connected. If the Virtual NIC is connecting to a   <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>, this property is ignored. |
| spec | [vim.host.VirtualNic.Specification](vim.host.VirtualNic.Specification.md "vim.host.VirtualNic.Specification") | true | None | Specification of the virtual network adapter. |


