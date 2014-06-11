vim.CustomFieldsManager
=======================


The CustomFieldsManager object is used to add and remove custom fields   to managed entities.   <p>   The custom fields values set on managed entities are available through the   <a href="vim.ManagedEntity.md#customValue">customValue</a> property and through the summary objects   for <a href="vim.VirtualMachine.md">VirtualMachine</a> and <a href="vim.HostSystem.md">HostSystem</a>. They are not available   directly through this managed object.   <p>   This functionality is only available through VirtualCenter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='field'>field</a> | [vim.CustomFieldsManager.FieldDef](vim.CustomFieldsManager.FieldDef.md "vim.CustomFieldsManager.FieldDef") | true | System.View | List of custom fields defined on this server. The fields are   sorted by name. |


AddCustomFieldDef([name](#string "string"), [moType](#string "string"), [fieldDefPolicy](vim.PrivilegePolicyDef.md "vim.PrivilegePolicyDef"), [fieldPolicy](vim.PrivilegePolicyDef.md "vim.PrivilegePolicyDef"))
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidPrivilege](vim.fault.InvalidPrivilege.md "vim.fault.InvalidPrivilege"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName")

---
| service name | AddCustomFieldDef |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Global.ManageCustomFields |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if a custom field with the name already exists. |
| [vim.fault.InvalidPrivilege](vim.fault.InvalidPrivilege.md "vim.fault.InvalidPrivilege") | if a specified privilege is not defined. |




RemoveCustomFieldDef()
----------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | RemoveCustomFieldDef |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Global.ManageCustomFields |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if no custom field with that key exists. |




RenameCustomFieldDef([name](#string "string"))
----------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName")

---
| service name | RenameCustomFieldDef |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Global.ManageCustomFields |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if a custom field with the name already exists. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if no custom field with that key exists. |




SetField([entity](vim.ManagedEntity.md "vim.ManagedEntity"), [value](#string "string"))
---------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | SetField |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if no custom field with that key exists. |




