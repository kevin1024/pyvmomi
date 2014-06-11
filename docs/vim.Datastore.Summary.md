vim.Datastore.Summary
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Summary information about the datastore. The status fields and managed object   reference is not set when an object of this type is created. These fields and   references are typically set later when these objects are associated with a host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| datastore | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | None | The reference to the managed object. |
| name | string | None | None | The name of the datastore. |
| url | string | None | None | The unique locator for the datastore. This property is guaranteed to be valid   only if <a href="vim.Datastore.Summary.md#accessible">accessible</a> is true. |
| capacity | long | None | None | Maximum capacity of this datastore, in bytes. This value is updated   periodically by the server. It can be explicitly refreshed with the Refresh   operation. This property is guaranteed to be valid only if <a href="vim.Datastore.Summary.md#accessible">accessible</a>   is true. |
| freeSpace | long | None | None | Available space of this datastore, in bytes. The server periodically   updates this value. It can be explicitly refreshed with the Refresh operation.   This property is guaranteed to be valid only if <a href="vim.Datastore.Summary.md#accessible">accessible</a> is true. |
| uncommitted | long | true | None | Total additional storage space, in bytes, potentially used by all   virtual machines on this datastore. The server periodically updates this   value.   It can be explicitly refreshed with the <a href="vim.Datastore.md#refreshStorageInfo">RefreshDatastoreStorageInfo</a> operation.   This property is valid only if <a href="vim.Datastore.Summary.md#accessible">accessible</a> is true. |
| accessible | bool | None | None | The connectivity status of this datastore. If this is set to false, meaning the   datastore is not accessible, this datastore's capacity and freespace properties   cannot be validated. Furthermore, if this property is set to false, some of the   properties in this summary and in <a href="vim.Datastore.Info.md">DatastoreInfo</a> should not be   used. Refer to the documentation for the property of your interest.    For datastores accessed from multiple hosts, vCenter Server reports   <a href="vim.Datastore.Summary.md#accessible">accessible</a> as an aggregated value of the   properties reported in MountInfo. For instance,   if a datastore is accessible through a subset of hosts, then the value of   <a href="vim.Datastore.Summary.md#accessible">accessible</a> will be reported as true by   vCenter Server. And the reason for a daastore being inaccessible from a host   will be reported in <a href="vim.host.MountInfo.md#inaccessibleReason">inaccessibleReason</a> |
| multipleHostAccess | bool | true | None | More than one host in the datacenter has been configured with access to the  datastore. This is only provided by VirtualCenter. |
| type | string | None | None | Type of file system volume, such as VMFS or NFS.<br>See <a href="vim.host.FileSystemVolume.md#type">type</a><br> |
| maintenanceMode | string | true | None | The current maintenance mode state of the datastore. The set of   possible values is described in <a href="vim.Datastore.Summary.MaintenanceModeState.md">DatastoreSummaryMaintenanceModeState</a>. |


