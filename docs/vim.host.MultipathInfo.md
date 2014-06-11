vim.host.MultipathInfo
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.host.MultipathInfo.md">HostMultipathInfo</a> data object describes the multipathing policy   configuration to determine the storage failover policies   for a SCSI logical unit.  The multipathing policy configuration operates on   SCSI logical units and the paths to the logical units.   <p>   Multipath policy configuration is only possible on storage devices   provided by the native multipathing plug-store plugin.  Storage devices   using the native multipathing storage plugin will have an entry   in this data object.  Storage devices provided by a different   storage plugin will not appear in the inventory represented by   this data object.   <p>   Legacy note: In hosts where <a href="vim.host.MultipathStateInfo.md">HostMultipathStateInfo</a> is not   defined or does not exist on the <a href="vim.host.StorageDeviceInfo.md">HostStorageDeviceInfo</a> object,   only native multipathing exists.  That means for these hosts, the   MultipathInfo object contains the complete set of LUNs and paths on the LUNs   available on the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| lun | [vim.host.MultipathInfo.LogicalUnit](vim.host.MultipathInfo.LogicalUnit.md "vim.host.MultipathInfo.LogicalUnit") | true | None | List of logical units that can be configured for multipathing. |


