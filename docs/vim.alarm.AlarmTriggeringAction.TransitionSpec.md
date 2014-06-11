vim.alarm.AlarmTriggeringAction.TransitionSpec
==============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Specification indicating which on transitions this action fires.   The existence of a Spec indicates that this action fires on   transitions from that Spec's startState to finalState.   <p>   There are only four acceptable {startState, finalState} pairs:   {green, yellow}, {yellow, red}, {red, yellow} and {yellow, green}.   At least one of these pairs must be specified.   Any deviation from the above will render the enclosing AlarmSpec invalid.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| startState | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | None | None | The state from which the alarm must transition for the action to   fire.  Valid choices are red, yellow and green. |
| finalState | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | None | None | The state to which the alarm must transition for the action to fire.   Valid choices are red, yellow, and green. |
| repeats | bool | None | None | Whether or not the action repeats, as per the actionFrequency defined   in the enclosing Alarm. |


