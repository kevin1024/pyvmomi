vim.vm.device.VirtualCdromOption.RemotePassthroughBackingOption
===============================================================
inherits from [vim.vm.device.VirtualDeviceOption.RemoteDeviceBackingOption](docs/vim.vm.device.VirtualDeviceOption.RemoteDeviceBackingOption.md)


The VirtualCdromOption.RemotePassthroughBackingOption data object type   contains the options for a remote pass-through CD-ROM device backing.   <p>   Note that the server cannot present a list of valid remote backing devices   because it is unable to scan remote hosts.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| exclusive | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate whether or not exclusive CD-ROM device access is supported. |


