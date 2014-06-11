vim.VirtualDiskManager.FileBackedVirtualDiskSpec
================================================
inherits from [vim.VirtualDiskManager.VirtualDiskSpec](docs/vim.VirtualDiskManager.VirtualDiskSpec.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Specification used to create a file based virtual disk

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| capacityKb | long | None | None | Specify the capacity of the virtual disk in Kb. |
| profile | [vim.vm.ProfileSpec](vim.vm.ProfileSpec.md "vim.vm.ProfileSpec") | true | None | Virtual Disk Profile requirement.   Profiles are solution specifics.   Profile Based Storage Management is a vSphere server extension.  The API users who want to provision VMs using Storage Profiles, need to  interact with it.   This is an optional parameter and if user doesn't specify profile,  the default behavior will apply. |


