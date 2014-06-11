vim.host.CpuSchedulerSystem
===========================
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")


This managed object provides an interface    through which you can gather and configure the host CPU scheduler    policies that affect the performance of running virtual machines.   <p>   <b>Note</b>: This managed object is useful only on platforms where   resource management controls are available to optimize the running   of virtual machines.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='hyperthreadInfo'>hyperthreadInfo</a> | [vim.host.CpuSchedulerSystem.HyperThreadScheduleInfo](vim.host.CpuSchedulerSystem.HyperThreadScheduleInfo.md "vim.host.CpuSchedulerSystem.HyperThreadScheduleInfo") | true | None | The hyperthread configuration for the CpuSchedulerSystem.  The    existence of this data object type indicates if the CPU scheduler    is capable of scheduling hyperthreads as resources. |


EnableHyperThreading()
----------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | EnableHyperThreading |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.HyperThreading |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the hyperthreading optimization is not available           on the host (the boolean <a href="vim.host.CpuSchedulerSystem.HyperThreadScheduleInfo.md#available">available</a>            is set to false). |




DisableHyperThreading()
-----------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | DisableHyperThreading |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.HyperThreading |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the hyperthreading optimization is not available           on the host (the boolean <a href="vim.host.CpuSchedulerSystem.HyperThreadScheduleInfo.md#available">available</a>           is set to false). |




