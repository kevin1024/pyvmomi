vim.PrivilegePolicyDef
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Describes a basic privilege policy.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| createPrivilege | string | None | None | Name of privilege required for creation. |
| readPrivilege | string | None | None | Name of privilege required for reading. |
| updatePrivilege | string | None | None | Name of privilege required for updating. |
| deletePrivilege | string | None | None | Name of privilege required for deleting. |


