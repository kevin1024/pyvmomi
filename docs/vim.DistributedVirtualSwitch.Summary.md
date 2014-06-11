vim.DistributedVirtualSwitch.Summary
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Summary of the distributed switch configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The name of the switch. |
| uuid | string | None | None | The generated UUID of the switch. |
| numPorts | int | None | None | Current number of ports, not including conflict ports. |
| productInfo | [vim.dvs.ProductSpec](vim.dvs.ProductSpec.md "vim.dvs.ProductSpec") | true | None | The product information for the implementation of the switch. |
| hostMember | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | The names of the hosts that join the switch. |
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | true | None | The Virtual Machines with Virtual NICs that connect to the switch.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter.    Since this property is on a DataObject, an update returned by WaitForUpdatesEx may   contain values for this property when some other property on the DataObject changes.   If this update is a result of a call to WaitForUpdatesEx with a non-empty   version parameter, the value for this property may not be current. |
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | The hosts with Virtual NICs that connect to the switch. |
| portgroupName | string | true | None | The names of the portgroups that are defined on the switch. |
| description | string | true | None | A description string of the switch. |
| contact | [vim.DistributedVirtualSwitch.ContactInfo](vim.DistributedVirtualSwitch.ContactInfo.md "vim.DistributedVirtualSwitch.ContactInfo") | true | None | The human operator contact information. |
| numHosts | int | true | None | The number of hosts in the switch. The value of this property   is not affected by the privileges granted to the current user. |


