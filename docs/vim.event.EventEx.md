vim.event.EventEx
=================
inherits from [vim.event.Event](docs/vim.event.Event.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


EventEx is a dynamically typed Event class, whose type is indicated by its  eventTypeId property.  <p>  A collection of eventTypeIds is registered by Extensions, which can now  pass in optional type information for each eventTypeId which indicates the  applicable argument names and types, among other properties.  <p>  EventEx allows event arguments of any type, though today, the system  only supports "string" and "moid" (a string which can be interpreted as an  object ID in the system) as argument types.  In the future, the system  may optionally strongly check the types of the arguments in the event  against the declared type information, based on how the event type is  declared.  <p>  EventEx also allows arbitrary "event object"s - the object which the  event refers to. You can put in any object identifier as the objectId,  but objectType should be filled in only if the object is actually present  in the VC Server's ManagedEntity inventory.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| eventTypeId | string | None | None | The type of the event. |
| severity | string | true | None | The severity level of the message: null=>info.<br>See <a href="vim.event.Event.EventSeverity.md">EventEventSeverity</a><br> |
| message | string | true | None | An arbitrary message string, not localized. |
| arguments | [vmodl.KeyAnyValue](vmodl.KeyAnyValue.md "vmodl.KeyAnyValue") | true | None | The event arguments associated with the event |
| objectId | string | true | None | The ID of the object (VM, Host, Folder..) which the event pertains to.  Federated or local inventory path. |
| objectType | string | true | None | the type of the object, if known to the VirtualCenter inventory |
| objectName | string | true | None | The name of the object |
| fault | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | The fault that triggered the event, if any |


