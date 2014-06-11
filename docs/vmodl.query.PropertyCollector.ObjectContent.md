vmodl.query.PropertyCollector.ObjectContent
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vmodl.query.PropertyCollector.ObjectContent.md">ObjectContent</a> data object type contains the   contents retrieved for a single managed object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| obj | vim.ExtensibleManagedObject | None | None | Reference to the managed object that contains properties of interest. |
| propSet | [vmodl.DynamicProperty](vmodl.DynamicProperty.md "vmodl.DynamicProperty") | true | None | Set of name-value pairs for the properties of the managed object. |
| missingSet | [vmodl.query.PropertyCollector.MissingProperty](vmodl.query.PropertyCollector.MissingProperty.md "vmodl.query.PropertyCollector.MissingProperty") | true | None | Properties for which values could not be retrieved and the associated  fault. |


