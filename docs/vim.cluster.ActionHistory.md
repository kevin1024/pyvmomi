vim.cluster.ActionHistory
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Base class for all action history.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| action | [vim.cluster.Action](vim.cluster.Action.md "vim.cluster.Action") | None | None | The action that was executed recently. |
| time | datetime | None | None | The time when the action was executed. |


