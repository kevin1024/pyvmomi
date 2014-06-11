vim.vm.FaultToleranceConfigInfo
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


FaultToleranceConfigInfo is a data object type containing Fault Tolerance   settings for this virtual machine.   role, instanceUuids and configPaths contain information about the    whole fault tolerance group.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| role | int | None | None | The index of the current VM in instanceUuids array starting from 1, so    1 means that it is the primary VM. |
| instanceUuids | string | None | None | The instanceUuid of all the VMs in this fault tolerance group. The   first element is the instanceUuid of the primary VM. |
| configPaths | string | None | None | The configuration file path for all the VMs in this fault tolerance   group. |


