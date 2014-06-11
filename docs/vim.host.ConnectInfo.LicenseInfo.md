vim.host.ConnectInfo.LicenseInfo
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type describes license information stored on the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| license | [vim.LicenseManager.LicenseInfo](vim.LicenseManager.LicenseInfo.md "vim.LicenseManager.LicenseInfo") | None | None | License information. |
| evaluation | [vim.LicenseManager.EvaluationInfo](vim.LicenseManager.EvaluationInfo.md "vim.LicenseManager.EvaluationInfo") | None | None | Evaluation information. |
| resource | [vim.LicenseManager.LicensableResourceInfo](vim.LicenseManager.LicensableResourceInfo.md "vim.LicenseManager.LicensableResourceInfo") | true | None | Licensable resources information.  <p>NOTE:    The values in this property may not be accurate for pre-5.0 hosts when returned by vCenter 5.0 |


