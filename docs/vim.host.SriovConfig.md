vim.host.SriovConfig
====================
inherits from [vim.host.PciPassthruConfig](docs/vim.host.PciPassthruConfig.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This data object allows configuration of SR-IOV device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sriovEnabled | bool | None | None | enable SR-IOV for this device |
| numVirtualFunction | int | None | None | Number of SR-IOV virtual functions to enable on this device |


