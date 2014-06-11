vim.host.PlugStoreTopology.Path
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type is an association class that describes a Path and   its associated Device.  A Path may be claimed by at most one Device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The identifier for the Path. |
| name | string | None | None | Name of path.  Use this property to correlate this path object to other   path objects.   <p>   The state of the Path can be retrieved from the data object (@link   vim.host.MultipathStateInfo.Path} on the <a href="vim.host.MultipathStateInfo.md">HostMultipathStateInfo</a> data object.   <p>   Use this name to configure LogicalUnit multipathing policy using <a href="vim.host.StorageSystem.md#enableMultipathPath">EnableMultipathPath</a> and <a href="vim.host.StorageSystem.md#disableMultipathPath">DisableMultipathPath</a>. |
| channelNumber | int | true | None | The channel number for a path if applicable. |
| targetNumber | int | true | None | The target number for a path if applicable.  The target number is not   guaranteed to be consistent across reboots or rescans of the adapter. |
| lunNumber | int | true | None | The LUN number for a path if applicable. |
| adapter | [vim.host.PlugStoreTopology.Adapter](vim.host.PlugStoreTopology.Adapter.md "vim.host.PlugStoreTopology.Adapter") | true | None | The adapter that provided the Path. |
| target | [vim.host.PlugStoreTopology.Target](vim.host.PlugStoreTopology.Target.md "vim.host.PlugStoreTopology.Target") | true | None | The target of the Path if any. |
| device | [vim.host.PlugStoreTopology.Device](vim.host.PlugStoreTopology.Device.md "vim.host.PlugStoreTopology.Device") | true | None | The device that claimed the Path if any. |


