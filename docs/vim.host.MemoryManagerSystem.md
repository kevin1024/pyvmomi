vim.host.MemoryManagerSystem
============================
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")


The MemoryManagerSystem managed object provides an interface through which   the host memory management policies that affect the performance of running   virtual machines can be gathered and configured.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='consoleReservationInfo'>consoleReservationInfo</a> | [vim.host.MemoryManagerSystem.ServiceConsoleReservationInfo](vim.host.MemoryManagerSystem.ServiceConsoleReservationInfo.md "vim.host.MemoryManagerSystem.ServiceConsoleReservationInfo") | true | None | Service console reservation information for the memory manager.  The   existence of this data object indicates if the service console memory   reservation must be configured for this host. |
| <a href='virtualMachineReservationInfo'>virtualMachineReservationInfo</a> | [vim.host.MemoryManagerSystem.VirtualMachineReservationInfo](vim.host.MemoryManagerSystem.VirtualMachineReservationInfo.md "vim.host.MemoryManagerSystem.VirtualMachineReservationInfo") | true | None | Virtual machine reservation information for the memory manager.  The   existence of this data object indicates if the virtual machine memory   reservation must be configured for this host. |


ReconfigureServiceConsoleReservation()
--------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | ReconfigureServiceConsoleReservation |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Memory |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if cfgBytes is negative or is greater than                           the total memory available. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the service console memory reservation does not                         apply to this host.  The existence of the                         consoleReservation property will indicate if this                         feature is applicable. |




ReconfigureVirtualMachineReservation([spec](vim.host.MemoryManagerSystem.VirtualMachineReservationSpec.md "vim.host.MemoryManagerSystem.VirtualMachineReservationSpec"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | ReconfigureVirtualMachineReservation |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Host.Config.Memory |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if virtualMachineReserved is negative or is           greater than the maximum amount reservable. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the virtualMachine reservation does not apply           to this host. The existence of the virtualMachineReservationInfo           property will indicate if this feature is applicable. |




