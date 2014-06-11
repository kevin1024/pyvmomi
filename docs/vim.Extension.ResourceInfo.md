vim.Extension.ResourceInfo
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object encapsulates the message resources for all locales.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| locale | string | None | None |  |
| module | string | None | None | Module for a resource type and other message or fault resources.  Examples: "task" for task, "event" for event and "auth" for "privilege". |
| data | [vim.KeyValue](vim.KeyValue.md "vim.KeyValue") | None | None |  |


