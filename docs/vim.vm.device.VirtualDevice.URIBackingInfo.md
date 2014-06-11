vim.vm.device.VirtualDevice.URIBackingInfo
==========================================
inherits from [vim.vm.device.VirtualDevice.BackingInfo](docs/vim.vm.device.VirtualDevice.BackingInfo.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The <code><a href="vim.vm.device.VirtualDevice.URIBackingInfo.md">VirtualDeviceURIBackingInfo</a></code> data object type   defines information for using a network socket as backing for a virtual device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| serviceURI | string | None | None | Identifies the local host or a system on the network,   depending on the value of <code><a href="vim.vm.device.VirtualDevice.URIBackingInfo.md#direction">direction</a></code>.   <ul>     <li>If you use the virtual machine as a server, the URI identifies         the host on which the virtual machine runs. In this case,         the host name part of the URI should be empty, or it should         specify the address of the local host.     <li>If you use the virtual machine as a client, the URI identifies         the remote system on the network.   </ul> |
| direction | string | None | None | The direction of the connection.  For possible values see   <a href="vim.vm.device.VirtualDeviceOption.URIBackingOption.Direction.md">VirtualDeviceURIBackingOptionDirection</a> |
| proxyURI | string | true | None | Identifies a proxy service that provides network access to the   <code><a href="vim.vm.device.VirtualDevice.URIBackingInfo.md#serviceURI">serviceURI</a></code>.   If you specify a proxy URI, the virtual machine initiates   a connection with the proxy service and forwards the   <a href="vim.vm.device.VirtualDevice.URIBackingInfo.md#serviceURI">serviceURI</a> and <a href="vim.vm.device.VirtualDevice.URIBackingInfo.md#direction">direction</a> to the proxy. |


