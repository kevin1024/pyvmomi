vim.vsan.host.DiskResult
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


A DiskResult represents the result of VSAN configuration operation  on a ScsiDisk, and its current eligibility state for use by  the VSAN service.<br>See <a href="vim.host.VsanSystem.md#queryDisksForVsan">QueryDisksForVsan</a><br>See <a href="vim.host.VsanSystem.md#update">UpdateVsan_Task</a><br>See <a href="vim.vsan.host.DiskResult.State.md">VsanHostDiskResultState</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| disk | [vim.host.ScsiDisk](vim.host.ScsiDisk.md "vim.host.ScsiDisk") | None | None | Disk for this result. |
| state | string | None | None | State of the disk for this result.<br>See <a href="vim.vsan.host.DiskResult.State.md">VsanHostDiskResultState</a><br> |
| vsanUuid | string | true | None | VSAN disk UUID in case this disk is a VSAN disk. |
| error | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | Error information for this result: may be populated with additional  information about the disk at hand, regardless of the disk's state.<br>See <a href="vim.fault.VsanDiskFault.md">VsanDiskFault</a><br>See <a href="vim.vsan.host.DiskResult.md#state">state</a><br> |


