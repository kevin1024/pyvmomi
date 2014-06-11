vim.host.VmfsRescanResult
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


When a user resignatures an UnresolvedVmfsVolume through DatastoreSystem API,   we resignature and auto-mount on the other hosts which share the    same underlying storage luns. As part of the operation, we rescan host.   This data object describes the outcome of rescan operation on a host

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | Host name on which rescan was performed |
| fault | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | 'fault' would be set if the operation was not successful |


