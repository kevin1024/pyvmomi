vim.AuthorizationManager.EntityPrivilege
========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines whether a set of privileges are granted for a managed entity.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | None | None | The entity on which the privileges are checked. |
| privAvailability | [vim.AuthorizationManager.PrivilegeAvailability](vim.AuthorizationManager.PrivilegeAvailability.md "vim.AuthorizationManager.PrivilegeAvailability") | None | None | whether a set of privileges are granted for the managed entity. |


