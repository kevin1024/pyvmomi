vim.vm.StorageInfo.UsageOnDatastore
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Storage space used by this virtual machine on a particular datastore.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| datastore | [vim.Datastore](vim.Datastore.md "vim.Datastore") | None | None | Reference to datastore for which information is being provided. |
| committed | long | None | None | Storage space, in bytes, on this datastore that is actually being used by   the virtual machine.   <p>   It includes space actually occupied by disks, logs, snapshots,   configuration files etc. Files of the virtual machine which are present   on a different datastore (e.g. a virtual disk on another datastore) are not   included here. <a href="vim.vm.FileLayoutEx.md">VirtualMachineFileLayoutEx</a> provides a detailed   break-up of the committed space. |
| uncommitted | long | None | None | Additional storage space, in bytes, potentially used by the virtual machine   on this datastore.   <p>   Additional space may be needed for example when lazily allocated disks grow,   or storage for swap is allocated when powering on the virtual machine.   <p>   If the virtual machine is running off delta disks (for example because   a snapshot was taken), then only the potential growth of the currently   used delta-disks is considered. |
| unshared | long | None | None | Storage space, in bytes, occupied by the virtual machine on this datastore   that is not shared with any other virtual machine. |


