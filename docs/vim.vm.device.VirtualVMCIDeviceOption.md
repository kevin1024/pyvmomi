vim.vm.device.VirtualVMCIDeviceOption
=====================================
inherits from [vim.vm.device.VirtualDeviceOption](docs/vim.vm.device.VirtualDeviceOption.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version4)


The <a href="vim.vm.device.VirtualVMCIDeviceOption.md">VirtualMachineVMCIDeviceOption</a> data object contains the options    for the virtual VMCI device (<a href="vim.vm.device.VirtualVMCIDevice.md">VirtualMachineVMCIDevice</a>).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| allowUnrestrictedCommunication | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Indicates support for VMCI communication and specifies the default   operation. If <a href="vim.option.BoolOption.md#defaultValue">defaultValue</a> is set to true,   the virtual machine can participate in VMCI communication with all other   virtual machines on the host. Otherwise, VMCI communication will be   restricted to trusted services such as the hypervisor on the host. |


