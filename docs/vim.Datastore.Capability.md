vim.Datastore.Capability
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about the capabilities of this datastore.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| directoryHierarchySupported | bool | None | None | Indicates whether or not directories can be created on this datastore. |
| rawDiskMappingsSupported | bool | None | None | Indicates whether or not raw disk mappings can be created on this datastore. |
| perFileThinProvisioningSupported | bool | None | None | Indicates whether or not the datastore supports thin provisioning on a per file   basis. When thin provisioning is used, backing storage is lazily allocated.   <p>   This is supported by VMFS3. VMFS2 always allocates storage eagerly. Thus, this   value is false for VMFS2. Most NAS systems always use thin provisioning.   They do not support configuring this on a per file basis, so for NAS systems   this value is also false. |
| storageIORMSupported | bool | None | None | Indicates whether the datastore supports Storage I/O Resource Management. |
| nativeSnapshotSupported | bool | None | None | Indicates whether the datastore supports native snapshot feature which is   based on Copy-On-Write. |
| topLevelDirectoryCreateSupported | bool | true | None | Indicates whether the datastore supports traditional top-level   directory creation.<br>See <a href="vim.DatastoreNamespaceManager.md">DatastoreNamespaceManager</a><br> |
| seSparseSupported | bool | true | None | Indicates whether the datastore supports the Flex-SE(SeSparse) feature. |


