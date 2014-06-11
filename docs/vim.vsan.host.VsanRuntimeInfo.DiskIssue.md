vim.vsan.host.VsanRuntimeInfo.DiskIssue
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Data structure of reporting a disk issue.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskId | string | None | None | Disk uuid,<br>See <a href="vim.host.ScsiLun.md#uuid">uuid</a><br> |
| issue | string | None | None | Type of issue<br>See DiskIssueType |


