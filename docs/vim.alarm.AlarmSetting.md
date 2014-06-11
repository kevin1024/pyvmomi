vim.alarm.AlarmSetting
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Tolerance and frequency limits of an alarm.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| toleranceRange | int | None | None | Tolerance range for the metric triggers, measured in one hundredth percentage.    <p>    A zero value means that the alarm    triggers whenever the metric value is above    or below the specified value.    A nonzero value means that the alarm    triggers only after reaching a certain percentage    above or below the nominal trigger value. |
| reportingFrequency | int | None | None | How often the alarm is triggered, measured in seconds.    <p>    A zero value means that the alarm is allowed    to trigger as often as possible.    A nonzero value means that any subsequent triggers    are suppressed for a period of seconds following a    reported trigger. |


