vim.vm.device.VirtualSerialPortOption
=====================================
inherits from [vim.vm.device.VirtualDeviceOption](docs/vim.vm.device.VirtualDeviceOption.md)


The <code><a href="vim.vm.device.VirtualSerialPortOption.md">VirtualSerialPortOption</a></code> data object contains the options   for configuring the virtual serial port device defined by the   <code><a href="vim.vm.device.VirtualSerialPort.md">VirtualSerialPort</a></code> data object.   These options include information about how the device is backed   physically on the host:  by a network socket, a host file, a host serial port device,   or a pipe to another process.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| yieldOnPoll | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Indicates whether the virtual machine supports the CPU yield option during   virtual serial port polling. When this feature is supported and enabled,   the virtual machine will periodically relinquish the processor if its   sole task is polling the virtual serial port.   <p>   If <code>yieldOnPoll.supported</code> is <code>false</code>, the virtual   machine ignores the virtual serial port object setting for   <code><a href="vim.vm.device.VirtualSerialPort.md#yieldOnPoll">yieldOnPoll</a></code>. |


