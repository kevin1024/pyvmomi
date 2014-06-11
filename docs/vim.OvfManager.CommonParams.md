vim.OvfManager.CommonParams
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A common super-class for basic OVF descriptor parameters

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| locale | string | None | None | The locale-identifier to choose from the descriptor. If empty, the   default locale on the server is used. |
| deploymentOption | string | None | None | The key of the chosen deployment option. If empty, the default option is  chosen. The list of possible deployment options is returned in the result of  parseDescriptor. |
| msgBundle | [vim.KeyValue](vim.KeyValue.md "vim.KeyValue") | true | None | An optional set of localization strings to be used. The server will use   these message strings to localize information in the result and in    error and warning messages.   <p>   This argument allows a client to pass messages from external    string bundles. The client is responsible for selecting the right string   bundle (based on locale) and parsing the external string bundle. The   passed in key/value pairs are looked up before any messages   included in the OVF descriptor itself. |
| importOption | string | true | None | An optional argument for modifing the OVF parsing. When the server parses an OVF  descriptor a set of options can be used to modify the parsing. The argument is a list  of keywords.  <p>  To get a list of supported keywords see <a href="vim.OvfManager.md#ovfImportOption">ovfImportOption</a>. Unknown  options will be ignored by the server. |


