vim.vm.device.VirtualDeviceOption.URIBackingOption
==================================================
inherits from [vim.vm.device.VirtualDeviceOption.BackingOption](docs/vim.vm.device.VirtualDeviceOption.BackingOption.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The URIBackingOption data object type describes network communication   options for virtual devices.   When establishing a connection with a remote system on the network,   the virtual machine can act as a server or a client.   When the virtual machine acts as a server, it accepts a connection.   When the virtual machine acts as a client, it initiates the connection.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| directions | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | List of possible directions. Valid directions are:   <ul>   <li><a href="vim.vm.device.VirtualDeviceOption.URIBackingOption.Direction.md#server">server</a>   <li><a href="vim.vm.device.VirtualDeviceOption.URIBackingOption.Direction.md#client">client</a>   </ul> |


