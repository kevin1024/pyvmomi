vim.vsan.host.ClusterStatus.State.CompletionEstimate
====================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Estimated completion status for transitory node states.<br>See <a href="vim.vsan.host.NodeState.md">VsanHostNodeState</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| completeTime | datetime | true | None | Estimated time of completion. |
| percentComplete | int | true | None | Estimated percent of completion as a value in the range [0, 100]. |


