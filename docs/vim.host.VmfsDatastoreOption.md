vim.host.VmfsDatastoreOption
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


VMFS datastore provisioning option that can be applied on a disk.  VMFS   datastores can be created or have their capacity increased using storage   from a disk.   There are often multiple ways in which extents can be allocated on a disk.   Each instance of this structure represents one of the possible options   that can be applied to provisiong VMFS datastore storage.  Only options   that follow ESX Server best practice guidelines will be presented.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| info | [vim.host.VmfsDatastoreOption.Info](vim.host.VmfsDatastoreOption.Info.md "vim.host.VmfsDatastoreOption.Info") | None | None | Information about this VMFS datastore provisioniing option.  This   structure describes the extent allocation policy represented by   this option. |
| spec | [vim.host.VmfsDatastoreSpec](vim.host.VmfsDatastoreSpec.md "vim.host.VmfsDatastoreSpec") | None | None | Specification to create or increase the capacity of a VMFS datastore.   This property contains a configuration specification that can be   applied to effect the creation or capacity increase. |


