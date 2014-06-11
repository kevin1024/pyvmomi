vmodl.query.PropertyCollector.RetrieveOptions
=============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vmodl.query.version.version3)


Options for <a href="vmodl.query.PropertyCollector.md#retrievePropertiesEx">RetrievePropertiesEx</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| maxObjects | int | true | None | The maximum number of <a href="vmodl.query.PropertyCollector.ObjectContent.md">ObjectContent</a> data   objects that should be returned in a single result from <a href="vmodl.query.PropertyCollector.md#retrievePropertiesEx">RetrievePropertiesEx</a>.    <p> An unset value indicates that there is no maximum. In this   case <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> policy may still limit the number   of objects. Any remaining objects may be retrieved with <a href="vmodl.query.PropertyCollector.md#continueRetrievePropertiesEx">ContinueRetrievePropertiesEx</a>.    <p> A positive value causes <a href="vmodl.query.PropertyCollector.md#retrievePropertiesEx">RetrievePropertiesEx</a> to   suspend the retrieval when the count of objects reaches the   specified maximum. <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> policy may still   limit the count to something less than <a href="vmodl.query.PropertyCollector.RetrieveOptions.md#maxObjects">maxObjects</a>. Any remaining   objects may be retrieved with <a href="vmodl.query.PropertyCollector.md#continueRetrievePropertiesEx">ContinueRetrievePropertiesEx</a>.    <p> A value less than or equal to 0 is illegal. |


