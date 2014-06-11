vim.alarm.EventAlarmExpression
==============================
inherits from [vim.alarm.AlarmExpression](docs/vim.alarm.AlarmExpression.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


An alarm expression that uses the event stream to trigger the alarm.   <p>   This alarm is triggered when an event matching this expression gets logged.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| comparisons | [vim.alarm.EventAlarmExpression.Comparison](vim.alarm.EventAlarmExpression.Comparison.md "vim.alarm.EventAlarmExpression.Comparison") | true | None | The attributes/values to compare. |
| eventType | string | None | None | The type of the event to trigger the alarm on. |
| eventTypeId | string | true | None | The eventTypeId of the event to match.  <p>  The semantics of how eventTypeId matching is done is as follows:  <ul>  <li>If the event being matched is of type <a href="vim.event.EventEx.md">EventEx</a>  or <a href="vim.event.ExtendedEvent.md">ExtendedEvent</a>, then we match this value  against the <code>eventTypeId</code> (for <code>EventEx</code>) or  <code>eventId</code> (for <code>ExtendedEvent</code>) member of the Event.  <li>Otherwise, we match it against the type of the Event itself.  </ul>  <p>  Either <code>eventType</code> or <code>eventTypeId</code> <i>must</i>  be set. |
| objectType | string | true | None | Name of the type of managed object on which the event is logged.  <p>  An event alarm defined on a <a href="vim.ManagedEntity.md">ManagedEntity</a>  is propagated to child entities in the VirtualCenter inventory depending  on the value of this attribute. If objectType is any of the following,  the alarm is propagated down to all children of that type:  <ul>  <li> A datacenter: <a href="vim.Datacenter.md">Datacenter</a>.  <li> A cluster of host systems: <a href="vim.ClusterComputeResource.md">ClusterComputeResource</a>.  <li> A single host system: <a href="vim.HostSystem.md">HostSystem</a>.  <li> A resource pool representing a set of physical resources on a single host:  <a href="vim.ResourcePool.md">ResourcePool</a>.  <li> A virtual machine: <a href="vim.VirtualMachine.md">VirtualMachine</a>.  <li> A datastore: <a href="vim.Datastore.md">Datastore</a>.  <li> A network: <a href="vim.Network.md">Network</a>.  <li> A distributed virtual switch:  <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.  </ul>  <p>  If objectType is unspecified or not contained in the above list,   the event alarm is not propagated down to child entities in the   VirtualCenter inventory.  <p>  It is possible to specify an event alarm containing two (or more) different   EventAlarmExpression's which contain different objectTypes. In such a case,  the event is propagated to all child entities with specified type(s). |
| status | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | true | None | The alarm's new state when this condition is evaluated and satisfied.  If not specified then there is no change to alarm status, and all  actions are fired (rather than those for the transition). |


