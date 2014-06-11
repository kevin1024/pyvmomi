vim.event.Event
===============
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This event is the base data object type from which all events inherit. All event   objects are data structures that describe events. While event data objects are data   structures that describe events, event data type documentation may describe what the   event records, rather than the data structure, itself.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | int | None | None | The event ID. |
| chainId | int | None | None | The parent or group ID. |
| createdTime | datetime | None | None | The time the event was created. |
| userName | string | None | None | The user who caused the event. |
| datacenter | [vim.event.DatacenterEventArgument](vim.event.DatacenterEventArgument.md "vim.event.DatacenterEventArgument") | true | None | The Datacenter object of the event. |
| computeResource | [vim.event.ComputeResourceEventArgument](vim.event.ComputeResourceEventArgument.md "vim.event.ComputeResourceEventArgument") | true | None | The ComputeResource object of the event. |
| host | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | true | None | The Host object of the event. |
| vm | [vim.event.VmEventArgument](vim.event.VmEventArgument.md "vim.event.VmEventArgument") | true | None | The VirtualMachine object of the event. |
| ds | [vim.event.DatastoreEventArgument](vim.event.DatastoreEventArgument.md "vim.event.DatastoreEventArgument") | true | None | The Datastore object of the event. |
| net | [vim.event.NetworkEventArgument](vim.event.NetworkEventArgument.md "vim.event.NetworkEventArgument") | true | None | The Network object of the event. |
| dvs | [vim.event.DvsEventArgument](vim.event.DvsEventArgument.md "vim.event.DvsEventArgument") | true | None | The DistributedVirtualSwitch object of the event. |
| fullFormattedMessage | string | true | None | A formatted text message describing the event. The message may be localized. |
| changeTag | string | true | None | The user entered tag to identify the operations and their side effects |


