vmodl.query.PropertyCollector.TraversalSpec
===========================================
inherits from [vmodl.query.PropertyCollector.SelectionSpec](docs/vmodl.query.PropertyCollector.SelectionSpec.md)


The <a href="vmodl.query.PropertyCollector.TraversalSpec.md">TraversalSpec</a> data object type specifies   how to derive a new set of objects to add to the filter.    <p> It specifies a property path whose value is either another managed   object or an array of managed objects included in the set of objects for   consideration.  This data object can also be named, using the "name"   field in the base type.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| type | string | None | None | Name of the object type containing the property. |
| path | string | None | None | Name of the property to use in order to select additional objects. |
| skip | bool | true | None | Flag to indicate whether or not to filter the object in the "path"  field. |
| selectSet | [vmodl.query.PropertyCollector.SelectionSpec](vmodl.query.PropertyCollector.SelectionSpec.md "vmodl.query.PropertyCollector.SelectionSpec") | true | None | Optional set of selections to specify additional objects to filter. |


