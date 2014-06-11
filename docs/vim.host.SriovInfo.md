vim.host.SriovInfo
==================
inherits from [vim.host.PciPassthruInfo](docs/vim.host.PciPassthruInfo.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This data object provides information about the state of SR-IOV device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sriovEnabled | bool | None | None | Whether SRIOV has been enabled by the user |
| sriovCapable | bool | None | None | Whether SRIOV is possible for this device |
| sriovActive | bool | None | None | Whether SRIOV is active for this device (meaning enabled + rebooted) |
| numVirtualFunctionRequested | int | None | None | Number of SRIOV virtual functions requested for this device |
| numVirtualFunction | int | None | None | Number of SRIOV virtual functions present on this device |
| maxVirtualFunctionSupported | int | None | None | Maximum number of SRIOV virtual functions supported on this device |


