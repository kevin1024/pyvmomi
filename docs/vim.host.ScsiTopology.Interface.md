vim.host.ScsiTopology.Interface
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the SCSI interface that is associated   with a list of targets.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The identifier for the SCSI interface |
| adapter | [vim.host.HostBusAdapter](vim.host.HostBusAdapter.md "vim.host.HostBusAdapter") | None | None | The link to data for this SCSI interface. |
| target | [vim.host.ScsiTopology.Target](vim.host.ScsiTopology.Target.md "vim.host.ScsiTopology.Target") | true | None | The list of targets to which the SCSI interface is associated. |


