vim.event.EventHistoryCollector
===============================
inherits from [vim.HistoryCollector](vim.HistoryCollector.md "vim.HistoryCollector")


EventHistoryCollector provides a mechanism for  retrieving historical data and updates when the server appends new  events.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='latestPage'>latestPage</a> | [vim.event.Event](vim.event.Event.md "vim.event.Event") | true | None | The items in the 'viewable latest page'. As new events that match the  collector's <a href="vim.event.EventFilterSpec.md">EventFilterSpec</a> are created, they are added to this  page, and the oldest events are removed from the collector to keep the  size of the page to that allowed by  HistoryCollector#setLatestPageSize.  <p>  The "oldest event" is the one with the smallest key (event ID). The  events in the returned page are unordered. |


ReadNextEvents()
----------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | ReadNextEvents |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if maxCount is out of range. |




ReadPreviousEvents()
--------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | ReadPreviousEvents |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if maxCount is out of range. |




