vmodl.query.PropertyCollector.MissingProperty
=============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Used for reporting properties for which values could not be retrieved.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| path | string | None | None | Property for which a value could not be retrieved |
| fault | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | None | None | Fault describing the failure to retrieve the property value.    <p> The possible faults for missing properties are: <ul>    <li> <a href="vmodl.fault.SystemError.md">SystemError</a> if there was some unknown problem        reading the value    <li> <a href="vmodl.fault.SecurityError.md">SecurityError</a> if the logged in session did        not have permission to read the value    </ul> |


