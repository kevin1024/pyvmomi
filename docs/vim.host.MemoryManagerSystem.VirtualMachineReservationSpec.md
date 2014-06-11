vim.host.MemoryManagerSystem.VirtualMachineReservationSpec
==========================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


The VirtualMachineReservationSpec data object specifies    configurable parameters for virtual machine memory reservation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| virtualMachineReserved | long | true | None | The amount of memory reserved for all running virtual machines, in   bytes. |
| allocationPolicy | string | true | None | Policy for allocating additional memory for virtual machines.<br>See VirtualMachineReservationInfo.AllocationPolicy |


