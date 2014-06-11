vmodl.query.PropertyCollector.MissingObject
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Used for reporting missing objects that were explicitly referenced by a   filter spec. In other words, any of the objects referenced in <a href="vmodl.query.PropertyCollector.FilterSpec.md#objectSet">objectSet</a>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| obj | vim.ExtensibleManagedObject | None | None | The object that is being reported missing |
| fault | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | Fault describing the failure to lookup this object    <p> The possible faults for missing objects are: <ul>    <li> <a href="vmodl.fault.SystemError.md">SystemError</a> if there was some unknown problem        looking up the object    <li> <a href="vmodl.fault.ManagedObjectNotFound.md">ManagedObjectNotFound</a> if the object is no        longer available    </ul> |


