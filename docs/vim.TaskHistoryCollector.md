vim.TaskHistoryCollector
========================
inherits from [vim.HistoryCollector](vim.HistoryCollector.md "vim.HistoryCollector")


TaskHistoryCollector provides a mechanism for  retrieving historical data and updates when the server appends new  tasks.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='latestPage'>latestPage</a> | [vim.TaskInfo](vim.TaskInfo.md "vim.TaskInfo") | true | None | The items in the 'viewable latest page'. As new tasks that match the  collector's <a href="vim.TaskFilterSpec.md">TaskFilterSpec</a> are created, they are added to this  page, and the oldest tasks are removed from the collector to keep the  size of the page to that allowed by  <a href="vim.HistoryCollector.md#setLatestPageSize">SetCollectorPageSize</a>.  <p>  The "oldest task" is the one with the oldest creation time. The  tasks in the returned page are unordered. |


ReadNextTasks()
---------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | ReadNextTasks |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if maxCount is out of range. |




ReadPreviousTasks()
-------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | ReadPreviousTasks |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if maxCount is out of range. |




