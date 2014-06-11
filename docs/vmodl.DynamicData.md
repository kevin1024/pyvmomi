vmodl.DynamicData
=================


DynamicData is a builtin object model data object type for manipulating data  properties dynamically. The primary usage is as a base class for types that may  be extended with subtypes in the future, where new properties should be sent to  old clients as a set of dynamic properties.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dynamicType | string | true | None | Reserved. |
| dynamicProperty | [vmodl.DynamicProperty](vmodl.DynamicProperty.md "vmodl.DynamicProperty") | true | None | Set of dynamic properties. This property is optional because only the  properties of an object that are unknown to a client will be part of this set.  This property is not readonly just in case we want to send such properties  from a client in the future. |


