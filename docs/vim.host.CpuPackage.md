vim.host.CpuPackage
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about a physical CPU package.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| index | short | None | None | Package index, starting from zero. |
| vendor | string | None | None | CPU vendor name, possible names currently are "Intel", "AMD",   or "unknown". |
| hz | long | None | None | CPU speed in HZ. |
| busHz | long | None | None | Bus speed in HZ. |
| description | string | None | None | String summary description of CPU (for display purposes). |
| threadId | short | None | None | The logical CPU threads on this package. |
| cpuFeature | [vim.host.CpuIdInfo](vim.host.CpuIdInfo.md "vim.host.CpuIdInfo") | true | None | The CPU feature bit on this particular CPU. This is independent of   the product and licensing capabilities. |


