vim.Extension.ServerInfo
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object type describes a server for the extension.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| url | string | None | None | Server url. |
| description | [vim.Description](vim.Description.md "vim.Description") | None | None | Server description. |
| company | string | None | None | Company information. |
| type | string | None | None | Type of server (examples may include SOAP, REST, HTTP, etc.). |
| adminEmail | string | None | None | Extension administrator email addresses. |
| serverThumbprint | string | true | None | Thumbprint of the extension server certificate presented to clients |


