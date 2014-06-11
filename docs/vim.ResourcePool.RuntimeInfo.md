vim.ResourcePool.RuntimeInfo
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Current runtime resource usage and state of the resource pool

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| memory | [vim.ResourcePool.ResourceUsage](vim.ResourcePool.ResourceUsage.md "vim.ResourcePool.ResourceUsage") | None | None | Runtime resource usage for memory. Values are in bytes. |
| cpu | [vim.ResourcePool.ResourceUsage](vim.ResourcePool.ResourceUsage.md "vim.ResourcePool.ResourceUsage") | None | None | Runtime resource usage for CPU. Values are in Mhz. |
| overallStatus | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | None | None | Overall health of the tree. See header for description of various  statuses and when they are set |


