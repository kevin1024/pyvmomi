vim.host.SecuritySpec
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


DataObject used for configuring the Security settings

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| adminPassword | string | true | None | Administrator password to configure |
| removePermission | [vim.AuthorizationManager.Permission](vim.AuthorizationManager.Permission.md "vim.AuthorizationManager.Permission") | true | None | Permissions to remove |
| addPermission | [vim.AuthorizationManager.Permission](vim.AuthorizationManager.Permission.md "vim.AuthorizationManager.Permission") | true | None | Permissions to add |


