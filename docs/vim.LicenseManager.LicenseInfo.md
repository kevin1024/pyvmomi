vim.LicenseManager.LicenseInfo
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Encapsulates information about a license

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| licenseKey | string | None | None | Key for the license. E.g. serial number. |
| editionKey | string | None | None | Edition key. |
| name | string | None | None | Display name for the license |
| total | int | None | None | Total number of units contain in the license |
| used | int | true | None | Number of units used from this license |
| costUnit | string | None | None | The cost unit for this license |
| properties | [vmodl.KeyAnyValue](vmodl.KeyAnyValue.md "vmodl.KeyAnyValue") | true | None | Additional properties associated with this license |
| labels | [vim.KeyValue](vim.KeyValue.md "vim.KeyValue") | true | None | Key-value lables for this license |


