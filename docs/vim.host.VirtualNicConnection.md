vim.host.VirtualNicConnection
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


DataObject which provides a level of indirection when   identifying VirtualNics during configuration.   This dataObject lets users specify a VirtualNic in terms of   the portgroup/Dv Port the Virtual NIC is connected to.      This is useful in cases where VirtualNic will be created as part of   a configuration operation and the created VirtualNic is referred to   in some other part of configuration. e.g: for configuring VMotion

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| portgroup | string | true | None | Name of the portgroup to which the virtual nic is connected to.   If this parameter is set, use a virtual nic connected to   a legacy portgroup. |
| dvPort | [vim.dvs.PortConnection](vim.dvs.PortConnection.md "vim.dvs.PortConnection") | true | None | Identifier for the DistributedVirtualPort.   If the virtual nic is to be connected to a DVS,   #dvPort will be set instead of #portgroup |


