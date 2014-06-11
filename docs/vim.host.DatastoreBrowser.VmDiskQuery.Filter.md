vim.host.DatastoreBrowser.VmDiskQuery.Filter
============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The filter for the virtual disk primary file.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskType | string | true | None | If this optional property is set, only the virtual disk primary files that   match one of the specified disk types are selected. If no disk types are   specified, this search criteria is ignored.   <p>   The specified disk type is one of the backing information types for a   virtual disk.<br>See <a href="vim.vm.device.VirtualDisk.md">VirtualDisk</a><br> |
| matchHardwareVersion | int | true | None | If this optional property is set, only virtual disk primary files that match   one of the specified hardware versions are selected.  If no versions are   specified, this search criteria is ignored. |
| controllerType | string | true | None | If this optional property is set, only virtual disk files that have a   controller type that matches one of the controller types specified   are returned. If no controller types are specified, this search criteria   is ignored.   <p>   The specified controller type is one of the controller types for a   virtual disk.<br>See <a href="vim.vm.device.VirtualIDEController.md">VirtualIDEController</a><br>See <a href="vim.vm.device.VirtualSCSIController.md">VirtualSCSIController</a><br> |
| thin | bool | true | None | This optional property can be used to filter disks based on whether   they are thin-provsioned or not: if set to true, only thin-provisioned   disks are returned, and vice-versa. |


