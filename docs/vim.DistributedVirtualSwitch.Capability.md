vim.DistributedVirtualSwitch.Capability
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.DistributedVirtualSwitch.Capability.md">DVSCapability</a> data object  describes the distributed virtual switch features and indicates  the level of configuration that is allowed.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dvsOperationSupported | bool | true | None | Indicates whether this switch allows vCenter users to modify   the switch configuration at the switch level,   except for host member, policy, and scope operations. |
| dvPortGroupOperationSupported | bool | true | None | Indicates whether this switch allows vCenter users to modify   the switch configuration at the portgroup level,   except for host member, policy, and scope operations. |
| dvPortOperationSupported | bool | true | None | Indicates whether this switch allows vCenter users to modify   the switch configuration at the port level,   except for host member, policy, and scope operations. |
| compatibleHostComponentProductInfo | [vim.dvs.HostProductSpec](vim.dvs.HostProductSpec.md "vim.dvs.HostProductSpec") | true | None | List of host component product information that is compatible   with the current switch implementation. |
| featuresSupported | [vim.DistributedVirtualSwitch.FeatureCapability](vim.DistributedVirtualSwitch.FeatureCapability.md "vim.DistributedVirtualSwitch.FeatureCapability") | true | None | Indicators for which version-specific distributed virtual switch  features are available on this switch.  <p>  This information is read-only, with the following exception.  For a third-party distributed switch implementation, you can  set the property  <a href="vim.DistributedVirtualSwitch.FeatureCapability.md">DVSFeatureCapability</a>.<a href="vim.DistributedVirtualSwitch.FeatureCapability.md#vmDirectPathGen2Supported">vmDirectPathGen2Supported</a>  during switch creation or when you call the  <a href="vim.DistributedVirtualSwitch.md#updateCapability">UpdateDvsCapability</a> method. |


