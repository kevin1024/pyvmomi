vim.host.StorageDeviceInfo
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the storage subsystem configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostBusAdapter | [vim.host.HostBusAdapter](vim.host.HostBusAdapter.md "vim.host.HostBusAdapter") | true | None | The list of host bus adapters available on the host. |
| scsiLun | [vim.host.ScsiLun](vim.host.ScsiLun.md "vim.host.ScsiLun") | true | None | The list of SCSI logical units available on the host. |
| scsiTopology | [vim.host.ScsiTopology](vim.host.ScsiTopology.md "vim.host.ScsiTopology") | true | None | Storage topology view of SCSI storage devices.  This data object   exists only if storage topology information is available.  See the   <a href="vim.host.ScsiTopology.md">ScsiTopology</a> data object type for   more information. |
| multipathInfo | [vim.host.MultipathInfo](vim.host.MultipathInfo.md "vim.host.MultipathInfo") | true | None | The multipath configuration that controls multipath policy for ScsiLuns.   This data object exists only if path information is available and is   configurable. |
| plugStoreTopology | [vim.host.PlugStoreTopology](vim.host.PlugStoreTopology.md "vim.host.PlugStoreTopology") | true | None | The plug-store topology on the host system.  This data object exists only if   the plug-store system is available and configurable. |
| softwareInternetScsiEnabled | bool | None | None | Indicates if the software iSCSI initiator is enabled on this system |


