vim.CustomFieldsManager.FieldDef
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Describes a custom field.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | int | None | None | A unique ID used to reference this custom field in assignments. This   ID is unique for the lifetime of the field (even across   rename operations). |
| name | string | None | None | Name of the field. |
| type | string | None | None | Type of the field. |
| managedObjectType | string | true | None | Type of object for which the field is valid. If not specified,   the field is valid for all managed objects. |
| fieldDefPrivileges | [vim.PrivilegePolicyDef](vim.PrivilegePolicyDef.md "vim.PrivilegePolicyDef") | true | None | The set of privileges to apply on this field definition |
| fieldInstancePrivileges | [vim.PrivilegePolicyDef](vim.PrivilegePolicyDef.md "vim.PrivilegePolicyDef") | true | None | The set of privileges to apply on instances of this field |


