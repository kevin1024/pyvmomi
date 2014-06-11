vim.host.DigestInfo
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type describes the digest information

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| digestMethod | string | None | None | Method in which the digest value is calculated. The set of possible   values is described in <a href="vim.host.DigestInfo.DigestMethodType.md">HostDigestInfoDigestMethodType</a>. |
| digestValue | int | None | None | The variable length byte array containing the digest value calculated by   the specified digestMethod. |
| objectName | string | true | None | The name of the object from which this digest value is calcaulated. |


