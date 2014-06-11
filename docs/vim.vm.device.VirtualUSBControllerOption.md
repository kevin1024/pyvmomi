vim.vm.device.VirtualUSBControllerOption
========================================
inherits from [vim.vm.device.VirtualControllerOption](docs/vim.vm.device.VirtualControllerOption.md)


The VirtualUSBControllerOption data object type contains the options   for a virtual USB Host Controller Interface.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| autoConnectDevices | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate whether or not the ability to autoconnect devices   is enabled for this virtual USB controller. |
| ehciSupported | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate whether or not enhanced host controller   interface (USB 2.0) is available on this virtual USB controller. |
| supportedSpeeds | string | None | None | Range of USB device speeds supported by this USB controller type.   Acceptable values are specified at <a href="vim.vm.UsbInfo.Speed.md">VirtualMachineUsbInfoSpeed</a>. |


