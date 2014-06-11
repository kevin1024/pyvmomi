vim.host.PlugStoreTopology.Device
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type is an association class that describes a ScsiLun   and its associated Path objects.  The ScsiLun is a Device that is formed   from a set of Paths.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Linkable identifier. |
| lun | [vim.host.ScsiLun](vim.host.ScsiLun.md "vim.host.ScsiLun") | None | None | The SCSI device corresponding to logical unit. |
| path | [vim.host.PlugStoreTopology.Path](vim.host.PlugStoreTopology.Path.md "vim.host.PlugStoreTopology.Path") | true | None | The array of paths available to access this LogicalUnit. |


