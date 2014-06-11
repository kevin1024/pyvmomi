vim.event.EventManager
======================


This managed object type provides properties and methods for   event management support.   Event objects are used to record significant state changes of   managed entities.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='description'>description</a> | [vim.event.EventDescription](vim.event.EventDescription.md "vim.event.EventDescription") | None | System.View | Static descriptive strings used in events. |
| <a href='latestEvent'>latestEvent</a> | [vim.event.Event](vim.event.Event.md "vim.event.Event") | true | System.View | The latest event that happened on the VirtualCenter server. |
| <a href='maxCollector'>maxCollector</a> | int | None | System.View | For each client, the maximum number of event collectors that can exist   simultaneously. |


RetrieveArgumentDescription([eventTypeId](#string "string"))
------------------------------------------------------------

| service name | RetrieveArgumentDescription |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




CreateCollectorForEvents([filter](vim.event.EventFilterSpec.md "vim.event.EventFilterSpec"))
--------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | CreateCollectorForEvents |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if there are more than the maximum number of                        event collectors. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the filter is null or if any of its fields                           is invalid, such as an invalid reference to a                           managed object, alarm, or scheduled task, or an                           invalid event type or event chain id, etc. |




LogUserEvent([entity](vim.ManagedEntity.md "vim.ManagedEntity"), [msg](#string "string"))
-----------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | LogUserEvent |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the entity is of a wrong type or the "msg" string is                           empty. |




QueryEvents([filter](vim.event.EventFilterSpec.md "vim.event.EventFilterSpec"))
-------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryEvents |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the filter is null or if any of its fields                          is invalid, such as an invalid reference to a                          managed object, alarm, or scheduled task, or an                          invalid event type or event chain id, etc. |




PostEvent([eventToPost](vim.event.Event.md "vim.event.Event"), [taskInfo](vim.TaskInfo.md "vim.TaskInfo"))
----------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidEvent](vim.fault.InvalidEvent.md "vim.fault.InvalidEvent"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | PostEvent |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Global.LogEvent |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidEvent](vim.fault.InvalidEvent.md "vim.fault.InvalidEvent") | no longer thrown by this API |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if  <ul>  <li>an invalid reference to a managed object is passed in to one of the  <a href="vim.event.EntityEventArgument.md">EntityEventArgument</a> fields  <li>an invalid severity value is passed in an <a href="vim.event.EventEx.md">EventEx</a>.  </ul> |




