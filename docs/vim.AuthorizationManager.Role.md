vim.AuthorizationManager.Role
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type specifies a collection of privileges used    to grant access to users on managed entities.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| roleId | int | None | None | Unique role identifier. |
| system | bool | None | None | Whether or not the role is system-defined. System-defined roles cannot be    changed. |
| name | string | None | None | System-defined or user-defined role name. |
| info | [vim.Description](vim.Description.md "vim.Description") | None | None | Displayable role information. |
| privilege | string | true | None | Privileges provided by this role, by privilege identifier. |


