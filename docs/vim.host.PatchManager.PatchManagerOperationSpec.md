vim.host.PatchManager.PatchManagerOperationSpec
===============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Optional parameters for hostd to pass to exupdate.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| proxy | string | true | None | The name of the possible proxy for esxupdate to use to connect to a server.   The patch and metadata may be cached within the proxy server. |
| port | int | true | None | The port of the possible proxy for esxupdate to use to connect to a server.   The patch and metadata may be cached within the proxy server. |
| userName | string | true | None | The user name used for the proxy server. |
| password | string | true | None | The password used for the proxy server. This is passed with ssl through a  trusted channel. |
| cmdOption | string | true | None | Possible command line options when calling esxupdate. |


