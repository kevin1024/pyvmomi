vim.vm.device.VirtualUSBXHCIControllerOption
============================================
inherits from [vim.vm.device.VirtualControllerOption](docs/vim.vm.device.VirtualControllerOption.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The VirtualUSBXHCIControllerOption data object type contains the options   for a virtual USB Extensible Host Controller Interface (USB 3.0).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| autoConnectDevices | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate whether or not the ability to autoconnect devices   is enabled for this virtual USB controller. |
| supportedSpeeds | string | None | None | Range of USB device speeds supported by this USB controller type.   Acceptable values are specified at <a href="vim.vm.UsbInfo.Speed.md">VirtualMachineUsbInfoSpeed</a>. |


