vim.LicenseManager.LicenseUsageInfo
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Contains source information, licensed features, and usage.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| source | [vim.LicenseManager.LicenseSource](vim.LicenseManager.LicenseSource.md "vim.LicenseManager.LicenseSource") | None | None | The source from which licensing data is acquired.<br>See <a href="vim.LicenseManager.LicenseSource.md">LicenseSource</a><br> |
| sourceAvailable | bool | None | None | Returns whether or not the source is currently available.<br>See <a href="vim.LicenseManager.md#sourceAvailable">sourceAvailable</a><br> |
| reservationInfo | [vim.LicenseManager.ReservationInfo](vim.LicenseManager.ReservationInfo.md "vim.LicenseManager.ReservationInfo") | true | None | A list of feature reservations. |
| featureInfo | [vim.LicenseManager.FeatureInfo](vim.LicenseManager.FeatureInfo.md "vim.LicenseManager.FeatureInfo") | true | None | Includes all the features that are referenced in the reservation array. |


