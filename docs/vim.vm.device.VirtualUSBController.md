vim.vm.device.VirtualUSBController
==================================
inherits from [vim.vm.device.VirtualController](docs/vim.vm.device.VirtualController.md)


The <a href="vim.vm.device.VirtualUSBController.md">VirtualUSBController</a> data object describes a virtual USB controller   and contains a list of the devices connected to the controller.   A virtual machine must have a virtual USB controller before you can add   a USB device to the virtual machine configuration. To add a controller,   include a <a href="vim.vm.device.VirtualUSBController.md">VirtualUSBController</a> object in the   <a href="vim.vm.device.VirtualDeviceSpec.md">VirtualDeviceConfigSpec</a> for your virtual machine configuration.   You can add only one controller to a virtual machine.   A virtual USB controller supports up to 20 USB device connections on the   virtual machine.   <p>   The ESX Server host must have the USB controller hardware and modules   that support USB 2.0 and USB1.1.   You can use a maximum of 15 USB controllers on a host. If your system   includes an additional number of controllers with connected devices,   the additional devices will not be available to virtual machines on the host.   <p>   You must remove all USB devices from a virtual machine before you can   remove the USB controller.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| autoConnectDevices | bool | true | None | Flag to indicate whether or not the ability to hot plug devices   is enabled on this controller. |
| ehciEnabled | bool | true | None | Flag to indicate whether or not enhanced host controller   interface (USB 2.0) is enabled on this controller. |


