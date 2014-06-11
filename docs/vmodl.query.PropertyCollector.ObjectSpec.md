vmodl.query.PropertyCollector.ObjectSpec
========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Within a <a href="vmodl.query.PropertyCollector.FilterSpec.md">PropertyFilterSpec</a>, the <a href="vmodl.query.PropertyCollector.ObjectSpec.md">ObjectSpec</a> data object type specifies the managed   object at which the filter begins to collect the managed object   references and properties specified by the associated <a href="vmodl.query.PropertyCollector.PropertySpec.md">PropertySpec</a> set. If the "skip" property is present   and set to true, then the filter does not check to see if the starting   object's type matches any of the types listed in the associated sets of   <a href="vmodl.query.PropertyCollector.PropertySpec.md">PropertySpec</a> data objects.    <p> If the <a href="vmodl.query.PropertyCollector.ObjectSpec.md#selectSet">selectSet</a> property is   present, then this specifies additional objects to filter.  These objects   are defined by one or more <a href="vmodl.query.PropertyCollector.SelectionSpec.md">SelectionSpec</a>   objects.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| obj | vim.ExtensibleManagedObject | None | System.View | Starting object. |
| skip | bool | true | None | Flag to specify whether or not to report this managed object's   properties.  If the flag is true, the filter will not report this   managed object's properties. |
| selectSet | [vmodl.query.PropertyCollector.SelectionSpec](vmodl.query.PropertyCollector.SelectionSpec.md "vmodl.query.PropertyCollector.SelectionSpec") | true | None | Set of selections to specify additional objects to filter. |


