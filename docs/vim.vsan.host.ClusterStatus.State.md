vim.vsan.host.ClusterStatus.State
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Data object representing the VSAN node state for a host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| state | string | None | None | VSAN node state for this host.<br>See <a href="vim.vsan.host.NodeState.md">VsanHostNodeState</a><br> |
| completion | [vim.vsan.host.ClusterStatus.State.CompletionEstimate](vim.vsan.host.ClusterStatus.State.CompletionEstimate.md "vim.vsan.host.ClusterStatus.State.CompletionEstimate") | true | None | An estimation of the completion of a node state transition; this  value may be populated for transitory node states.<br>See <a href="vim.vsan.host.NodeState.md">VsanHostNodeState</a><br> |


