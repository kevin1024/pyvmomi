vim.LicenseManager.AvailabilityInfo
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Describes how many licenses of a particular feature is provided by the licensing   source.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| feature | [vim.LicenseManager.FeatureInfo](vim.LicenseManager.FeatureInfo.md "vim.LicenseManager.FeatureInfo") | None | None | Describes the feature. |
| total | int | None | None | Total number of licenses for this given type that are installed on the source. |
| available | int | None | None | The number of licenses that have not yet been reserved on the source. |


