vim.host.PciPassthruConfig
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object provides information about the state of PciPassthru   for all pci devices.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | The name ID of this PCI, composed of "bus:slot.function". |
| passthruEnabled | bool | None | None | Whether passThru is has been configured for this device |


