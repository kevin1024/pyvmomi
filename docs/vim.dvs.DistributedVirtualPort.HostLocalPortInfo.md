vim.dvs.DistributedVirtualPort.HostLocalPortInfo
================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


This data object type describes the information about the host local port.   A host local port is  created to resurrect the management network connection   on a VMkernel Virtual NIC.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| switchUuid | string | None | None | UUID of the vSphere Distributed Switch that management interface is connected to. |
| portKey | string | None | None | Portkey of the DVPort that management interface is now connected to. |
| setting | [vim.dvs.DistributedVirtualPort.Setting](vim.dvs.DistributedVirtualPort.Setting.md "vim.dvs.DistributedVirtualPort.Setting") | None | None | The configuration of the new host local port. |
| vnic | string | None | None | The Virtual NIC device connected to this port |


