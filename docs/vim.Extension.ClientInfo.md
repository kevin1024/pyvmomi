vim.Extension.ClientInfo
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object type describes a client of the extension.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| version | string | None | None | Client version number as a dot-separated string. For example, "1.0.0" |
| description | [vim.Description](vim.Description.md "vim.Description") | None | None | Description of client. |
| company | string | None | None | Company information. |
| type | string | None | None | Type of client (examples may include win32, .net, linux, etc.). |
| url | string | None | None | Plugin url. |


