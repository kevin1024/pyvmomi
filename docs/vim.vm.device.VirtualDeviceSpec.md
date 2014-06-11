vim.vm.device.VirtualDeviceSpec
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The VirtualDeviceSpec data object type encapsulates change   specifications for an individual virtual device. The virtual   device being added or modified must be fully specified.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| operation | [vim.vm.device.VirtualDeviceSpec.Operation](vim.vm.device.VirtualDeviceSpec.Operation.md "vim.vm.device.VirtualDeviceSpec.Operation") | true | None | Type of operation being performed on the specified virtual device.   If no operation is specified, the spec. is ignored. |
| fileOperation | [vim.vm.device.VirtualDeviceSpec.FileOperation](vim.vm.device.VirtualDeviceSpec.FileOperation.md "vim.vm.device.VirtualDeviceSpec.FileOperation") | true | None | Type of operation being performed on the backing   of the specified virtual device.   If no file operation is specified in the VirtualDeviceSpec,   then any backing filenames in the   <a href="vim.vm.device.VirtualDevice.md">VirtualDevice</a>   must refer to files that already exist.   The "replace" and "delete" values for this property are only   applicable to virtual disk backing files. |
| device | [vim.vm.device.VirtualDevice](vim.vm.device.VirtualDevice.md "vim.vm.device.VirtualDevice") | None | None | Device specification, with all necessary properties set. |
| profile | [vim.vm.ProfileSpec](vim.vm.ProfileSpec.md "vim.vm.ProfileSpec") | true | None | Virtual Device Profile requirement.   Profiles are solution specifics.   Storage Profile Based Management(SPBM) is a vSphere server extension.  The API users who want to provision VMs using Storage Profiles, need to  interact with SPBM service.   This is an optional parameter and if user doesn't specify profile,  the default behavior will apply. |


