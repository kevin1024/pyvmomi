vim.host.Device
===============
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type defines a device on the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| deviceName | string | None | None | The name of the device on the host. For example,   /dev/cdrom or \\serverX\device_name. |
| deviceType | string | None | None | Device type when available:   floppy, mouse, cdrom, disk, scsi device, or adapter. |


