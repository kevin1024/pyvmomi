vim.TaskInfo
============
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type contains all information about a task. A task   represents an operation performed by VirtualCenter or ESX.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The unique key for the task. |
| task | [vim.Task](vim.Task.md "vim.Task") | None | None | The managed object that represents this task. |
| description | [vmodl.LocalizableMessage](vmodl.LocalizableMessage.md "vmodl.LocalizableMessage") | true | None | The description field of the task describes the current phase of    operation of the task. For a task that does a single monolithic   activity, this will be fixed and unchanging.   For tasks that have various substeps, this field will change   as the task progresses from one phase to another. |
| name | string | true | None | The name of the operation that created the task. This is not set    for internal tasks. |
| descriptionId | string | None | None | An identifier for this operation. This includes publicly visible   internal tasks and is a lookup in the TaskDescription methodInfo   data object. |
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | Managed entity to which the operation applies. |
| entityName | string | true | None | The name of the managed entity, locale-specific, retained for the   history collector database. |
| locked | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | If the state of the task is "running", then this property is a list of   managed entities that the operation has locked, with a shared lock. |
| state | [vim.TaskInfo.State](vim.TaskInfo.State.md "vim.TaskInfo.State") | None | None | Runtime status of the task. |
| cancelled | bool | None | None | Flag to indicate whether or not the client requested   cancellation of the task. |
| cancelable | bool | None | None | Flag to indicate whether or not the cancel task operation is supported. |
| error | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | If the task state is "error", then this property contains the fault code. |
| result | object | true | None | If the task state is "success", then this property may be used   to hold a return value. |
| progress | int | true | None | If the task state is "running", then this property contains a   progress measurement, expressed as percentage completed, from 0 to 100.   <p>   If this property is not set, then the command does not report progress. |
| reason | [vim.TaskReason](vim.TaskReason.md "vim.TaskReason") | None | None | Kind of entity responsible for creating this task. |
| queueTime | datetime | None | None | Time stamp when the task was created. |
| startTime | datetime | true | None | Time stamp when the task started running. |
| completeTime | datetime | true | None | Time stamp when the task was completed (whether success or failure). |
| eventChainId | int | None | None | Event chain ID that leads to the corresponding events. |
| changeTag | string | true | None | The user entered tag to identify the operations and their side effects |
| parentTaskKey | string | true | None | Tasks can be cretaed by another task. This shows <a href="vim.TaskInfo.md#key">key</a> of the task spun off this task. This is to  track causality between tasks. |
| rootTaskKey | string | true | None | Tasks can be cretaed by another task and such creation can go on for  multiple levels. This is the <a href="vim.TaskInfo.md#key">key</a> of the task  that started the chain of tasks. |


