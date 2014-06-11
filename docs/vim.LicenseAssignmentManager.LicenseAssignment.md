vim.LicenseAssignmentManager.LicenseAssignment
==============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entityId | string | None | None | Id for the entity |
| scope | string | true | None | Scope of the entityId |
| entityDisplayName | string | true | None | Display name of the entity |
| assignedLicense | [vim.LicenseManager.LicenseInfo](vim.LicenseManager.LicenseInfo.md "vim.LicenseManager.LicenseInfo") | None | None | License assigned to the entity |
| properties | [vmodl.KeyAnyValue](vmodl.KeyAnyValue.md "vmodl.KeyAnyValue") | true | None | Additional properties associated with this assignment  Some of the properties are:  "inUseFeatures"  -- Features in the license key that are being used by the entity  "ProductName"    -- Name of the entity. Should match the product name of the assigned license.  "ProductVersion" -- Version of the entity. Should match the product version of the assigned license.  "Evaluation" -- EvaluationInfo object representing the evaluation left for the entity. |


