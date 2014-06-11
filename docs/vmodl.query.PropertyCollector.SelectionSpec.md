vmodl.query.PropertyCollector.SelectionSpec
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vmodl.query.PropertyCollector.SelectionSpec.md">SelectionSpec</a> is the base type for data   object types that specify what additional objects to filter. The base   type contains only an optional "name" field, which allows a selection to   be named for future reference. More information is available in the   subtype.    <p> Named selections support recursive specifications on an object   hierarchy.  When used by a derived object, the "name" field allows other   <a href="vmodl.query.PropertyCollector.SelectionSpec.md">SelectionSpec</a> objects to refer to the object by   name. When used as the base type only, the "name" field indicates   recursion to the derived object by name.    <p> Names are meaningful only within the same FilterSpec.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | true | None | Name of the selection specification. |


