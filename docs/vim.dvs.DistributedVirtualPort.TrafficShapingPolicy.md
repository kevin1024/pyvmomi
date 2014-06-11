vim.dvs.DistributedVirtualPort.TrafficShapingPolicy
===================================================
inherits from [vim.InheritablePolicy](docs/vim.InheritablePolicy.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type describes traffic shaping policy.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | [vim.BoolPolicy](vim.BoolPolicy.md "vim.BoolPolicy") | true | None | The flag to indicate whether or not traffic shaper is enabled on   the port. |
| averageBandwidth | [vim.LongPolicy](vim.LongPolicy.md "vim.LongPolicy") | true | None | The average bandwidth in bits per second if shaping is enabled on   the port. |
| peakBandwidth | [vim.LongPolicy](vim.LongPolicy.md "vim.LongPolicy") | true | None | The peak bandwidth during bursts in bits per second if traffic   shaping is enabled on the port. |
| burstSize | [vim.LongPolicy](vim.LongPolicy.md "vim.LongPolicy") | true | None | The maximum burst size allowed in bytes if shaping is enabled on   the port. |


