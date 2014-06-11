vmodl.query.PropertyCollector.FilterUpdate
==========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vmodl.query.PropertyCollector.FilterUpdate.md">PropertyFilterUpdate</a> data object type contains a   list of updates to data visible through a specific filter. Note that if a   property changes through multiple filters, then a client receives an   update for each filter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| filter | [vmodl.query.PropertyCollector.Filter](vmodl.query.PropertyCollector.Filter.md "vmodl.query.PropertyCollector.Filter") | None | None | Filter that was updated. |
| objectSet | [vmodl.query.PropertyCollector.ObjectUpdate](vmodl.query.PropertyCollector.ObjectUpdate.md "vmodl.query.PropertyCollector.ObjectUpdate") | true | None | Set of changes to object properties in the filter. |
| missingSet | [vmodl.query.PropertyCollector.MissingObject](vmodl.query.PropertyCollector.MissingObject.md "vmodl.query.PropertyCollector.MissingObject") | true | None | Objects that could not be found on the server, but were specified in a   <a href="vmodl.query.PropertyCollector.FilterSpec.md#objectSet">objectSet</a>.    <p> This field will only be populated for objects that were determined   to be missing since the data version passed to <a href="vmodl.query.PropertyCollector.md#checkForUpdates">CheckForUpdates</a>, <a href="vmodl.query.PropertyCollector.md#waitForUpdates">WaitForUpdates</a>, or <a href="vmodl.query.PropertyCollector.md#waitForUpdatesEx">WaitForUpdatesEx</a> and will not contain objects that were missing   prior to that data version. |


