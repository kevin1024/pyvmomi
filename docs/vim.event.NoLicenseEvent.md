vim.event.NoLicenseEvent
========================
inherits from [vim.event.LicenseEvent](docs/vim.event.LicenseEvent.md)


These are events reported by License Manager.  <p>  A NoLicenseEvent is reported if the required licenses could not be  reserved. Each feature that is not fully licensed is reported.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| feature | [vim.LicenseManager.FeatureInfo](vim.LicenseManager.FeatureInfo.md "vim.LicenseManager.FeatureInfo") | None | None |  |


