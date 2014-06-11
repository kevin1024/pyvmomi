vim.vm.device.HostDiskMappingOption
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The HostDiskMappingOption data object type describes   the options for a virtual disk mapping to a host disk.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| physicalPartition | [vim.vm.device.HostDiskMappingOption.PartitionOption](vim.vm.device.HostDiskMappingOption.PartitionOption.md "vim.vm.device.HostDiskMappingOption.PartitionOption") | true | None | Array of valid partitions on this physical disk.   There is no default for this array. |
| name | string | None | None | Host resource name. |


