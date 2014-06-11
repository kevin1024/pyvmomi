vim.vm.DiskDeviceInfo
=====================
inherits from [vim.vm.TargetInfo](docs/vim.vm.TargetInfo.md)


The DiskDeviceInfo class contains basic information about a specific disk hardware   device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| capacity | long | true | None | Size of disk |
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | true | None | List of known virtual machines using this physical disk as a backing |


