vim.dvs.DistributedVirtualPort.FilterPolicy
===========================================
inherits from [vim.InheritablePolicy](docs/vim.InheritablePolicy.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines Network Filter Policy.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| filterConfig | [vim.dvs.DistributedVirtualPort.FilterConfig](vim.dvs.DistributedVirtualPort.FilterConfig.md "vim.dvs.DistributedVirtualPort.FilterConfig") | true | None | List of Network Filter Configurations.   In an update operation, the array can contain all   <a href="vim.dvs.DistributedVirtualPort.TrafficFilterConfigSpec.md">DvsTrafficFilterConfigSpec</a> objects   or all <a href="vim.dvs.DistributedVirtualPort.FilterConfig.md">DvsFilterConfig</a> and   <a href="vim.dvs.DistributedVirtualPort.TrafficFilterConfig.md">DvsTrafficFilterConfig</a>   object, but not mixed of Config and Spec objects. If array of   FilterConfigSpec and TrafficFilterConfigSpec is used   for updating Network Filter then only the Network Filters   matching <a href="vim.dvs.DistributedVirtualPort.md#key">key</a> /   <a href="vim.dvs.DistributedVirtualPort.md#key">key</a>   is updated.   If array of <a href="vim.dvs.DistributedVirtualPort.FilterConfig.md">DvsFilterConfig</a> and   <a href="vim.dvs.DistributedVirtualPort.TrafficFilterConfig.md">DvsTrafficFilterConfig</a>   is used for updating port settings, the Network Filter   settings will be overridden with the new array specified. The   specified array should only contain FilterConfig and   TrafficFilterConfig objects with FilterConfig#inherited /   TrafficFilterConfig#inherited set to false.   FilterConfig/TrafficFilterConfig  objects with   FilterConfig#inherited/TrafficFilterConfig#inherited as   true in the specified array will be ignored. The updated result will   include FilterConfig/TrafficFilterConfig objects   inherited from parent, if any. |


