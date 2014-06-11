vim.host.LicenseSpec
====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| source | [vim.LicenseManager.LicenseSource](vim.LicenseManager.LicenseSource.md "vim.LicenseManager.LicenseSource") | true | None | License source to be used |
| editionKey | string | true | None | License edition to use |
| disabledFeatureKey | string | true | None | Disabled features. When an edition is set, all the features in it  are enabled by default. The following parameter gives a finer   control on which features are disabled. |
| enabledFeatureKey | string | true | None | Enabled features |


