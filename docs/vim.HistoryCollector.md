vim.HistoryCollector
====================


This managed object type enables clients to retrieve historical data and   receive updates when the server appends new data to a collection.   This is a base type for item-specific types related to event or task history.    Historical data is inherently append-only,  although a server administrator may periodically purge old data.  <p>  Typically, a client creates a history collector by using a filter on a  potentially large set, such as all the events in a datacenter.  The collector provides access to the items that match the filter,  which could also be a relatively large set.  <p>  The items in a collector are always ordered by date and time of creation.  Item properties normally include this time stamp.  <p>  The client may set the "viewable latest page" for the collector,  which is the contiguous subset of the items that are of  immediate interest. These items are available as the "latestPage"  property, which the client may retrieve and monitor by using the  <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> managed object.   <p>  Clients can change the page size of the "latestPage" by using   <a href="vim.HistoryCollector.md#setLatestPageSize">setLatestPageSize()</a>.  <p>  The client may use the following features of the history collector.  <ul>  <li><a href="vim.HistoryCollector.md#rewind">RewindCollector</a> - Moves the "scrollable view" to   the oldest item (the default setting).  <li>readNext - Retrieves all the items in the collector, from the oldest  item to the newest item. Retrieves either   <a href="vim.TaskHistoryCollector.md#readNext">tasks</a> or   <a href="vim.event.EventHistoryCollector.md#readNext">events</a> depending on the operation.   <li>readPrev - Retrieves all items (excluding the "viewable latest page") in  the collector, from the newest item to the oldest item. Retrieves either   <a href="vim.TaskHistoryCollector.md#readPrev">tasks</a> or   <a href="vim.event.EventHistoryCollector.md#readPrev">events</a> depending on the operation.  <li><a href="vim.HistoryCollector.md#reset">ResetCollector</a> - Moves the "scrollable view" to   the item immediately preceding the "viewable latest page".  </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='filter'>filter</a> | object | None | None | The filter used to create this collector.  <p>  The type of the returned filter is determined by the managed object  for which the collector is created. |


SetCollectorPageSize()
----------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | SetCollectorPageSize |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if maxCount is out of range. |




RewindCollector()
-----------------

| service name | RewindCollector |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




ResetCollector()
----------------

| service name | ResetCollector |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




DestroyCollector()
------------------

| service name | DestroyCollector |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




