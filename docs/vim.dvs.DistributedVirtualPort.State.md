vim.dvs.DistributedVirtualPort.State
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The state of a DistributedVirtualPort.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| runtimeInfo | [vim.dvs.DistributedVirtualPort.RuntimeInfo](vim.dvs.DistributedVirtualPort.RuntimeInfo.md "vim.dvs.DistributedVirtualPort.RuntimeInfo") | true | None | Run time information of the port.   This property is set only when the port is running. |
| stats | [vim.dvs.PortStatistics](vim.dvs.PortStatistics.md "vim.dvs.PortStatistics") | None | None | Statistics of the port. |
| vendorSpecificState | [vim.dvs.KeyedOpaqueBlob](vim.dvs.KeyedOpaqueBlob.md "vim.dvs.KeyedOpaqueBlob") | true | None | Opaque binary blob that stores vendor-specific runtime state data. |


