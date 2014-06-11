vim.host.CpuSchedulerSystem.HyperThreadScheduleInfo
===================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the CpuSchedulerSystem configuration    for optimizing hyperthreading.  The primary hyperthreading    optimization employed by the CpuSchedulerSystem is to utilize    hyperthreads as additional schedulable resources.  Although    hyperthreads provide limited additional concurrency,   certain workloads (such as idling) can take advantage of    these hyperthreads.  This is particularly useful for SMP virtual    machines that use gang scheduling.  (Gang scheduling refers to a   situation in which all of a parallel program's tasks are grouped   into a "gang" and concurrently scheduled on distinct   processors of a parallel computer system.)   <p>   Changes to the hyperthreading optimization can take effect only    after a system restart.  Therefore, while it is possible to change    the configuration at any time, the change will take effect only    on the next boot.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| available | bool | None | None | The flag to indicate whether or not hyperthreading    optimization is available on the system.  This property    is set by VMware prior to installation. |
| active | bool | None | None | The flag to indicate whether or not the CPU scheduler is    currently treating    hyperthreads as schedulable resources.  Setting this property   involves a successful invocation of either the   <a href="vim.host.CpuSchedulerSystem.md#enableHyperThreading">enableHyperThreading()</a> method ("true") or the    <a href="vim.host.CpuSchedulerSystem.md#disableHyperThreading">disableHyperthreading()</a> method    ("false").  The property is set once the system is rebooted. |
| config | bool | None | None | The flag to indicate whether or not the CPU scheduler    should treat hyperthreads as    schedulable resources the next time the CPU scheduler starts.    <p>   <ul>   <li>This property is set to "true" by successfully invoking the    <a href="vim.host.CpuSchedulerSystem.md#enableHyperThreading">enableHyperThreading()</a> method.   <li>This property is set to "false" by successfully invoking the    <a href="vim.host.CpuSchedulerSystem.md#disableHyperThreading">disableHyperthreading()</a> method. |


