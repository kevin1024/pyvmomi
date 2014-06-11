vim.TaskManager
===============


The TaskManager managed object provides an interface for creating and managing   <a href="vim.Task.md">Task</a> managed objects. Many operations are non-blocking,   returning a <a href="vim.Task.md">Task</a> managed object that can be monitored by a   client application. <a href="vim.Task.md">Task</a> managed objects may also be   accessed through the TaskManager.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='recentTask'>recentTask</a> | [vim.Task](vim.Task.md "vim.Task") | true | System.View | A list of <a href="vim.Task.md">Task</a> managed objects that completed recently,   that are currently running, or that are queued to run.   </ul>   <p>   The list contains only <a href="vim.Task.md">Task</a> objects that the client   has permission to access, which is determined by having permission to   access the <a href="vim.Task.md">Task</a> object's managed <a href="vim.TaskInfo.md#entity">entity</a>.   <p>   The completed <a href="vim.Task.md">Task</a> objects by default include only   <a href="vim.Task.md">Task</a> objects that completed within the past 10 minutes.   When connected to vCenter Server, there is an additional default limitation   that each of the completed <a href="vim.Task.md">Task</a> objects in this list is one   of the last 200 completed <a href="vim.Task.md">Task</a> objects.   <p>   This property should not be used for tracking <a href="vim.Task.md">Task</a>   completion. Generally, a <a href="vim.view.ListView.md">ListView</a> is a better way to   monitor a specific set of <a href="vim.Task.md">Task</a> objects.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter. Any other version value will not   produce any property values as no updates are generated. |
| <a href='description'>description</a> | [vim.TaskDescription](vim.TaskDescription.md "vim.TaskDescription") | None | System.View | Locale-specific, static strings that describe <a href="vim.Task.md">Task</a>   information to users. |
| <a href='maxCollector'>maxCollector</a> | int | None | System.View | Maximum number of <a href="vim.TaskHistoryCollector.md">TaskHistoryCollector</a>   data objects that can exist concurrently, per client. |


CreateCollectorForTasks([filter](vim.TaskFilterSpec.md "vim.TaskFilterSpec"))
-----------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | CreateCollectorForTasks |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if there are more than the maximum number of                        task collectors. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the filter is null or unknown. |




CreateTask([obj](#vim.ExtensibleManagedObject "vim.ExtensibleManagedObject"), [taskTypeId](#string "string"), [initiatedBy](#string "string"), [parentTaskKey](#string "string"))
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

| service name | CreateTask |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Task.Create |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




