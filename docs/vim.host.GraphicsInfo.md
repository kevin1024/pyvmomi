vim.host.GraphicsInfo
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This data object type describes information about a single   graphics device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| deviceName | string | None | None | The device name. |
| vendorName | string | None | None | The vendor name. |
| pciId | string | None | None | PCI ID of this device composed of "bus:slot.function". |
| graphicsType | string | None | None | Graphics type (@see GraphicsType). |
| memorySizeInKB | long | None | None | Memory capacity of graphics device or zero if not available. |
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | true | None | Virtual machines using this graphics device. |


