vim.ResourcePool.Summary
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type encapsulates a typical set of resource   pool information that is useful for list views and summary pages.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | Name of resource pool. |
| config | [vim.ResourceConfigSpec](vim.ResourceConfigSpec.md "vim.ResourceConfigSpec") | None | None | Current configuration of the resource pool. |
| runtime | [vim.ResourcePool.RuntimeInfo](vim.ResourcePool.RuntimeInfo.md "vim.ResourcePool.RuntimeInfo") | None | None | Current runtime state of the resource pool. |
| quickStats | [vim.ResourcePool.Summary.QuickStats](vim.ResourcePool.Summary.QuickStats.md "vim.ResourcePool.Summary.QuickStats") | true | None | A set of statistics that are typically updated with near real-time regularity.   This data object type does not support notification, for scalability reasons.   Therefore, changes in QuickStats do not generate property collector updates.   To monitor statistics values, use the statistics and alarms modules instead. |
| configuredMemoryMB | int | true | None | Total configured memory of all virtual machines in the resource pool, in MB. |


