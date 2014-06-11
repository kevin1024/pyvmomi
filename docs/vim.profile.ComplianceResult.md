vim.profile.ComplianceResult
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


DataObject representing the result from a ComplianceCheck

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| profile | [vim.profile.Profile](vim.profile.Profile.md "vim.profile.Profile") | true | None | Profile for which the ComplianceResult applies |
| complianceStatus | string | None | None | Indicates the compliance status of the entity.  See |
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | Entity on which the compliance check was carried out.  Entity can be a Cluster, Host and so on. |
| checkTime | datetime | true | None | Time at which compliance check was last run on the entity |
| failure | [vim.profile.ComplianceResult.ComplianceFailure](vim.profile.ComplianceResult.ComplianceFailure.md "vim.profile.ComplianceResult.ComplianceFailure") | true | None | If complianceStatus is non-compliant, failure will  contain additional information about the compliance errors. |


