vim.alarm.Alarm
===============
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")


This managed object type defines an alarm that is triggered and    an action that occurs due to the triggered alarm when certain conditions    are met on a specific <a href="vim.ManagedEntity.md">ManagedEntity</a> object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='info'>info</a> | [vim.alarm.AlarmInfo](vim.alarm.AlarmInfo.md "vim.alarm.AlarmInfo") | None | System.View | Information about this alarm. |


RemoveAlarm()
-------------

| service name | RemoveAlarm |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Alarm.Delete |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




ReconfigureAlarm([spec](vim.alarm.AlarmSpec.md "vim.alarm.AlarmSpec"))
----------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | ReconfigureAlarm |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Alarm.Edit |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the alarm name is empty or too long. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if an alarm with the name already exists. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the specification is invalid. |




