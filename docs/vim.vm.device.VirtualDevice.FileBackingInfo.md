vim.vm.device.VirtualDevice.FileBackingInfo
===========================================
inherits from [vim.vm.device.VirtualDevice.BackingInfo](docs/vim.vm.device.VirtualDevice.BackingInfo.md)


<code><a href="vim.vm.device.VirtualDevice.FileBackingInfo.md">VirtualDeviceFileBackingInfo</a></code> is a data object type   for information about file backing for a device in a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| fileName | string | None | None | Filename for the host file used in this backing. |
| datastore | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | None | Reference to the datastore managed object where this file is stored.   If the file is not located on a datastore, then this reference is null.   This is not used for configuration. |
| backingObjectId | string | true | None | Backing object's durable and unmutable identifier.  Each backing object has a unique identifier which is not settable. |


