vim.profile.ComplianceManager
=============================
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Interface handling the Compliance aspects of entities.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


CheckCompliance([profile](vim.profile.Profile.md "vim.profile.Profile"), [entity](vim.ManagedEntity.md "vim.ManagedEntity"))
----------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | CheckCompliance |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If neither profile nor entity is specified. |




QueryComplianceStatus([profile](vim.profile.Profile.md "vim.profile.Profile"), [entity](vim.ManagedEntity.md "vim.ManagedEntity"))
----------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryComplianceStatus |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If neither profile nor entity is specified. |




ClearComplianceStatus([profile](vim.profile.Profile.md "vim.profile.Profile"), [entity](vim.ManagedEntity.md "vim.ManagedEntity"))
----------------------------------------------------------------------------------------------------------------------------------

| service name | ClearComplianceStatus |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Profile.Clear |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryExpressionMetadata([expressionName](#string "string"), [profile](vim.profile.Profile.md "vim.profile.Profile"))
--------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryExpressionMetadata |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If expressionName is invalid. |




