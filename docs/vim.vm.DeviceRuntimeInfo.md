vim.vm.DeviceRuntimeInfo
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The DeviceRuntimeInfo data object type provides information about   the execution state of a single virtual device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| runtimeState | [vim.vm.DeviceRuntimeInfo.DeviceRuntimeState](vim.vm.DeviceRuntimeInfo.DeviceRuntimeState.md "vim.vm.DeviceRuntimeInfo.DeviceRuntimeState") | None | None | The device runtime state. |
| key | int | None | None | The device key. |


