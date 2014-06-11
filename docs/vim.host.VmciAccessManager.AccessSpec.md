vim.host.VmciAccessManager.AccessSpec
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The AccessSpec data object declares an update to the service  access granted to a VM. The given list of services will either  be granted in addition to existing services, replace the  existing service or be revoked depending on the mode  specified. In case of a revoke, an empty or non-existing service  list indicates that all granted services should be revoked.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | None | None |  |
| services | string | true | None |  |
| mode | string | None | None |  |


