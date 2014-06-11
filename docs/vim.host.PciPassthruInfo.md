vim.host.PciPassthruInfo
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object provides information about the state of PciPassthru   for all pci devices.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | The name ID of this PCI, composed of "bus:slot.function". |
| dependentDevice | string | None | None | Device which needs to be unclaimed by vmkernel (may be bridge) |
| passthruEnabled | bool | None | None | Whether passThru has been configured by the user |
| passthruCapable | bool | None | None | Whether passThru is even possible for this device (decided by vmkctl) |
| passthruActive | bool | None | None | Whether passThru is active for this device (meaning enabled + rebooted) |


