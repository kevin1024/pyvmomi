vim.host.PortGroup.Port
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


A Port data object type is a runtime representation of network    connectivity between a network service or virtual machine and a   virtual switch.  This is different from a port group in that    the port group represents the configuration aspects of the   network connection.  The Port object provides runtime statistics.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | true | None | The linkable identifier. |
| mac | string | true | None | The Media Access Control (MAC) address of network service of    the virtual machine connected on this port. |
| type | string | None | None | The type of component connected on this port.  Must be one of the   values of <a href="vim.host.PortGroup.PortConnecteeType.md">PortGroupConnecteeType</a>. |


