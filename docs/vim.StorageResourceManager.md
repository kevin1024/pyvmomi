vim.StorageResourceManager
==========================
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


This managed object type provides a way to configure resource usage for   storage resources.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


ConfigureDatastoreIORM([datastore](vim.Datastore.md "vim.Datastore"), [spec](vim.StorageResourceManager.IORMConfigSpec.md "vim.StorageResourceManager.IORMConfigSpec"))
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.IORMNotSupportedHostOnDatastore](vim.fault.IORMNotSupportedHostOnDatastore.md "vim.fault.IORMNotSupportedHostOnDatastore"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InaccessibleDatastore](vim.fault.InaccessibleDatastore.md "vim.fault.InaccessibleDatastore")

---
| service name | ConfigureDatastoreIORM |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version6) |
| privilege    | None |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.IORMNotSupportedHostOnDatastore](vim.fault.IORMNotSupportedHostOnDatastore.md "vim.fault.IORMNotSupportedHostOnDatastore") | if called on a datastore that is           connected to a host that does not support storage I/O resource           management. |
| [vim.fault.InaccessibleDatastore](vim.fault.InaccessibleDatastore.md "vim.fault.InaccessibleDatastore") | if cannot access the datastore from any of the           hosts. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if called directly on a host or if called on a datastore           that does not have VMFS Volume. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if           1. IORMConfigSpec.congestionThreshold is not within the              desired range (5 to 100 milliseconds).           2. IORMConfigSpec.congestionThresholdMode is not specified and              IORMConfigSpec.congestionThreshold is specified. To set              congestionThreshold, congestionThresholdMode should be set to              manual |




QueryIORMConfigOption([host](vim.HostSystem.md "vim.HostSystem"))
-----------------------------------------------------------------

| service name | QueryIORMConfigOption |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version6) |
| privilege    | Datastore.Config |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryDatastorePerformanceSummary([datastore](vim.Datastore.md "vim.Datastore"))
-------------------------------------------------------------------------------
 raises [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryDatastorePerformanceSummary |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version6) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if input datastore cannot be found |




ApplyStorageDrsRecommendationToPod([pod](vim.StoragePod.md "vim.StoragePod"), [key](#string "string"))
------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | ApplyStorageDrsRecommendationToPod |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version6) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the specified key refers to a non-existent or an                           already executed recommendation.   <p> |




ApplyStorageDrsRecommendation([key](#string "string"))
------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | ApplyStorageDrsRecommendation |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version6) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the specified key refers to a non-existent or an                           already executed recommendation.   <p> |




CancelStorageDrsRecommendation([key](#string "string"))
-------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | CancelStorageDrsRecommendation |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version6) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the specified key refers to a non-existent or an                           already executed recommendation.   <p> |




RefreshStorageDrsRecommendation([pod](vim.StoragePod.md "vim.StoragePod"))
--------------------------------------------------------------------------

| service name | RefreshStorageDrsRecommendation |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version6) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




ConfigureStorageDrsForPod([pod](vim.StoragePod.md "vim.StoragePod"), [spec](vim.storageDrs.ConfigSpec.md "vim.storageDrs.ConfigSpec"))
--------------------------------------------------------------------------------------------------------------------------------------

| service name | ConfigureStorageDrsForPod |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version6) |
| privilege    | None |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|




RecommendDatastores([storageSpec](vim.storageDrs.StoragePlacementSpec.md "vim.storageDrs.StoragePlacementSpec"))
----------------------------------------------------------------------------------------------------------------

| service name | RecommendDatastores |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version6) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




