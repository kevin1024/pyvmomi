vim.LicenseManager.LicensableResourceInfo
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Encapsulates information about all licensable resources on the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| resource | [vmodl.KeyAnyValue](vmodl.KeyAnyValue.md "vmodl.KeyAnyValue") | None | None | List of currently supported resources.  The type of every value is long. The key can be one of ResourceKey  or arbitrary string.  <p>NOTE:    The values in this property may not be accurate for pre-5.0 hosts when returned by vCenter 5.0 |


