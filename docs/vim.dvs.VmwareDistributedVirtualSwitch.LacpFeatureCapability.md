vim.dvs.VmwareDistributedVirtualSwitch.LacpFeatureCapability
============================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


The feature capabilities of Link Aggregation Control Protocol supported by the   vSphere Distributed Switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| lacpSupported | bool | true | None | Flag to indicate whether Link Aggregation Control Protocol is supported on the   vSphere Distributed Switch. |
| multiLacpGroupSupported | bool | true | None | Flag to indicate whether the vSphere Distributed Switch supports more   than one Link Aggregation Control Protocol group to be configured.   It is suppported in vSphere Distributed Switch Version 5.5 or later. |


