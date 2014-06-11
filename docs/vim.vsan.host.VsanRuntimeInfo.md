vim.vsan.host.VsanRuntimeInfo
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This data object contains VSAN cluster runtime information from   the perspective of the host in question.   This data object is used to represent read-only state whose values   may change during operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| membershipList | [vim.vsan.host.MembershipInfo](vim.vsan.host.MembershipInfo.md "vim.vsan.host.MembershipInfo") | true | None | This property reports host membership information. |
| diskIssues | [vim.vsan.host.VsanRuntimeInfo.DiskIssue](vim.vsan.host.VsanRuntimeInfo.DiskIssue.md "vim.vsan.host.VsanRuntimeInfo.DiskIssue") | true | None | List of disk issues detected on this host.   <p>   To retrieve more information on the issues, use   <a href="vim.host.VsanSystem.md#queryDisksForVsan">QueryDisksForVsan</a>. |
| accessGenNo | int | true | None | Generation number tracking object accessibility. |


