vim.PerformanceManager.MetricId
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type contains information that associates a performance   counter with a performance metric. When constructing this data object for   the <a href="vim.PerformanceManager.QuerySpec.md#metricId">metricId</a> property of the <a href="vim.PerformanceManager.QuerySpec.md">PerfQuerySpec</a> to submit to one of the <a href="vim.PerformanceManager.md">PerformanceManager</a> query operations, the <a href="vim.PerformanceManager.MetricId.md#instance">instance</a> property   supports these special characters: <ul>    <li> An asterisk (*) to specify all instances of the metric for the        specified <a href="vim.PerformanceManager.MetricId.md#counterId">counterId</a> </li>    <li> Double-quotes ("") to specify aggregated statistics </li>    </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| counterId | int | None | None | The <a href="vim.PerformanceManager.CounterInfo.md#key">ID</a> of the counter for   the metric. |
| instance | string | None | None | An identifier that is derived from configuration names for the device   associated with the metric. It identifies the instance of the metric   with its source. This property may be empty. <ul>    <li> For memory and aggregated statistics, this property is empty. </li>    <li> For host and virtual machine devices, this property contains the        name of the device, such as the name of the host-bus adapter or        the name of the virtual Ethernet adapter. For example,        &#147;mpx&#46;vmhba33&#58;C0&#58;T0&#58;L0&#148; or        &#147;vmnic0&#58;&#148; </li>    <li> For a CPU, this property identifies the numeric position within        the CPU core, such as 0, 1, 2, 3. </li>    <li> For a virtual disk, this property identifies the file type: <ul>       <li> DISKFILE, for virtual machine base-disk files </li>      <li> SWAPFILE, for virtual machine swap files </li>      <li> DELTAFILE, for virtual machine snapshot overhead files </li>      <li> OTHERFILE, for all other files of a virtual machine </li>      </ul></li>    </ul> |


