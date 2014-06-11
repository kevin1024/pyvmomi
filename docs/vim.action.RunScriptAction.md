vim.action.RunScriptAction
==========================
inherits from [vim.action.Action](docs/vim.action.Action.md)


This data object type specifies a script that is triggered by an alarm.    You can use any elements of the    <a href="vim.action.Action.ActionParameter.md">ActionParameter</a> enumerated list    as part of your script to provide information available at runtime.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| script | string | None | None | The fully-qualified path to a shell script that runs on the    VirtualCenter server as a result of an alarm. |


