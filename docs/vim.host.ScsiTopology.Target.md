vim.host.ScsiTopology.Target
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the SCSI target that is associated   with a list of logical units.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The identifier for the SCSI target |
| target | int | None | None | The target identifier. |
| lun | [vim.host.ScsiTopology.Lun](vim.host.ScsiTopology.Lun.md "vim.host.ScsiTopology.Lun") | true | None | The list of SCSI logical units with which a target is associated. |
| transport | [vim.host.TargetTransport](vim.host.TargetTransport.md "vim.host.TargetTransport") | true | None | SCSI Transport information about the target. |


