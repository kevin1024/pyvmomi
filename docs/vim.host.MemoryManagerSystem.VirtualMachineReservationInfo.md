vim.host.MemoryManagerSystem.VirtualMachineReservationInfo
==========================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


The VirtualMachineReservationInfo data object type describes the   amount of memory that is being reserved for virtual machines on   the host, and how additional memory may be acquired.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| virtualMachineMin | long | None | None | The minimum amount of memory reserved for all running virtual machines,   in bytes. |
| virtualMachineMax | long | None | None | The maximum amount of memory reserved for all running virtual machines,   in bytes. |
| virtualMachineReserved | long | None | None | The amount of memory reserved for all running virtual machines,    in bytes. |
| allocationPolicy | string | None | None | Policy for allocating additional memory for virtual machines.<br>See AllocationPolicy |


