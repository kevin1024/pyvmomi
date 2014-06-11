vim.ExtensibleManagedObject
===========================


<a href="vim.ExtensibleManagedObject.md">ExtensibleManagedObject</a> provides methods and properties that provide   access to custom fields that may be associated with a managed object.   Use the <a href="vim.CustomFieldsManager.md">CustomFieldsManager</a> to define custom fields.   The <a href="vim.CustomFieldsManager.md">CustomFieldsManager</a> handles the entire list of custom fields   on a server. You can can specify the object type to which a particular custom    field applies by setting its <a href="vim.CustomFieldsManager.FieldDef.md#managedObjectType">managedObjectType</a>.   (If you do not set a managed object type for a custom field definition,   the field applies to all managed objects.)

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='value'>value</a> | [vim.CustomFieldsManager.Value](vim.CustomFieldsManager.Value.md "vim.CustomFieldsManager.Value") | true | System.View | List of custom field values. Each value uses a key to associate   an instance of a <a href="vim.CustomFieldsManager.StringValue.md">CustomFieldStringValue</a> with   a custom field definition. |
| <a href='availableField'>availableField</a> | [vim.CustomFieldsManager.FieldDef](vim.CustomFieldsManager.FieldDef.md "vim.CustomFieldsManager.FieldDef") | true | System.View | List of custom field definitions that are valid for the object's type.    The fields are sorted by <a href="vim.CustomFieldsManager.FieldDef.md#name">name</a>. |


setCustomValue([key](#string "string"), [value](#string "string"))
------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | setCustomValue |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if no custom field with that key exists. |




