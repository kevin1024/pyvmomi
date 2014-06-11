vim.vm.device.VirtualUSB.USBBackingInfo
=======================================
inherits from [vim.vm.device.VirtualDevice.DeviceBackingInfo](docs/vim.vm.device.VirtualDevice.DeviceBackingInfo.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


The <a href="vim.vm.device.VirtualUSB.USBBackingInfo.md">VirtualUSBUSBBackingInfo</a> data object  identifies a USB device on the host where the virtual machine  is located. This type of backing supports only a local connection  where the virtual machine will remain on the host to which the  USB device is attached.  <p>  To identify the USB device, you specify an autoconnect pattern  for the <a href="vim.vm.device.VirtualDevice.DeviceBackingInfo.md#deviceName">deviceName</a>.  The virtual machine can connect to the USB device if the ESX server  can find a USB device described by the autoconnect pattern.  The autoconnect pattern consists of name:value pairs. You can  use any combination of the following fields.  <ul>  <li>path - USB connection path on the host</li>  <li>pid - idProduct field in the USB device descriptor</li>  <li>vid - idVendor field in the USB device descriptor</li>  <li>hostId - unique ID for the host</li>  <li>speed - device speed (low, full, or high)</li>  </ul>  <p>  For example, the following pattern identifies a USB device:  <p>  &nbsp;&nbsp;&nbsp;&nbsp;<code>"path:1/3/0 hostId:44\ 45\ 4c\ 43\ 00\ 10\ 54-80\ 35\ ca\ c0\ 4f\ 4d\ 37\ 31"</code>  <p>  This pattern identifies the USB device connected to port 1/3/0 on the  host with the unique id <code>0x44454c4c430010548035cac04f4d3731</code>.  <p>  Special characters for autoconnect pattern values:  <ul>  <li>The name and value are separated by a colon (:). </li>  <li>Name:value pairs are separated by spaces. </li>  <li>The escape character is a backslash (\). Use a single backslash to embed  a space in a value. Use a double blackslash to embed a single backslash  in the value.</li>  </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


