vim.vm.device.VirtualController
===============================
inherits from [vim.vm.device.VirtualDevice](docs/vim.vm.device.VirtualDevice.md)


VirtualController is the base data object type for a device controller in   a virtual machine. VirtualController extends   <a href="vim.vm.device.VirtualDevice.md">VirtualDevice</a> to inherit   general information about a controller (such as name and description), and to allow   controllers to appear in a generic list of virtual devices.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| busNumber | int | None | None | Bus number associated with this controller. |
| device | int | true | None | List of devices currently controlled by this controller.    Each entry contains the <a href="vim.vm.device.VirtualDevice.md#key">key</a> property of the   corresponding device object. |


