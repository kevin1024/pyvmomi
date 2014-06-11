vim.DistributedVirtualSwitch.NetworkResourceManagementCapability
================================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Dataobject representing the feature capabilities of network resource management   supported by the vSphere Distributed Switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| networkResourceManagementSupported | bool | None | None | Indicates whether network I/O control is   supported on the vSphere Distributed Switch. Network I/O control   is supported in vSphere Distributed Switch Version 4.1 or later. |
| networkResourcePoolHighShareValue | int | None | None | High share level (<a href="vim.SharesInfo.Level.md">SharesLevel</a>.<a href="vim.SharesInfo.Level.md#high">high</a>)   for <a href="vim.dvs.NetworkResourcePool.AllocationInfo.md">DVSNetworkResourcePoolAllocationInfo</a>.<a href="vim.dvs.NetworkResourcePool.AllocationInfo.md#shares">shares</a>.   <p>   The <code>networkResourcePoolHighshareValue</code> property implicitly defines   the legal range of share values to be between 1 and this value.   This property also defines values for other level types, such as   <a href="vim.SharesInfo.Level.md#normal">normal</a> being one half of this value and   <a href="vim.SharesInfo.Level.md#low">low</a> being one fourth of this value.   This feature is supported in vSphere Distributed   Switch Version 4.1 or later. |
| qosSupported | bool | None | None | Indicates whether Qos Tag(802.1p priority tag)is supported on the   vSphere Distributed Switch. Qos Tag is supported in vSphere   Distributed Switch Version 5.0 or later. |
| userDefinedNetworkResourcePoolsSupported | bool | None | None | Indicates whether the switch supports creating user defined resource   pools. This feature is supported in vSphere Distributed   Switch Version 5.0 or later. |


