vim.cluster.DasAdvancedRuntimeInfo
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Base class for advanced runtime information related to the high   availability service for a cluster.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dasHostInfo | [vim.cluster.DasHostInfo](vim.cluster.DasHostInfo.md "vim.cluster.DasHostInfo") | true | None | The information pertaining to the HA agents on the hosts |
| heartbeatDatastoreInfo | [vim.cluster.DasAdvancedRuntimeInfo.HeartbeatDatastoreInfo](vim.cluster.DasAdvancedRuntimeInfo.HeartbeatDatastoreInfo.md "vim.cluster.DasAdvancedRuntimeInfo.HeartbeatDatastoreInfo") | true | None | The map of a datastore to the set of hosts that are using  the datastore for storage heartbeating. |


