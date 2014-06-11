vim.LicenseAssignmentManager
============================
as of [vSphere API 4.0](vim.version.md#vim.version.version5)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


UpdateAssignedLicense([entity](#string "string"), [licenseKey](#string "string"), [entityDisplayName](#string "string"))
------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.LicenseEntityNotFound](vim.fault.LicenseEntityNotFound.md "vim.fault.LicenseEntityNotFound")

---
| service name | UpdateAssignedLicense |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Global.Licenses |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.LicenseEntityNotFound](vim.fault.LicenseEntityNotFound.md "vim.fault.LicenseEntityNotFound") | vim.fault.LicenseEntityNotFound |




RemoveAssignedLicense([entityId](#string "string"))
---------------------------------------------------
 raises [vim.fault.LicenseEntityNotFound](vim.fault.LicenseEntityNotFound.md "vim.fault.LicenseEntityNotFound")

---
| service name | RemoveAssignedLicense |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Global.Licenses |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.LicenseEntityNotFound](vim.fault.LicenseEntityNotFound.md "vim.fault.LicenseEntityNotFound") | vim.fault.LicenseEntityNotFound |




QueryAssignedLicenses([entityId](#string "string"))
---------------------------------------------------

| service name | QueryAssignedLicenses |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




