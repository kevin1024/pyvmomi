vim.host.PlugStoreTopology.Adapter
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type is an association class that describes a host bus   adapter and its associated storage Paths.  The set of Paths on all the   host bus adapters is the complete set of Paths in the system.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The identifier for the host bus adapter. |
| adapter | [vim.host.HostBusAdapter](vim.host.HostBusAdapter.md "vim.host.HostBusAdapter") | None | None | The link to the host bus adapter for this inebtrface. |
| path | [vim.host.PlugStoreTopology.Path](vim.host.PlugStoreTopology.Path.md "vim.host.PlugStoreTopology.Path") | true | None | The list of paths to which the host bus adapter is associated. |


