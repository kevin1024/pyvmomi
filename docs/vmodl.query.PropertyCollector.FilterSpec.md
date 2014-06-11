vmodl.query.PropertyCollector.FilterSpec
========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Specify the property data that is included in a filter. A filter can   specify part of a single managed object, or parts of multiple related   managed objects in an inventory hierarchy - for example, to collect   updates from all virtual machines in a given folder.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| propSet | [vmodl.query.PropertyCollector.PropertySpec](vmodl.query.PropertyCollector.PropertySpec.md "vmodl.query.PropertyCollector.PropertySpec") | None | None | Set of properties to include in the filter, specified for each object   type. |
| objectSet | [vmodl.query.PropertyCollector.ObjectSpec](vmodl.query.PropertyCollector.ObjectSpec.md "vmodl.query.PropertyCollector.ObjectSpec") | None | None | Set of specifications that determine the objects to filter. |
| reportMissingObjectsInResults | bool | true | None | Control how to report missing objects during filter creation.    <p> If false or unset and <a href="vmodl.query.PropertyCollector.FilterSpec.md#objectSet">objectSet</a> refers to missing objects,   filter creation will fail with a <a href="vmodl.fault.ManagedObjectNotFound.md">ManagedObjectNotFound</a> fault.    <p> If true and <a href="vmodl.query.PropertyCollector.FilterSpec.md#objectSet">objectSet</a> refers   to missing objects, filter creation will not fail and missing objects   will be reported via filter results. This is the recommended setting   when <a href="vmodl.query.PropertyCollector.FilterSpec.md#objectSet">objectSet</a> refers to   transient objects.    <p> In an <a href="vmodl.query.PropertyCollector.UpdateSet.md">UpdateSet</a> missing objects will   appear in the <a href="vmodl.query.PropertyCollector.FilterUpdate.md#missingSet">missingSet</a> field.    <p> In a <a href="vmodl.query.PropertyCollector.RetrieveResult.md">RetrieveResult</a> missing objects will   simply be omitted from the objects field.    <p> For a call to <a href="vmodl.query.PropertyCollector.md#retrieveContents">RetrieveProperties</a> missing objects will simply   be omitted from the results. |


