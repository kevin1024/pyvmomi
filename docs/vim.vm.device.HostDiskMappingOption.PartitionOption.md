vim.vm.device.HostDiskMappingOption.PartitionOption
===================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The PhysicalPartitionOption data class contains the options   for a partition on a physical disk.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | Partition name. |
| fileSystem | string | None | None | File system, if the partition is formatted. |
| capacityInKb | long | None | None | Partition capacity, in KB. |


