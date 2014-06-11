vim.host.DatastoreBrowser.VmDiskQuery.Details
=============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Details for the virtual disk primary file.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskType | bool | None | None | The flag to indicate whether the type of the physical disk backing   the virtual disk is returned. |
| capacityKb | bool | None | None | The flag to indicate whether the capacity of the virtual disk from   the point of view of a virtual machine is returned. |
| hardwareVersion | bool | None | None | The flag to indicate whether the hardware version of the virtual disk   file is returned. |
| controllerType | bool | true | None | The flag to indicate whether or not the controller type of the virtual disk   file is returned. |
| diskExtents | bool | true | None | The flag to indicate whether or not the disk extents of the virtual disk   are returned. |
| thin | bool | true | None | The flag to indicate whether the thin-ness of the disk is returned. |


