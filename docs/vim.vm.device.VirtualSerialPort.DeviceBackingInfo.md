vim.vm.device.VirtualSerialPort.DeviceBackingInfo
=================================================
inherits from [vim.vm.device.VirtualDevice.DeviceBackingInfo](docs/vim.vm.device.VirtualDevice.DeviceBackingInfo.md)


The <code><a href="vim.vm.device.VirtualSerialPort.DeviceBackingInfo.md">VirtualSerialPortDeviceBackingInfo</a></code> data object   defines information for using a host serial port device as backing for a   <code><a href="vim.vm.device.VirtualSerialPort.md">VirtualSerialPort</a></code>. On a host, the first virtual machine   to configure physical device backing for a virtual serial port will obtain   the mapping. As long as that machine maintains the backing, any additional attempts   to configure backing using that device will fail (a recoverable error, see   the connection info <code><a href="vim.vm.device.VirtualDevice.ConnectInfo.md#status">status</a></code>).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


