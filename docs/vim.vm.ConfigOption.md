vim.vm.ConfigOption
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This configuration data object type contains information about the execution    environment for a virtual machine. This includes information about which features are    supported, such as:   <ul>      <li> Which guest operating systems are supported.      <li> How devices are emulated. For example, that a CD-ROM drive can be emulated            with a file or that a serial port can be emulated with a pipe.   </ul>   VirtualCenter can provide a broader environment than any single physical host. This    is a departure from traditional virtualization approaches, which rely on the host    system to define the environment for virtual machines. This data object describes    environment capabilities and is used by VirtualCenter to choose hosts on which to run    virtual machines.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| version | string | None | None | The version corresponding to this configOption. |
| description | string | None | None | A description string for this configOption. |
| guestOSDescriptor | [vim.vm.GuestOsDescriptor](vim.vm.GuestOsDescriptor.md "vim.vm.GuestOsDescriptor") | None | None | List of supported guest operating systems.  The choice of guest operating system may limit the set of valid devices.  For example, you cannot select Vmxnet with all guest operating systems. |
| guestOSDefaultIndex | int | None | None | Index into guestOsDescriptor array denoting the default guest  operating system. |
| hardwareOptions | [vim.vm.VirtualHardwareOption](vim.vm.VirtualHardwareOption.md "vim.vm.VirtualHardwareOption") | None | None | Processor, memory, and virtual device options for a virtual machine. |
| capabilities | [vim.vm.Capability](vim.vm.Capability.md "vim.vm.Capability") | None | None | Capabilities supported by a virtual machine. |
| datastore | [vim.vm.DatastoreOption](vim.vm.DatastoreOption.md "vim.vm.DatastoreOption") | None | None | The datastore options for this virtual machine. |
| defaultDevice | [vim.vm.device.VirtualDevice](vim.vm.device.VirtualDevice.md "vim.vm.device.VirtualDevice") | true | None | The list of virtual devices that are created on a virtual machine by default.    Clients should not create these devices. |
| supportedMonitorType | string | None | None | The monitor types supported by a host. The acceptable monitor types   are enumerated by <a href="vim.vm.FlagInfo.MonitorType.md">VirtualMachineFlagInfoMonitorType</a>. |
| supportedOvfEnvironmentTransport | string | true | None | Specifies the supported property transports that are   available for the OVF environment |
| supportedOvfInstallTransport | string | true | None | Specifies the supported transports for the OVF    installation phase. |


