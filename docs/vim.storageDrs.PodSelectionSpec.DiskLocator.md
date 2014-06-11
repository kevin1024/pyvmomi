vim.storageDrs.PodSelectionSpec.DiskLocator
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The disk locator class.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskId | int | None | None | The disk ID. |
| diskMoveType | string | true | None | The disk move type. |
| diskBackingInfo | [vim.vm.device.VirtualDevice.BackingInfo](vim.vm.device.VirtualDevice.BackingInfo.md "vim.vm.device.VirtualDevice.BackingInfo") | true | None | The disk backing info. |
| profile | [vim.vm.ProfileSpec](vim.vm.ProfileSpec.md "vim.vm.ProfileSpec") | true | None | Virtual Disk Profile requirement.   Profiles are solution specific.   Profile Based Storage Management is a vSphere server extension.  The API users who want to provision VMs using Storage Profiles, need to  interact with it.   This is an optional parameter and if user doesn't specify profile,  the default behavior will apply. |


