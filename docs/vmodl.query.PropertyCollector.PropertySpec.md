vmodl.query.PropertyCollector.PropertySpec
==========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Within a <a href="vmodl.query.PropertyCollector.FilterSpec.md">PropertyFilterSpec</a>, A <a href="vmodl.query.PropertyCollector.PropertySpec.md">PropertySpec</a> specifies which properties should be   reported to the client for objects of the given managed object type that   are visited and not skipped.  One more subtle side effect is that if a   managed object is visited and not skipped, but there is no <a href="vmodl.query.PropertyCollector.PropertySpec.md">PropertySpec</a> associated with the managed object's   type, the managed object will not be reported to the client.    <p> Also, the set of properties applicable to a given managed object type   is the union of the properties implied by the <a href="vmodl.query.PropertyCollector.PropertySpec.md">PropertySpec</a> objects even, in the case of a <a href="vmodl.query.PropertyCollector.RetrieveResult.md">RetrieveResult</a>, where there may be an applicable   <a href="vmodl.query.PropertyCollector.PropertySpec.md">PropertySpec</a> in more than one filter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| type | string | None | None | Name of the managed object type being collected. |
| all | bool | true | None | Specifies whether or not all properties of the object are read. If   this property is set to true, the <a href="vmodl.query.PropertyCollector.PropertySpec.md#pathSet">pathSet</a> property is ignored. |
| pathSet | string | true | None | Specifies which managed object properties are retrieved. If the <a href="vmodl.query.PropertyCollector.PropertySpec.md#pathSet">pathSet</a> is empty, then the   <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> retrieves references to the managed objects   and no managed object properties are collected. |


