vim.alarm.AlarmTriggeringAction
===============================
inherits from [vim.alarm.AlarmAction](docs/vim.alarm.AlarmAction.md)


This data object type describes one or more   triggering transitions and an action to be done   when an alarm is triggered.   <p>   There are four triggering transitions; at least one of them must   be provided. A gray state is considered the same as a green state,   for the purpose of detecting transitions.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| action | [vim.action.Action](vim.action.Action.md "vim.action.Action") | None | None | The action to be done when the alarm is triggered. |
| transitionSpecs | [vim.alarm.AlarmTriggeringAction.TransitionSpec](vim.alarm.AlarmTriggeringAction.TransitionSpec.md "vim.alarm.AlarmTriggeringAction.TransitionSpec") | true | None | Indicates on which transitions this action executes and repeats.   This is optional only for backwards compatibility. |
| green2yellow | bool | None | None | Flag to specify that the alarm should trigger on a transition   from green to yellow. |
| yellow2red | bool | None | None | Flag to specify that the alarm should trigger on a transition   from yellow to red. |
| red2yellow | bool | None | None | Flag to specify that the alarm should trigger on a transition   from red to yellow. |
| yellow2green | bool | None | None | Flag to specify that the alarm should trigger on a transition   from yellow to green. |


