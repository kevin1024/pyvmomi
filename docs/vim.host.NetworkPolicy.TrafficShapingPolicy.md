vim.host.NetworkPolicy.TrafficShapingPolicy
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes traffic shaping policy.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | true | None | The flag to indicate whether or not traffic shaper is enabled on   the port. |
| averageBandwidth | long | true | None | The average bandwidth in bits per second if shaping is enabled on   the port. |
| peakBandwidth | long | true | None | The peak bandwidth during bursts in bits per second if traffic   shaping is enabled on the port. |
| burstSize | long | true | None | The maximum burst size allowed in bytes if shaping is enabled on   the port. |


