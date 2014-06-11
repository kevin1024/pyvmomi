vim.host.PciDevice
==================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes information about    a single Peripheral Component Interconnect (PCI) device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | The name ID of this PCI, composed of "bus:slot.function". |
| classId | short | None | None | The class of this PCI. |
| bus | int | None | None | The bus ID of this PCI. |
| slot | int | None | None | The slot ID of this PCI. |
| function | int | None | None | The function ID of this PCI. |
| vendorId | short | None | None | The vendor ID of this PCI.  <p>   The vendor ID might be a negative value. A vSphere Server uses an unsigned   short integer to represent a PCI vendor ID. The WSDL representation of the ID   is a signed short integer. If the vendor ID is greater than 32767, the Server   will convert the ID to its two's complement for the WSDL representation.   When you specify a PCI device vendor ID for a virtual machine   (<a href="vim.vm.device.VirtualPCIPassthrough.DeviceBackingInfo.md">VirtualPCIPassthroughDeviceBackingInfo</a>.vendorId),   you must use the retrieved <a href="vim.host.PciDevice.md">HostPciDevice</a>.deviceId value. |
| subVendorId | short | None | None | The subvendor ID of this PCI.  <p>  The subvendor ID might be a negative value.  A vSphere Server uses an unsigned   short integer to represent a PCI subvendor ID. The WSDL representation of the ID   is a signed short integer. If the subvendor ID is greater than 32767, the Server   will convert the ID to its two's complement for the WSDL representation. |
| vendorName | string | None | None | The vendor name of this PCI. |
| deviceId | short | None | None | The device ID of this PCI.   <p>   The device ID might be a negative value. A vSphere Server uses an unsigned   short integer to represent a PCI device ID. The WSDL representation of the ID   is a signed short integer. If the PCI ID is greater than 32767, the Server   will convert the ID to its two's complement for the WSDL representation.   When you specify a PCI device ID for a virtual machine   (<a href="vim.vm.device.VirtualPCIPassthrough.DeviceBackingInfo.md">VirtualPCIPassthroughDeviceBackingInfo</a>.deviceId),   you must use the <a href="vim.host.PciDevice.md">HostPciDevice</a>.deviceId value as retrieved   and convert it to a string. |
| subDeviceId | short | None | None | The subdevice ID of this PCI.  <p>  The subdevice ID might be a negative value.  A vSphere Server uses an unsigned  short integer to represent a PCI subdevice ID. The WSDL representation of the ID  is a signed short integer. If the subdevice ID is greater than 32767, the Server  will convert the ID to its two's complement for the WSDL representation. |
| parentBridge | string | true | None | The parent bridge of this PCI. |
| deviceName | string | None | None | The device name of this PCI. |


