vim.dvs.KeyedOpaqueBlob
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This class defines a data structure to hold opaque binary data   identified by a key.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | A key that identifies the opaque binary blob. |
| opaqueData | string | None | None | The opaque data. It is recommended that base64 encoding be used for binary   data. |


