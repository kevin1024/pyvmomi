vim.dvs.VmwareDistributedVirtualSwitch.VspanFeatureCapability
=============================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Indicators of support for version-specific Distributed Port Mirroring sessions.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| mixedDestSupported | bool | None | None | Flag to indicate whether mixed dest mirror session is supported on the   vSphere Distributed Switch. |
| dvportSupported | bool | None | None | Flag to indicate whether dvport mirror session is supported on the   vSphere Distributed Switch. |
| remoteSourceSupported | bool | None | None | Flag to indicate whether remote mirror source session is supported on the   vSphere Distributed Switch. |
| remoteDestSupported | bool | None | None | Flag to indicate whether remote mirror destination session is supported on the   vSphere Distributed Switch. |
| encapRemoteSourceSupported | bool | None | None | Flag to indicate whether encapsulated remote mirror source session is supported on the   vSphere Distributed Switch. |


