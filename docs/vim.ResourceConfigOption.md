vim.ResourceConfigOption
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


This data object type is a default value and value range specification   for <a href="vim.ResourceConfigSpec.md">ResourceConfigSpec</a> object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| cpuAllocationOption | [vim.ResourceAllocationOption](vim.ResourceAllocationOption.md "vim.ResourceAllocationOption") | None | None | Resource allocation options for CPU.<br>See <a href="vim.ResourceAllocationInfo.md">ResourceAllocationInfo</a><br> |
| memoryAllocationOption | [vim.ResourceAllocationOption](vim.ResourceAllocationOption.md "vim.ResourceAllocationOption") | None | None | Resource allocation options for memory.<br>See <a href="vim.ResourceAllocationInfo.md">ResourceAllocationInfo</a><br> |


