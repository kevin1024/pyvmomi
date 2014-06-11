vim.Extension
=============
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object type contains all information about an extension.   An extension may contain zero or more server interfaces and zero   or more clients.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| description | [vim.Description](vim.Description.md "vim.Description") | None | None | Description of extension. |
| key | string | None | None | Extension key. Should follow java package naming conventions   for uniqueness (e.g. "com.example.management").   <p>   Extension names can only contain characters belonging to the    lower ASCII character set (UTF-7) with the exception of the    following characters:   <ol>   <li>All whitespace characters ("space" - ascii character 0x20 is allowed)</li>   <li>Control characters</li>   <li>Comma (ascii 0x2c), Forward slash (ascii 0x2f), Backward slash (ascii 0x5c),    Hash/Pound (ascii 0x23), Plus (ascii 0x2b), Greater (ascii 0x3e), Lesser (ascii 0x3c),    Equals (ascii 0x3d), Semi-colon (ascii 0x3b) and Double quote (ascii 0x22).</li>   </ol> |
| company | string | true | None | Company information. |
| type | string | true | None | Type of extension (example may include CP-DVS, NUOVA-DVS, etc.). |
| version | string | None | None | Extension version number as a dot-separated string. For example, "1.0.0" |
| subjectName | string | true | None | Subject name from client certificate. |
| server | [vim.Extension.ServerInfo](vim.Extension.ServerInfo.md "vim.Extension.ServerInfo") | true | None | Servers for this extension. |
| client | [vim.Extension.ClientInfo](vim.Extension.ClientInfo.md "vim.Extension.ClientInfo") | true | None | Clients for this extension. |
| taskList | [vim.Extension.TaskTypeInfo](vim.Extension.TaskTypeInfo.md "vim.Extension.TaskTypeInfo") | true | None | Definitions of tasks defined by this extension. |
| eventList | [vim.Extension.EventTypeInfo](vim.Extension.EventTypeInfo.md "vim.Extension.EventTypeInfo") | true | None | Definitions of events defined by this extension. |
| faultList | [vim.Extension.FaultTypeInfo](vim.Extension.FaultTypeInfo.md "vim.Extension.FaultTypeInfo") | true | None | Definitions of faults defined by this extension. |
| privilegeList | [vim.Extension.PrivilegeInfo](vim.Extension.PrivilegeInfo.md "vim.Extension.PrivilegeInfo") | true | None | Definitions privileges defined by this extension. |
| resourceList | [vim.Extension.ResourceInfo](vim.Extension.ResourceInfo.md "vim.Extension.ResourceInfo") | true | None | Resource data for all locales |
| lastHeartbeatTime | datetime | None | None | Last extension heartbeat time. |
| healthInfo | [vim.Extension.HealthInfo](vim.Extension.HealthInfo.md "vim.Extension.HealthInfo") | true | None | Health specification provided by this extension. |
| ovfConsumerInfo | [vim.Extension.OvfConsumerInfo](vim.Extension.OvfConsumerInfo.md "vim.Extension.OvfConsumerInfo") | true | None | OVF consumer specification provided by this extension. |
| extendedProductInfo | [vim.ext.ExtendedProductInfo](vim.ext.ExtendedProductInfo.md "vim.ext.ExtendedProductInfo") | true | None | Extended product information, such as URLs to vendor, product, etc. |
| managedEntityInfo | [vim.ext.ManagedEntityInfo](vim.ext.ManagedEntityInfo.md "vim.ext.ManagedEntityInfo") | true | None | Information about entities managed by this extension. An extension can  register virtual machines as managed by itself, by setting the  <a href="vim.vm.ConfigSpec.md#managedBy">managedBy</a> property of the virtual  machine. |
| shownInSolutionManager | bool | true | None | Opt-in to the Solution Manager. If set to true, this extension will be  shown in the Solution Manager. If not set, or set to false, this extension  is not shown in the Solution Manager. |
| solutionManagerInfo | [vim.ext.SolutionManagerInfo](vim.ext.SolutionManagerInfo.md "vim.ext.SolutionManagerInfo") | true | None | Solution Manager configuration for this extension. |


