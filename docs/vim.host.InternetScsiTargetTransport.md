vim.host.InternetScsiTargetTransport
====================================
inherits from [vim.host.TargetTransport](docs/vim.host.TargetTransport.md)


Internet SCSI transport information about a SCSI target.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| iScsiName | string | None | None | The iSCSI name of the target. |
| iScsiAlias | string | None | None | The iSCSI alias of the target. |
| address | string | true | None | The IP addresses through which the target may be reached. |


