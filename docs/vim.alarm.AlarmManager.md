vim.alarm.AlarmManager
======================


The alarm manager is a singleton object for managing alarms   within a service instance.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='defaultExpression'>defaultExpression</a> | [vim.alarm.AlarmExpression](vim.alarm.AlarmExpression.md "vim.alarm.AlarmExpression") | true | System.View | The default setting for each alarm expression, used to populate the   initial client wizard screen. |
| <a href='description'>description</a> | [vim.alarm.AlarmDescription](vim.alarm.AlarmDescription.md "vim.alarm.AlarmDescription") | None | System.View | The static descriptive strings used in alarms. |


CreateAlarm([entity](vim.ManagedEntity.md "vim.ManagedEntity"), [spec](vim.alarm.AlarmSpec.md "vim.alarm.AlarmSpec"))
---------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | CreateAlarm |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the alarm name is empty or too long. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if an alarm with the name already exists. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the specification is invalid. |




GetAlarm([entity](vim.ManagedEntity.md "vim.ManagedEntity"))
------------------------------------------------------------

| service name | GetAlarm |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




AreAlarmActionsEnabled([entity](vim.ManagedEntity.md "vim.ManagedEntity"))
--------------------------------------------------------------------------

| service name | AreAlarmActionsEnabled |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | None |
| return type | [bool](bool.md "bool") |
### Faults
| fault | description |
|:------|:------------|




EnableAlarmActions([entity](vim.ManagedEntity.md "vim.ManagedEntity"))
----------------------------------------------------------------------

| service name | EnableAlarmActions |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




GetAlarmState([entity](vim.ManagedEntity.md "vim.ManagedEntity"))
-----------------------------------------------------------------
 raises [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound"), [vmodl.fault.InvalidRequest](vmodl.fault.InvalidRequest.md "vmodl.fault.InvalidRequest")

---
| service name | GetAlarmState |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidRequest](vmodl.fault.InvalidRequest.md "vmodl.fault.InvalidRequest") | if the referenced entity is null. |
| [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound") | if the referenced entity is invalid. |




AcknowledgeAlarm([alarm](vim.alarm.Alarm.md "vim.alarm.Alarm"), [entity](vim.ManagedEntity.md "vim.ManagedEntity"))
-------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.InvalidRequest](vmodl.fault.InvalidRequest.md "vmodl.fault.InvalidRequest")

---
| service name | AcknowledgeAlarm |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidRequest](vmodl.fault.InvalidRequest.md "vmodl.fault.InvalidRequest") | if the referenced alarm/entity is null |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the tuple doesn't exist. |
| [vmodl.fault.ManagedObjectNotFound](vmodl.fault.ManagedObjectNotFound.md "vmodl.fault.ManagedObjectNotFound") | if the referenced alarm/entity is invalid. |




