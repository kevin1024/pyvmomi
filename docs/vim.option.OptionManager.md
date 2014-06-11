vim.option.OptionManager
========================


This managed object type is used for managing key/value pair    options.   <p>   <ul>   <li>You can define options on the fly, in a logical tree using a dot notation   for keys.  For example, "Ethernet.Connection" describes the Connection   option as child of the Ethernet option.   <li>You can use the queryMethod to retrieve a single property or    a subset of properties based on the dot notation path.   </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='supportedOption'>supportedOption</a> | [vim.option.OptionDef](vim.option.OptionDef.md "vim.option.OptionDef") | true | None | A list of supported key/value pair options including their    type information. |
| <a href='setting'>setting</a> | [vim.option.OptionValue](vim.option.OptionValue.md "vim.option.OptionValue") | true | None | A list of the current settings for the key/value pair options. |


QueryOptions([name](#string "string"))
--------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName")

---
| service name | QueryOptions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if no option or subtree exists with the           given name. |




UpdateOptions([changedValue](vim.option.OptionValue.md "vim.option.OptionValue"))
---------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | UpdateOptions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if one or more OptionValue objects refers to a            non-existent option. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if one or more OptionValue contains an            invalid value. |




