vim.vm.DatastoreInfo
====================
inherits from [vim.vm.TargetInfo](docs/vim.vm.TargetInfo.md)


DatastoreInfo describes a datastore that a virtual disk can be   stored on.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| datastore | [vim.Datastore.Summary](vim.Datastore.Summary.md "vim.Datastore.Summary") | None | None | Information about the datastore |
| capability | [vim.Datastore.Capability](vim.Datastore.Capability.md "vim.Datastore.Capability") | None | None | Information about the datastore capabilities |
| maxFileSize | long | None | None | The maximum size of a file that can reside on this datastore. |
| maxVirtualDiskCapacity | long | true | None | The maximum capacity of a virtual disk which can be created on this volume |
| mode | string | None | None | Access mode for this datastore. This is either   readOnly or readWrite. A virtual disk needs to be   stored on readWrite datastore. ISOs can be read   from a readOnly datastore.<br>See <a href="vim.host.MountInfo.AccessMode.md">HostMountMode</a><br> |
| vStorageSupport | string | true | None | Indicate the states of vStorage hardware acceleration  support for this datastore.  <p><br>See <a href="vim.host.FileSystemMountInfo.VStorageSupportStatus.md">FileSystemMountInfoVStorageSupportStatus</a><br> |


