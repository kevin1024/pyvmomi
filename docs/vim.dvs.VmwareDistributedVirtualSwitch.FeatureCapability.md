vim.dvs.VmwareDistributedVirtualSwitch.FeatureCapability
========================================================
inherits from [vim.DistributedVirtualSwitch.FeatureCapability](docs/vim.DistributedVirtualSwitch.FeatureCapability.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Indicators of support for version-specific DVS features that are only   available on a VMware-class switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vspanSupported | bool | true | None | Flag to indicate whether vspan(DVMirror) is supported on the   vSphere Distributed Switch.   Distributed Port Mirroring is supported in vSphere Distributed Switch Version 5.0 or later. |
| lldpSupported | bool | true | None | Flag to indicate whether LLDP(Link Layer Discovery Protocol) is supported on the   vSphere Distributed Switch.   LLDP is supported in vSphere Distributed Switch Version 5.0 or later. |
| ipfixSupported | bool | true | None | Flag to indicate whether IPFIX(NetFlow) is supported on the   vSphere Distributed Switch.   IPFIX is supported in vSphere Distributed Switch Version 5.0 or later. |
| vspanCapability | [vim.dvs.VmwareDistributedVirtualSwitch.VspanFeatureCapability](vim.dvs.VmwareDistributedVirtualSwitch.VspanFeatureCapability.md "vim.dvs.VmwareDistributedVirtualSwitch.VspanFeatureCapability") | true | None | The support for version-specific Distributed Port Mirroring sessions. |
| lacpCapability | [vim.dvs.VmwareDistributedVirtualSwitch.LacpFeatureCapability](vim.dvs.VmwareDistributedVirtualSwitch.LacpFeatureCapability.md "vim.dvs.VmwareDistributedVirtualSwitch.LacpFeatureCapability") | true | None | The support for version-specific Link Aggregation Control Protocol. |


