vim.vm.device.VirtualSerialPort.PipeBackingInfo
===============================================
inherits from [vim.vm.device.VirtualDevice.PipeBackingInfo](docs/vim.vm.device.VirtualDevice.PipeBackingInfo.md)


The <code><a href="vim.vm.device.VirtualSerialPort.PipeBackingInfo.md">VirtualSerialPortPipeBackingInfo</a></code> data object defines information   for backing a <code><a href="vim.vm.device.VirtualSerialPort.md">VirtualSerialPort</a></code> with a named pipe.   You can use a pipe to connect a virtual serial port to a host   application or to another virtual machine on the host computer.   This is useful for capturing debugging information sent through   the virtual serial port.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| endpoint | string | None | None | Indicates the role the virtual machine assumes as an endpoint   for the pipe. The valid values are "client" or "server". |
| noRxLoss | bool | true | None | Enables optimized data transfer over the pipe. When you use this feature,   the ESX server buffers data to prevent data overrun.   This allows the virtual machine to read   all of the data transferred over the pipe with no data loss.   To use optimized data transfer, set <code>noRxLoss</code> to <code>true</code>.   To disable this feature, set the property to <code>false</false>.   <p>   This property is optional. If this property is not set, the ESX server   uses the default value specified in the pipe backing options   (noRxLoss.defaultValue - see   <code><a href="vim.vm.device.VirtualSerialPortOption.PipeBackingOption.md#noRxLoss">noRxLoss</a></code>   in the pipe backing option object).   <p>   To use this property, optimized data transfer must be supported on the host.   (See <code><a href="vim.vm.device.VirtualSerialPortOption.PipeBackingOption.md#noRxLoss">noRxLoss</a></code>   in the pipe backing option object.)   If the ESX server does not support the option, it ignores the   <code>noRxLoss</code> setting in the pipe backing information object.   <p>   <b>Note</b>: You can use this feature even if the other end of the pipe   is not an application, but this is more likely to fail. |


