vim.host.InternetScsiHba.DigestProperties
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The digest settings for this host bus adapter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| headerDigestType | string | true | None | The header digest preference if header digest is enabled |
| headerDigestInherited | bool | true | None | Header digest setting is inherited |
| dataDigestType | string | true | None | The data digest preference if data digest is enabled |
| dataDigestInherited | bool | true | None | Data digest setting is inherited |


