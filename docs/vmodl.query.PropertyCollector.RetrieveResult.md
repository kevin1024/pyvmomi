vmodl.query.PropertyCollector.RetrieveResult
============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vmodl.query.version.version3)


Result of <a href="vmodl.query.PropertyCollector.md#retrievePropertiesEx">RetrievePropertiesEx</a> and <a href="vmodl.query.PropertyCollector.md#continueRetrievePropertiesEx">ContinueRetrievePropertiesEx</a>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| token | string | true | None | A token used to retrieve further retrieve results.    <p> If set, the token should be passed to <a href="vmodl.query.PropertyCollector.md#continueRetrievePropertiesEx">ContinueRetrievePropertiesEx</a> to retrieve more results. Each token   may be passed to continueRetrievePropertiesEx only once, and only in   the same session in which it was returned and to the same   <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> object that returned it.    <p> If unset, there are no further results to retrieve after this   <a href="vmodl.query.PropertyCollector.RetrieveResult.md">RetrieveResult</a>. |
| objects | [vmodl.query.PropertyCollector.ObjectContent](vmodl.query.PropertyCollector.ObjectContent.md "vmodl.query.PropertyCollector.ObjectContent") | None | None | retrieved objects. |


