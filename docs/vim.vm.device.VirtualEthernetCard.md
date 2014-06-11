vim.vm.device.VirtualEthernetCard
=================================
inherits from [vim.vm.device.VirtualDevice](docs/vim.vm.device.VirtualDevice.md)


The <a href="vim.vm.device.VirtualEthernetCard.md">VirtualEthernetCard</a> data object contains the properties   of an Ethernet adapter attached to a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| addressType | string | true | None | MAC address type.   <p>   Valid values for address type are:   <table>   <dt>Manual</dt>   <dd>Statically assigned MAC address.</dd>   <dt>Generated</dt>   <dd>Automatically generated MAC address.</dd>   <dt>Assigned</dt>   <dd>MAC address assigned by VirtualCenter.</dd>   </table> |
| macAddress | string | true | None | MAC address assigned to the virtual network adapter. Clients can   set this property to any of the allowed address types. The server might   override the specified value for "Generated" or "Assigned" if it does not   fall in the right ranges or is determined to be a duplicate. |
| wakeOnLanEnabled | bool | true | None | Indicates whether wake-on-LAN is enabled on this virtual network adapter. Clients  can set this property to selectively enable or disable wake-on-LAN. |


