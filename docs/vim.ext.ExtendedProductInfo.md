vim.ext.ExtendedProductInfo
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This data object encapsulates extended product information for an extension.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| companyUrl | string | true | None | URL to extension vendor. |
| productUrl | string | true | None | URL to vendor's description of this extension. |
| managementUrl | string | true | None | URL to management UI for this extension. |
| self | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | The VirtualMachine or VirtualApp that is running this extension. |


