vim.host.InternetScsiHba.DigestCapabilities
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The digest capabilities for this host bus adapter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| headerDigestSettable | bool | true | None | True if this host bus adapter supports the configuration  of the use of header digest. Defaults to false, in which  case no header digests will be used. |
| dataDigestSettable | bool | true | None | True if this host bus adapter supports the configuration  of the use of data digest. Defaults to false, in which  case no data digests will be used. |
| targetHeaderDigestSettable | bool | true | None | True if configuration of the use of header digest is supported  on the targets associated with the host bus adapter. Defaults to  false, in which case no header digests will be used. |
| targetDataDigestSettable | bool | true | None | True if configuration of the use of data digest is supported  on the targets associated with the host bus adapter. Defaults to  false, in which case no data digests will be used. |


