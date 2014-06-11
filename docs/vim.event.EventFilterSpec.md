vim.event.EventFilterSpec
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Event filter used to query events in the history collector database.   The client creates an event history collector with a filter specification,   then retrieves the events from the event history collector.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.event.EventFilterSpec.ByEntity](vim.event.EventFilterSpec.ByEntity.md "vim.event.EventFilterSpec.ByEntity") | true | None | The filter specification for retrieving events by managed entity.   If the property is not set, then events attached to all managed entities   are collected. |
| time | [vim.event.EventFilterSpec.ByTime](vim.event.EventFilterSpec.ByTime.md "vim.event.EventFilterSpec.ByTime") | true | None | The filter specification for retrieving tasks by time.   If the property is not set, then events with any time stamp are collected. |
| userName | [vim.event.EventFilterSpec.ByUsername](vim.event.EventFilterSpec.ByUsername.md "vim.event.EventFilterSpec.ByUsername") | true | None | The filter specification for retrieving events by username.   If the property is not set, then events belonging to any user are collected. |
| eventChainId | int | true | None | The filter specification for retrieving events by chain ID.   If the property is not set, events with any chain ID are collected. |
| alarm | [vim.alarm.Alarm](vim.alarm.Alarm.md "vim.alarm.Alarm") | true | None | This property, if set, limits the set of collected events to those   associated with the specified alarm.   If the property is not set, events are collected regardless of their   association with alarms. |
| scheduledTask | [vim.scheduler.ScheduledTask](vim.scheduler.ScheduledTask.md "vim.scheduler.ScheduledTask") | true | None | This property, if set, limits the set of collected events to those   associated with the specified scheduled task.   If the property is not set, events are collected regardless of their   association with any scheduled task. |
| disableFullMessage | bool | true | None | Flag to specify whether or not to prepare the full formatted message   for each event.   If the property is not set, the collected events do not include   the full formatted message. |
| category | string | true | None | This property, if set, limits the set of collected events to those   associated with the specified category.   If the property is not set, events are collected regardless of their   association with any category.     "category" here is the same as Event.severity. |
| type | string | true | None | This property, if set, limits the set of collected events to those  specified types.  If the property is not set, events are collected regardless of their  types. |
| tag | string | true | None | This property, if set, limits the set of filtered events to those that  have it. If not set, or the size of it 0, the tag of an event is  disregarded. A blank string indicates events without tags. |
| eventTypeId | string | true | None | This property, if set, limits the set of collected events to those  specified types.  <p>  Note: if both <a href="vim.event.EventFilterSpec.md#eventTypeId">eventTypeId</a> and <a href="vim.event.EventFilterSpec.md#type">type</a> are specified, an  exception may be thrown by <a href="vim.event.EventManager.md#createCollector">CreateCollectorForEvents</a>.  <p>  The semantics of how eventTypeId matching is done is as follows:  <ul>  <li>If the event being collected is of type <a href="vim.event.EventEx.md">EventEx</a>  or <a href="vim.event.ExtendedEvent.md">ExtendedEvent</a>, then we match against the  <code>eventTypeId</code> (for <code>EventEx</code>) or  <code>eventId</code> (for <code>ExtendedEvent</code>) member of the Event.  <li>Otherwise, we match against the type of the Event itself.  </ul>    If neither this property, nor <code>type</code>, is set, events are  collected regardless of their types. |


