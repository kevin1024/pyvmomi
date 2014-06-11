vim.host.DiskDimensions.Chs
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes dimensions using the cylinder,    head, sector (CHS) coordinate system.  This coordinate system    is generally needed for partitioning for legacy reasons.  When defining    partitions, many partitioning utilities do not function correctly when   certain CHS constraints are not met.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| cylinder | long | None | None | The number of cylinders. |
| head | int | None | None | The number of heads per cylinders. |
| sector | int | None | None | The number of sectors per head. |


