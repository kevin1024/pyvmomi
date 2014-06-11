vim.host.VmfsDatastoreSpec
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Base class for VMFS datastore addition specification.  Used as a generic   way to point to one of the creation specifications that can be used to   apply a specification to effect the creation or extension of a VMFS   datastore.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskUuid | string | None | None | The UUID of the SCSI disk on which the VMFS datastore is located.<br>See <a href="vim.host.ScsiDisk.md">HostScsiDisk</a><br>See <a href="vim.host.ScsiLun.md#uuid">uuid</a><br> |


