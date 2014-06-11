vim.vsan.host.DiskMapResult
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


A DiskMapResult represents the result of an operation performed  on the set of disks in a <a href="vim.vsan.host.DiskMapping.md">VsanHostDiskMapping</a>.<br>See <a href="vim.host.VsanSystem.md#initializeDisks">InitializeDisks_Task</a><br>See <a href="vim.host.VsanSystem.md#update">UpdateVsan_Task</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| mapping | [vim.vsan.host.DiskMapping](vim.vsan.host.DiskMapping.md "vim.vsan.host.DiskMapping") | None | None | DiskMapping for this result. |
| diskResult | [vim.vsan.host.DiskResult](vim.vsan.host.DiskResult.md "vim.vsan.host.DiskResult") | true | None | List of results for each disk in the mapping. |
| error | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | Error information for this result.<br>See <a href="vim.fault.VsanDiskFault.md">VsanDiskFault</a><br> |


