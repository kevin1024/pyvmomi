vmodl.query.PropertyCollector.ObjectUpdate
==========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vmodl.query.PropertyCollector.ObjectUpdate.md">ObjectUpdate</a> data object type contains   information about changes to a particular managed object. We distinguish   updates when an object is created, destroyed, or modified, as well as   when the object enters or leaves the set of objects dynamically   associated with a filter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| kind | [vmodl.query.PropertyCollector.ObjectUpdate.Kind](vmodl.query.PropertyCollector.ObjectUpdate.Kind.md "vmodl.query.PropertyCollector.ObjectUpdate.Kind") | None | None | Kind of update that caused the filter to report a change. |
| obj | vim.ExtensibleManagedObject | None | None | Reference to the managed object to which this update applies. |
| changeSet | [vmodl.query.PropertyCollector.Change](vmodl.query.PropertyCollector.Change.md "vmodl.query.PropertyCollector.Change") | true | None | Optional set of changes to the object.  Present only if the "kind" is   either "modify" or "enter". |
| missingSet | [vmodl.query.PropertyCollector.MissingProperty](vmodl.query.PropertyCollector.MissingProperty.md "vmodl.query.PropertyCollector.MissingProperty") | true | None | Properties whose value could not be retrieved and their associated   faults.  Present only if the "kind" is either "modify" or "enter". |


