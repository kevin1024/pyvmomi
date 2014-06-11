vim.LicenseManager.FeatureInfo
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


A single feature that can be licensed. This information is immutable.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Unique identifier for license as defined in License source data.   Max length of this string is 64 characters of ASCII/ISO Latin-1   character set. |
| featureName | string | None | None | The display string for the feature name. |
| featureDescription | string | true | None | A human readable description of what function this feature enables. |
| state | [vim.LicenseManager.FeatureInfo.State](vim.LicenseManager.FeatureInfo.State.md "vim.LicenseManager.FeatureInfo.State") | true | None | Describes the state of the feature based on the current edition license. This   property is unset for an edition license. |
| costUnit | string | None | None | Each license has a cost associated with it and the value of costUnit   specifies the applicable unit.   <p><br>See <a href="vim.LicenseManager.FeatureInfo.CostUnit.md">LicenseFeatureInfoUnit</a><br> |
| sourceRestriction | string | true | None | Describe any restriction on the source of a license for this feature.   <p><br>See <a href="vim.LicenseManager.FeatureInfo.SourceRestriction.md">LicenseFeatureInfoSourceRestriction</a><br> |
| dependentKey | string | true | None | Report List of feature keys used by this edition. |
| edition | bool | true | None | Flag to indicate whether the feature is an edition. |
| expiresOn | datetime | true | None | Date representing the expiration date |


