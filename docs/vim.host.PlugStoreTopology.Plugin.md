vim.host.PlugStoreTopology.Plugin
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type represents a Plugin in the plug store architecture.   A Plugin claims a set of paths and groups them into Devices.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The identifier of the plugin. |
| name | string | None | None | The name of the plugin. |
| device | [vim.host.PlugStoreTopology.Device](vim.host.PlugStoreTopology.Device.md "vim.host.PlugStoreTopology.Device") | true | None | The set of devices formed by this plugin. |
| claimedPath | [vim.host.PlugStoreTopology.Path](vim.host.PlugStoreTopology.Path.md "vim.host.PlugStoreTopology.Path") | true | None | The set of paths claimed by this plugin.  Not every claimed path   will necessarily appear as part of a Device.  Claimed paths will   only appear under Devices if the device identifier of the path   matches up with the device identifier exposed by the Device. |


