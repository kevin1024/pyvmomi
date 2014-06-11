vim.PerformanceManager.CounterInfo
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type contains metadata for a performance counter. See   <a href="vim.PerformanceManager.md">PerformanceManager</a> for definitions of available counters.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | int | None | None | A system-generated number that uniquely identifies the counter in the   context of the system. The performance counter ID. |
| nameInfo | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | The name of the counter with label and summary details. For example,   the counter with name "usage" for the "cpu" group of performance   counters. |
| groupInfo | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | The group of the performance counter with its label and summary   details. Counter groups include "cpu," "mem," "net," "disk," "system,"   "rescpu," and "clusterServices," for example. |
| unitInfo | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | The unit for the values of the performance counter with its label and   summary details. See <a href="vim.PerformanceManager.CounterInfo.Unit.md">PerformanceManagerUnit</a> for a   description of the valid values. |
| rollupType | [vim.PerformanceManager.CounterInfo.RollupType](vim.PerformanceManager.CounterInfo.RollupType.md "vim.PerformanceManager.CounterInfo.RollupType") | None | None | The counter type. Valid values include average, maximum, minimum,   latest, summation, or none. This determines the type of statistical   values that are returned for the counter. None means that the counter   is never rolled up. |
| statsType | [vim.PerformanceManager.CounterInfo.StatsType](vim.PerformanceManager.CounterInfo.StatsType.md "vim.PerformanceManager.CounterInfo.StatsType") | None | None | Statistics type for the counter. Valid values include absolute, delta,   or rate. |
| level | int | true | None | Minimum level at which metrics of this type will be collected by   VirtualCenter Server. The value for this property for any performance   counter is a number from 1 to 4. The higher the setting, the more data   is collected by VirtualCenter Server. The default setting for   VirtualCenter Server is 1, which collects the minimal amount of   performance data that is typically useful to administrators and   developers alike. The specific level of each counter is documented in   the respective counter-documentation pages, by group. See <a href="vim.PerformanceManager.md">PerformanceManager</a> for links to the counter group pages. |
| perDeviceLevel | int | true | None | Minimum level at which the per device metrics of this type will be   collected by vCenter Server. The value for this property for any   performance counter is a number from 1 to 4. By default all per device   metrics are calculated at level 3 or more. If a certain per device   counter is collected at a certain level, the aggregate metric is also   calculated at that level, i.e., perDeviceLevel is greater than or   equal to level. |
| associatedCounterId | int | true | None | The counter IDs associated with the same performance counter name for   the same device type. For example, the rollup types for CPU Usage for   a host are average, minimum, and maximum&#46; Therefore, their counter   IDs are associated. |


