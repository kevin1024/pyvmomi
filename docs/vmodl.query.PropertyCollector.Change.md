vmodl.query.PropertyCollector.Change
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Describes a change to a property.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | Property or nested property to which the change applies.  Nested   properties are specified by paths; for example,    <ul>   <li>foo.bar   <li>foo.arProp["key val"]   <li>foo.arProp["key val"].baz   </ul> |
| op | [vmodl.query.PropertyCollector.Change.Op](vmodl.query.PropertyCollector.Change.Op.md "vmodl.query.PropertyCollector.Change.Op") | None | None | Change operation for the property. Valid values are:   <table>   <dt>add</dt>   <dd>The property is a collection and the change inserts an element       into the collection.</dd>   <dt>remove</dt>   <dd>The property is a collection and the change deletes an element       from the collection.</dd>   <dt>assign</dt>   <dd>The change is a new value for the property.</dd>   <dt>indirectRemove</dt>   <dd>The property was removed because a containing property was removed       or unset</dd>   </table> |
| val | object | true | None | New value for the property when "op" is either "add" or "assign". |


