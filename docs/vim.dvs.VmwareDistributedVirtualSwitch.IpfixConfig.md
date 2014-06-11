vim.dvs.VmwareDistributedVirtualSwitch.IpfixConfig
==================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Configuration for IPFIX monitoring of distributed virtual switch traffic.   IPFIX monitoring must be enabled to use this capability. See   <a href="vim.dvs.VmwareDistributedVirtualSwitch.VmwarePortConfigPolicy.md">VMwareDVSPortSetting</a>.<a href="vim.dvs.VmwareDistributedVirtualSwitch.VmwarePortConfigPolicy.md#ipfixEnabled">ipfixEnabled</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| collectorIpAddress | string | true | None | IP address for the ipfix collector, specified using IPv4 dot notation.   This must be set before ipfix monitoring can be enabled for the   switch, or for any portgroup or port of the switch. |
| collectorPort | int | true | None | Port for the ipfix collector. This must be set before ipfix monitoring   can be enabled for the switch, or for any portgroup or port of the   switch. Legal value range is 0-65535. |
| activeFlowTimeout | int | None | None | The number of seconds after which "active" flows are forced to be   exported to the collector. Legal value range is 60-3600. Default 60. |
| idleFlowTimeout | int | None | None | The number of seconds after which "idle" flows are forced to be   exported to the collector. Legal value range is 10-600. Default 15. |
| samplingRate | int | None | None | The ratio of total number of packets to the number of packets   analyzed. Set to 0 to disable sampling. Legal value range is 0-1000.   Default 0. |
| internalFlowsOnly | bool | None | None | Whether to limit analysis to traffic that has both source and   destination served by the same host. Default false. |


