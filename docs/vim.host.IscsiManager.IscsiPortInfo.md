vim.host.IscsiManager.IscsiPortInfo
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The IscsiPortInfo data object describes the   Virtual NIC that are bound to an iSCSI adapter and   also it describes the candidate Virtual NICs that   can be bound to a given iSCSI adapter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vnicDevice | string | true | None | Virtual NIC Name.   Contains the name of the Virtual NIC device. This may be  unset in case where the bound Virtual NIC doesn't have the system object or  where a candidate Physical NIC isn't associated with any Virtual NIC. |
| vnic | [vim.host.VirtualNic](vim.host.VirtualNic.md "vim.host.VirtualNic") | true | None | Virtual NIC Object corresponding to the vnicDevice.   May be unset if Virtual NIC object corresponding to vnicDevice doesn't  exist in the system. |
| pnicDevice | string | true | None | Physical NIC Name. |
| pnic | [vim.host.PhysicalNic](vim.host.PhysicalNic.md "vim.host.PhysicalNic") | true | None | Physical NIC Object corresponding to the pnicDevice.   May be unset if Physical NIC object corresponding to pnicDevice doesn't  exist in the system or the vnicDevice doesn't have any Physical NIC  associated with it. |
| switchName | string | true | None | Name of the virtual switch this Physical/Virtual NIC belongs.   May be unset if the vnicDevice and/or pnicDevice do not have a  virtual switch associated with them. |
| switchUuid | string | true | None | UUID of the virtual switch this Physical/Virtual NIC belongs.   May be unset if the vnicDevice and/or pnicDevice do not have a  virtual switch associated with them or the associated switch is not VDS. |
| portgroupName | string | true | None | Name of the portgroup to which this Virtual NIC belongs.   May be unset if the vnicDevice and/or pnicDevice do not have a  Portgroup associated with them. |
| portgroupKey | string | true | None | Portgroup key to which this Virtual NIC belongs.   May be unset if the vnicDevice and/or pnicDevice do not have a  Portgroup associated with them or the associated portgroup does  is not of VDS type. |
| portKey | string | true | None | portkey to which this Virtual NIC belongs.   May be unset if the vnicDevice is not assigned to a specific port or  the switch is not VDS. |
| complianceStatus | [vim.host.IscsiManager.IscsiStatus](vim.host.IscsiManager.IscsiStatus.md "vim.host.IscsiManager.IscsiStatus") | true | None | Status indicating whether the Virtual NIC is compliant with the  network policy that is required by iSCSI port binding.   May be unset in the candidate NIC list. |
| pathStatus | string | true | None | A status, as defined in PathStatus, indicating the   existing storage paths dependency level on a given Virtual NIC.   May be unset in the candidate NIC list. |


