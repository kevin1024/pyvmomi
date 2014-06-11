vim.vm.ScsiDiskDeviceInfo
=========================
inherits from [vim.vm.DiskDeviceInfo](docs/vim.vm.DiskDeviceInfo.md)


The ScsiDiskDeviceInfo class contains detailed information about a specific   scsi disk hardware device. These devices are for the   vim.vm.device.VirtualDisk.RawDiskMappingVer1BackingInfo.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| disk | [vim.host.ScsiDisk](vim.host.ScsiDisk.md "vim.host.ScsiDisk") | true | None | Detailed information about the disk. |
| transportHint | string | true | None | Transport identifier hint used to identify the device.  To definitively   correlate this device with a host physical disk, use the disk property.   This identifier is intended as a hint to end users to identify the   disk device. |
| lunNumber | int | true | None | LUN number hint used to identify the SCSI device.  To definitively   correlate this device with a host physical disk, use the disk property.   This identifier is intended as a hint to end users to identify the   disk device. |


