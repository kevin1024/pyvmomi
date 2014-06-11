vim.vm.device.VirtualSerialPortOption.PipeBackingOption
=======================================================
inherits from [vim.vm.device.VirtualDeviceOption.PipeBackingOption](docs/vim.vm.device.VirtualDeviceOption.PipeBackingOption.md)


The <code><a href="vim.vm.device.VirtualSerialPortOption.PipeBackingOption.md">VirtualSerialPortPipeBackingOption</a></code> data object contains   the options for backing a serial port device with a pipe to another process.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| endpoint | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | Indicates the choices available and the default setting   for the pipe endpoint. As an endpoint, the virtual machine can act   as a client or a server. |
| noRxLoss | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Indicates whether the server supports optimized data transfer   over the pipe and also specifies default behavior.   <p>   When this feature is supported and enabled, the server buffers data   to prevent data overrun. This allows the virtual machine to read all   of the data transferred over the pipe with no data loss.   <p>   If optimized data transfer is supported (<code>noRxLoss.supported</code>   is <code>true</code>):   <ul>     <li>You can enable (or disable) the feature explicitly by setting the         <code><a href="vim.vm.device.VirtualSerialPort.PipeBackingInfo.md#noRxLoss">noRxLoss</a></code>         property on the pipe backing information object.     <li>If you do not set the         <code><a href="vim.vm.device.VirtualSerialPort.PipeBackingInfo.md#noRxLoss">noRxLoss</a></code>         property on the         the pipe backing information object, the server enables         optimized data transfer if the <code>noRxLoss.defaultValue</code>         property on the pipe backing options object is <code>true</code>.   </ul>   <p>   If <code>noRxLoss.supported</code> is <code>false</code>, the server   ignores the optimization settings.   <p>   <b>Note</b>: You can use this feature even if the other end of the pipe   is not an application, but it is more likely to fail. |


