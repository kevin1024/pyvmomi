vim.host.ScsiTopology.Lun
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the SCSI logical unit.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The identifier for the SCSI Lun |
| lun | int | None | None | The logical unit number of the SCSI logical unit. |
| scsiLun | [vim.host.ScsiLun](vim.host.ScsiLun.md "vim.host.ScsiLun") | None | None | The link to data for this SCSI logical unit. |


