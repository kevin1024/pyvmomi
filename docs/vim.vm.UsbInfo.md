vim.vm.UsbInfo
==============
inherits from [vim.vm.TargetInfo](docs/vim.vm.TargetInfo.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object contains information about a physical USB device  on the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| description | string | None | None | A user visible name of the USB device. |
| vendor | int | None | None | The vendor ID of the USB device. |
| product | int | None | None | The product ID of the USB device. |
| physicalPath | string | None | None | An autoconnect pattern which describes the device's physical   path. This is the path to the specific port on the host where the   USB device is attached. |
| family | string | true | None | The device class families.   For possible values see   <a href="vim.vm.UsbInfo.Family.md">VirtualMachineUsbInfoFamily</a> |
| speed | string | true | None | The possible device speeds detected by server.   For possible values see   <a href="vim.vm.UsbInfo.Speed.md">VirtualMachineUsbInfoSpeed</a> |
| summary | [vim.vm.Summary](vim.vm.Summary.md "vim.vm.Summary") | true | None | Summary information about the virtual machine that is currently   using this device, if any. |


