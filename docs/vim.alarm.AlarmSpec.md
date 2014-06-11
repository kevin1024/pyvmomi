vim.alarm.AlarmSpec
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Parameters for alarm creation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | Name of the alarm. |
| systemName | string | true | None | System name of the alarm.  <p>  This is set only for predefined Alarms - i.e. Alarms created by the  server automatically. Editing or renaming Alarms from the UI does  not affect this value, and user-created Alarms do not have a  systemName at all.  <p>  The purpose of this field is to identify system-created Alarms  reliably, even if they are edited by users. |
| description | string | None | None | Description of the alarm. |
| enabled | bool | None | None | Flag to indicate whether or not the alarm is enabled or disabled. |
| expression | [vim.alarm.AlarmExpression](vim.alarm.AlarmExpression.md "vim.alarm.AlarmExpression") | None | None | Top-level alarm expression that defines trigger conditions. |
| action | [vim.alarm.AlarmAction](vim.alarm.AlarmAction.md "vim.alarm.AlarmAction") | true | None | Action to perform when the alarm is triggered. |
| actionFrequency | int | true | None | Frequency in seconds, which specifies how often appropriate actions  should repeat when an alarm does not change state. |
| setting | [vim.alarm.AlarmSetting](vim.alarm.AlarmSetting.md "vim.alarm.AlarmSetting") | true | None | Tolerance and maximum frequency settings. |


