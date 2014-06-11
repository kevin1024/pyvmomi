vim.host.PhysicalNic.LinkSpeedDuplex
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.host.PhysicalNic.LinkSpeedDuplex.md">PhysicalNicLinkInfo</a> data object describes   the link speed and the type of duplex communication.  The link speed indicates   the bit rate in megabits per second.  The duplex boolean indicates if the link   is capable of full-duplex or half-duplex communication.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| speedMb | int | None | None | Bit rate on the link. |
| duplex | bool | None | None | Flag to indicate whether or not the link is capable of   full-duplex ("true") or only half-duplex ("false"). |


