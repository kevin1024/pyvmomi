vim.vm.device.VirtualVMCIDevice
===============================
inherits from [vim.vm.device.VirtualDevice](docs/vim.vm.device.VirtualDevice.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version4)


The <a href="vim.vm.device.VirtualVMCIDevice.md">VirtualMachineVMCIDevice</a> data object represents  a virtual communication device that supports the VMCI  (Virtual Machine Communication Interface).  Each virtual machine has a VMCI device that handles  interprocess socket-based communication.  VMCI device information is available in the virtual machine  hardware device list  (<a href="vim.VirtualMachine.md">VirtualMachine</a>.<a href="vim.VirtualMachine.md#config">config</a>.<a href="vim.vm.ConfigInfo.md#hardware">hardware</a>.<a href="vim.vm.VirtualHardware.md#device">device</a>[]).  <p>  An application running on a virtual machine uses the VMCI Sockets API  for communication with other virtual machines on the same host  (communication between virtual machines is not supported on vSphere  5.1 and later platforms as described for  VirtualVMCIDevice.<a href="vim.vm.device.VirtualVMCIDevice.md#allowUnrestrictedCommunication">allowUnrestrictedCommunication</a>),  or for communication with the host.  For information about using the vSphere VMCI Sockets API,  see the <i>VMCI Sockets Programming Guide</i>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | long | true | None | Unique identifier for VMCI socket access to this virtual machine.   Use this value to identify this virtual machine in calls to the   VMCI Sockets API. Applications running on other virtual machines on this   host will use this value to connect to this virtual machine.   You can cast this value to a 32-bit unsigned integer.   <p>   The vSphere Server sets this value when a virtual machine   powers on. The Server may change this value after power   operations such as vMotion or restoring a virtual machine   from a snapshot. If you have saved a VMCI device identifier,   check to see if the value is still valid after power   operations. |
| allowUnrestrictedCommunication | bool | true | None | Determines the extent of VMCI communication with this virtual   machine. Set this property to true to allow VMCI communication   with all virtual machines on the host and with trusted services.   Set this property to false to allow VMCI communication only   with trusted services such as the hypervisor on the host.   <p>   If unset, communication is restricted to trusted services only.   <p> |


