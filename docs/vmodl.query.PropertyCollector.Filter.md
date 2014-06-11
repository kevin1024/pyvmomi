vmodl.query.PropertyCollector.Filter
====================================


The <a href="vmodl.query.PropertyCollector.Filter.md">PropertyFilter</a> managed object type defines a filter   that controls the properties for which a <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> detects   incremental changes.  Filters are subordinate objects; they are part of the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> and do not have independent lifetimes.  A Filter   is automatically destroyed when the session on which it was created is   closed or the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> on which it was created is   destroyed.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='spec'>spec</a> | [vmodl.query.PropertyCollector.FilterSpec](vmodl.query.PropertyCollector.FilterSpec.md "vmodl.query.PropertyCollector.FilterSpec") | None | None | Specifications for this filter. |
| <a href='partialUpdates'>partialUpdates</a> | bool | None | None | Flag to indicate if a change to a nested property reports only the   nested change or the entire specified property value.  If the value is   true, a change reports only the nested property.  If the value is   false, a change reports the enclosing property named in the filter. |


DestroyPropertyFilter()
-----------------------

| service name | DestroyPropertyFilter |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




