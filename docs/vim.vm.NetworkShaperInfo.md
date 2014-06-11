vim.vm.NetworkShaperInfo
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Network traffic shaping specification.   <p>   Traffic shaping is used to configure the network utilization   characteristics of a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | true | None | Is the shaper enabled? |
| peakBps | long | true | None | Peak bandwidth, in bits per second. |
| averageBps | long | true | None | Average bandwidth, in bits per second. |
| burstSize | long | true | None | Burst size, in bytes. |


