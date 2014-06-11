vim.host.DatastoreSystem.Capabilities
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Capability vector indicating the available product features.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| nfsMountCreationRequired | bool | None | None | Indicates whether mounting the NFS volume is required to be done as part   of NAS datastore creation. If this is set to true, then NAS datastores   cannot be created for currently mounted NFS volumes. |
| nfsMountCreationSupported | bool | None | None | Indicates whether mounting an NFS volume is supported   when a NAS datastore is created. If this option is false,   then NAS datastores corresponding to NFS volumes can be created   only for already mounted NFS volumes. |
| localDatastoreSupported | bool | None | None | Indicates whether local datastores are supported. |
| vmfsExtentExpansionSupported | bool | None | None | Indicates whether vmfs extent expansion is supported. |


