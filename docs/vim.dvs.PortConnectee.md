vim.dvs.PortConnectee
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Information about the entity that connects to a DistributedVirtualPort.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| connectedEntity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | The connected entity.  This property should always be set unless the user's setting  does not have System.Read privilege on the object referred to  by this property. |
| nicKey | string | true | None | The key of the virtual NIC that connects to this port. |
| type | string | true | None | The type of the connectee.   See <a href="vim.dvs.PortConnectee.ConnecteeType.md">ConnecteeType</a> for valid values. |
| addressHint | string | true | None | A hint on address information of the NIC that connects to this port. |


